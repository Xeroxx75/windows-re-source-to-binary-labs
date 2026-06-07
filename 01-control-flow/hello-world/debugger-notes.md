# Debugger Notes - hello-world

## Goal

Observe the path from the PE entry point toward the user `main` function.

## x64dbg Setup

- Binary:
- Breakpoint at system breakpoint: yes / no
- Breakpoint at entry point: yes / no
- Breakpoint at `main`: yes / no

## Observations

- Initial module:
- Entry point address:
- Current thread:
- Call stack before `main`:
- Function that calls `main`:
- Address of `main`:

## Registers Near `main`

| Register | Value | Meaning |
| --- | --- | --- |
| RIP |  |  |
| RSP |  |  |
| RCX |  |  |
| RDX |  |  |
| R8 |  |  |
| R9 |  |  |

## Breakpoints

| Breakpoint | Reason | Result |
| --- | --- | --- |
| Entry point | Observe loader to runtime transition |  |
| `main` | Observe user code |  |

## Notes

- 
