# Libsass Test Plugin

Native libsass plugin for testing purposes only

## Building

You need to have [libsass] [1] already [compiled] [2] or [installed] [3] as a
shared library (inclusive header files). It is then compiled via `cmake`. See
this example to compile it on windows via [MinGW] [4] Compiler Suite:

```cmd
git clone https://github.com/sass/libsass.git
mingw32-make -C libsass BUILD=shared CC=gcc -j5
git clone https://github.com/mgreter/libsass-test.git
cd libsass-test && mkdir build && cd build
cmake -G "MinGW Makefiles" .. -DLIBSASS_DIR="..\..\libsass"
mingw32-make CC=gcc -j5 && dir test.dll
```

You may define `LIBSASS_INCLUDE_DIR` and `LIBSASS_LIBRARY_DIR` separately!

## Copyright

� 2017 [Marcel Greter] [5]

[1]: https://github.com/sass/libsass
[2]: https://github.com/sass/libsass/wiki/Building-Libsass
[3]: http://libsass.ocbnet.ch/installer/
[4]: http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/
[5]: https://github.com/mgreter

