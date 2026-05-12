# Pymsym for Windows [pre-compiled version]

## About pymsym and libmsym
Pymsym is currently maintained by Corin Wagen [https://github.com/corinwagen/pymsym]. The original libmsys was developed by Marcus Johansson [https://github.com/mcodev31/libmsym].

## What is this repository for?
I found that the installation of pymsym via pip on Windows is somewhat problematic probably due to imcompatibility of MSVC with C99. This repository gives a Windows version of pymsym precompiled by MSYS2/MinGW64 via almost static linking.

My motivation to use this library is Goodvibes [https://github.com/patonlab/goodvibes] version 4 or later depends on pymsym for molecular symmetry checking. 

## How to install
Download all files (pyproject.toml and pymsym directory) then

```
cd /to/your/directory/with_pyproject.toml
pip install .
```

Or if git is available, you may be able to directory install from this repository.

`pip install git+https://github.com/npe1011/pymsym-win.git`

`uv add git+https://github.com/npe1011/pymsym-win.git`

numpy is required. I did not check the version dependency of numpy.

## Cautions
Only a few tests have been done. Please let me know if you have any problems.


This is prepared with the assistance of Gemini.
