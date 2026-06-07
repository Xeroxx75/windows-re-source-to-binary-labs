# Experiment Template

## Metadata

- Experiment:
- Date:
- Goal:
- OS:
- Compiler:
- Architecture:
- Build mode:
- SHA256:

## Starting Question

What exact change or concept am I trying to observe?

## Predictions Before Analysis

Fill this before opening PE-bear, Detect It Easy, Ghidra, x64dbg or Procmon.

### Expected PE Structure

- File type:
- Architecture:
- Subsystem:
- Expected sections:
- Expected entry point area:
- Expected imports:
- Expected strings:
- Expected resources:
- Expected TLS callbacks:

### Expected Disassembly

- Functions I expect to recognize:
- Branches I expect to see:
- Loops I expect to see:
- Compiler/runtime code I expect before `main`:
- Debug vs Release differences I expect:

### Expected Runtime Behavior

- Child processes:
- Secondary threads:
- File activity:
- Registry activity:
- DLL loads:
- Network activity:
- API breakpoints worth setting:

## Source Notes

- Important functions:
- Important strings:
- Important API calls:
- Control-flow elements:

## Build Notes

- Commands:
- Warnings:
- Output files:
- Hashes:
- Build differences:

## Static Analysis

- Identification:
- PE structure:
- Imports:
- Strings:
- Entry point:
- Path toward `main`:
- Functions of interest:
- Surprises:

## Dynamic Analysis

- Environment:
- Tools:
- Process activity:
- Thread activity:
- File activity:
- Registry activity:
- Network activity:
- Surprises:

## Debugger Notes

- Breakpoints:
- Call stack:
- Registers:
- Arguments:
- Return values:
- Memory observations:

## Comparison

- Correct predictions:
- Wrong predictions:
- Missing predictions:
- Source vs binary differences:
- Debug vs Release differences:

## Conclusion

- What I learned:
- What surprised me:
- What to test next:
