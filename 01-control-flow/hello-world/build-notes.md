# Build Notes - hello-world

## Goal

Compile a minimal C program into Windows PE executables and compare Debug vs Release builds.

## Predictions Before Build

- I expect the output to be a Windows PE console executable.
- I expect x64 builds to be identified as PE32+.
- I expect the string `Hello, Windows reverse engineering!` to remain visible.
- I expect runtime/compiler code to appear before my `main`.
- I do not expect file, registry, thread or network APIs from my source code.

## MinGW-w64 Commands

Run from Linux if MinGW-w64 is installed:

```bash
cd windows-re-source-to-binary-labs/01-control-flow/hello-world/src
x86_64-w64-mingw32-gcc -Wall -Wextra -O0 -g -o ../hello-x64-debug.exe hello.c
x86_64-w64-mingw32-gcc -Wall -Wextra -O2 -s -o ../hello-x64-release.exe hello.c
```

- `O0`: no optimization, used to make source-to-assembly matching easier.  
- `g`: adds debug information.  
- `O2`: optimized compilation, used to observe compiler transformations.  
- `s`: strips symbols, to observe a binary closer to a release build.

Debug = more readable, closer to the source  
Release = more optimized, less readable, closer to a real distributed binary

## Build Results

| Build | Command | Output | SHA256 | Notes |
| --- | --- | --- | --- | --- |
| x64 Debug | `x86_64-w64-mingw32-gcc -Wall -Wextra -O0 -g -o ../hello-x64-debug.exe hello.c` | `hello-x64-debug.exe` | 2c3cf2a368cb1e2a912357874a0dd807c2e4a2b9ab4a869ee1fd378646a440c3 | Debug symbols included; easier to inspect |
| x64 Release | `x86_64-w64-mingw32-gcc -Wall -Wextra -O2 -s -o ../hello-x64-release.exe hello.c` | `hello-x64-release.exe` | 3b6e8651314450fc2ccaefb6d592ff28401d3e8481c6c6d2bcfd21f47635bd6a | Stripped and optimized |

## Surprises

- 
