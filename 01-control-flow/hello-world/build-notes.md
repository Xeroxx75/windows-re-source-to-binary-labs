# Build Notes - hello-world

## Goal

Compile a minimal C program into Windows PE executables and compare Debug vs Release builds.

## Predictions Before Build

- I expect the output to be a Windows PE console executable.
- I expect x64 builds to be identified as PE32+.
- I expect the string `Hello, Windows reverse engineering!` to remain visible.
- I expect runtime/compiler code to appear before my `main`.
- I do not expect file, registry, thread or network APIs from my source code.

## MSVC x64 Commands

Run from **x64 Native Tools Command Prompt for VS**:

```bat
cd path\to\windows-re-source-to-binary-labs\01-control-flow\hello-world\src
cl /nologo /W4 /Zi /Od /Fe:..\hello-x64-debug.exe hello.c
cl /nologo /W4 /O2 /Fe:..\hello-x64-release.exe hello.c
```

## MinGW-w64 Commands

Run from Linux if MinGW-w64 is installed:

```bash
cd windows-re-source-to-binary-labs/01-control-flow/hello-world/src
x86_64-w64-mingw32-gcc -Wall -Wextra -O0 -g -o ../hello-x64-debug.exe hello.c
x86_64-w64-mingw32-gcc -Wall -Wextra -O2 -s -o ../hello-x64-release.exe hello.c
```

## Build Results

| Build | Command | Output | SHA256 | Notes |
| --- | --- | --- | --- | --- |
| x64 Debug |  |  |  |  |
| x64 Release |  |  |  |  |

## Surprises

- 
