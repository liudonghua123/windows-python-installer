# windows-python-installer

### What's it

A windows python installer repack which is support on windows 7+. This project do the following changes of the official [cpython](https://github.com/python/cpython) 

- [x] Modify the windows installer, remove os limitation for making the installer to work on windows 7+.
- [x] Build on `Visual Studio 2022` as my local or the default in github actions is `Visual Studio 2022`.
- [x] Change the font of `pythonXY.chm` to `'Microsoft YaHei'` as the default looks ugly.
- [x] Include `api-ms-win-core-path-l1-1-0.dll` which is from https://github.com/nalexandru/api-ms-win-core-path-HACK in the installer to support running python 3.9+ on windows 7+.

### Motivation

I wrote a simple pyqt5 based app which use python 3.10 and packaged via pyinstaller, but the app could not run on windows 7. After some tries, I made it to work on windows 7. Some discussion could be found on https://github.com/orgs/pyinstaller/discussions/6200.

Maybe someone else need to run python 3.9, 3.10 or later versions on their windows 7, so I create this project to help them.

### Remarks

In order to run this python 3.9/3.10/3.11 on windows 7, you need windows 7 sp1 and install [UCRT](https://support.microsoft.com/en-us/topic/update-for-universal-c-runtime-in-windows-c0514201-7fe6-95a3-b0a5-287930f3560c) which is provided as [KB2999226](https://www.microsoft.com/en-us/download/details.aspx?id=49077).

For python 3.12, due to use of `AddDllDirectory`, you need to install `KB2533623`, see also [Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/en-us/topic/microsoft-security-advisory-insecure-library-loading-could-allow-remote-code-execution-486ea436-2d47-27e5-6cb9-26ab7230c704), [adang1345/PythonWin7/Notes.md](https://github.com/adang1345/PythonWin7/blob/master/Notes.md).

The `KB2533623` could not download anymore, so I upload to `resources` directory.

### Reference

- https://cpython-core-tutorial.readthedocs.io/en/latest/build_cpython_windows.html

### License

MIT License

Copyright (c) 2022 liudonghua