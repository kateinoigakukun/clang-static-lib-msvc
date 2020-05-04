Clang assumes that static library doesn't have `lib` prefix on msvc.

```bash
$ clang.exe -c StaticLib.c -o StaticLib.o
$ ar.exe rcs StaticLib.lib StaticLib.o
$ clang.exe -c main.c -L. -lStaticLib
```
