# windows-python-installer

### What's it

A windows python installer repack which is support on windows 7+. This project do the following changes of the official [cpython](https://github.com/python/cpython) 

- [x] Modify the windows installer, remove os limitation for making the installer to work on windows 7+.
- [x] Build on `Visual Studio 2022` as my local or the default in github actions is `Visual Studio 2022`.
- [x] Change the font of `pythonXY.chm` to `'Microsoft YaHei'` as the default looks ugly.
- [ ] Include `api-ms-win-core-path-l1-1-0.dll` which is from https://github.com/nalexandru/api-ms-win-core-path-HACK in the installer to support running python 3.9+ on windows 7+.

### Motivation

I wrote a simple pyqt5 based app which use python 3.10 and packaged via pyinstaller, but the app could not run on windows 7. After some tries, I made it to work on windows 7. Some discussion could be found on https://github.com/orgs/pyinstaller/discussions/6200.

Maybe someone else need to run python 3.9, 3.10 or later versions on their windows 7, so I create this project to help them.

### Reference

- https://cpython-core-tutorial.readthedocs.io/en/latest/build_cpython_windows.html

### License

MIT License

Copyright (c) 2022 liudonghua