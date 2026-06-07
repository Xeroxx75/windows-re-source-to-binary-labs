# Static Analysis - hello-world

Use the vault note `04-PRACTICE/static-analysis-playbook.md` as the checklist. This file is the concrete report for this experiment, not a copy of the whole course note.

## 0. Context

- Source: self-written `src/hello.c`.
- Goal: identify the PE structure, entry point path and visible artifacts of a minimal program.
- Execution status: not executed during this phase.

## 1. Identification

| Item | Debug | Release |
| --- | --- | --- |
| File name |  |  |
| File type |  |  |
| Architecture |  |  |
| Size |  |  |
| SHA256 |  |  |
| Compiler hints |  |  |

## 2. PE Structure

| Item | Debug | Release |
| --- | --- | --- |
| Subsystem |  |  |
| Entry point RVA |  |  |
| Entry point section |  |  |
| Sections |  |  |
| TLS callbacks |  |  |
| Resources |  |  |
| Relocations |  |  |

## 3. Imports

Expected:

- C runtime related imports.
- Console/output related runtime path.
- No explicit Win32 file, registry, process, thread or network API from the source.

Observed:

- Debug:
- Release:

## 4. Strings

Expected:

- `Hello, Windows reverse engineering!`

Observed:

- Debug:
- Release:

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
