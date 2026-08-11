# Static Analysis - hello-world

## 0. Context

- Source: self-written `src/hello.c`.
- Goal: identify the PE structure, entry point path and visible artifacts of a minimal program.
- Execution status: not executed during this phase.

## 1. Identification

| Item | Debug | Release |
| --- | --- | --- |
| File name | `hello-x64-debug.exe` | `hello-x64-release.exe` |
| File type | `PE64` | `PE64` |
| Architecture | `AMD64` | `AMD64` |
| Size | `241.53 KiB` | `39.00 KiB` |
| SHA256 | `2c3cf2a368cb1e2a912357874a0dd807c2e4a2b9ab4a869ee1fd378646a` | `3b6e8651314450fc2ccaefb6d592ff28401d3e8481c6c6d2bcfd21f47635bd6a` |
| Compiler hints | `msvcrt.dll`; `__mingw_app_type`; DIE: MinGW | MinGW-w64 runtime; DIE heuristic: Microsoft Visual C/C++ |

## 2. PE Structure

| Item                | Debug        | Release      |
| ------------------- | ------------ | ------------ |
| Subsystem           | `WINDOW_CUI` | `WINDOW_CUI` |
| Entry point RVA     | `000014d0`   | `000014d0`   |
| Entry point section | `.text`      | `.text`      |
| Sections            | 19           | 10           |
| TLS callbacks       | 2            | 2            |
| Resources           | None         | None         |
| Relocations         | 4 blocks     | 4 blocks     |

## 3. Imports

Expected:

- Windows API imports from `KERNEL32.dll`.
- C runtime (CRT) imports from `msvcrt.dll`.

Observed:

- Debug: `KERNEL32.dll` & `msvcrt.dll`
- Release: `KERNEL32.dll` & `msvcrt.dll`

## 4. Strings

Expected:

- `Hello, Windows reverse engineering!`

Observed:

- Debug: `Hello, Windows reverse engineering!`
- Release: `Hello, Windows reverse engineering!`

## 5. Ghidra Notes

- Entry point function:
- Path toward `main`:
- Name Ghidra gives to `main`:
- Runtime functions noticed:
- Decompiled `main`:

## 6. Prediction Check

| Prediction | Result | Notes |
| --- | --- | --- |
| PE console executable |  |  |
| String visible |  |  |
| Runtime before `main` |  |  |
| No suspicious APIs |  |  |

## 7. Static Conclusion

- What is confirmed:
- What is still unclear:
- What to verify dynamically:
