Absolutely — here’s the smaller `.md` version with the directories included:

````md
# Python & uv Setup / Fix

## Python Directory

Python was installed under:

```text
C:\Users\<username>\AppData\Local\Programs\Python\Python313\
````

Python executable:

```text
C:\Users\<username>\AppData\Local\Programs\Python\Python313\python.exe
```

## uv Directory

`uv` was installed in Python's Scripts directory:

```text
C:\Users\<username>\AppData\Local\Programs\Python\Python313\Scripts\
```

The `uv.exe` executable is located there:

```text
C:\Users\<username>\AppData\Local\Programs\Python\Python313\Scripts\uv.exe
```

## Verification

Check Python:

```bash
python --version
```

Check uv:

```bash
uv --version
```

Verify uv package:

```bash
python -m pip show uv
```

Confirmed installed version:

```text
uv 0.12.10
```

## Fix

The issue was caused by the Python `Scripts` directory not being correctly available in `PATH`.

Adding the following to `PATH` makes `uv` available from any terminal:

```text
C:\Users\<username>\AppData\Local\Programs\Python\Python313\Scripts\