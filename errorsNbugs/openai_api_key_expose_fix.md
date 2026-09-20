# OpenAI API Key & Git Security Fix

## OBJECTIVE

Secure the OpenAI API key and prevent `.env` from being committed to Git.

## What Was Solved

* Revoked the previously exposed API key and created a new one.
* Added `.env` to `.gitignore`.
* Removed `.env` from Git tracking while keeping it locally:

  ```bash
  git rm --cached .env
  ```
* Amended the commit so `.env` is no longer included.

## Verification

Check `.env` is no longer tracked:

```bash
git ls-files .env
```

→ **No output**

Check `.env` is ignored:

```bash
git check-ignore -v .env
```

→ Should show:

```text
.gitignore:2:.env    .env
```

Check the latest commit:

```bash
git show --stat --oneline HEAD
```

→ `.env` should **not** appear.

## Key Takeaway

`.gitignore` prevents untracked files from being committed. A file already tracked by Git must first be removed with:

```bash
git rm --cached <file>