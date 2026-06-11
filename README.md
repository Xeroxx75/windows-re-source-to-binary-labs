# Windows RE Source-to-Binary Labs

Progressive reverse engineering labs on small Windows programs written from source, compiled into PE files, then analyzed statically and dynamically.

## Goal

Build Windows reverse engineering fundamentals before analyzing real malware.

The workflow is always:

```text
Write source
Predict expected observations
Compile variants
Inspect the PE
Inspect disassembly and decompiler output
Run under observation
Debug selected functions
Modify the source
Compare differences
Document surprises
```

## Structure

```text
01-control-flow/
02-functions-and-calling-conventions/
03-win32-files-and-registry/
04-processes-and-threads/
05-dll-and-dynamic-imports/
06-tls-callbacks/
07-compiler-options/
08-packing-with-upx/
templates/
```

Each experiment uses:

```text
experiment-name/
├── src/
├── build-notes.md
├── static-analysis.md
├── dynamic-analysis.md
├── debugger-notes.md
├── screenshots/
└── conclusions.md
```

## Current Labs

- `01-control-flow/hello-world`: first PE compilation and analysis workflow.
