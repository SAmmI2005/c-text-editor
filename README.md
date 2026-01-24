# C Text Editor (Undo Stack)

A minimalist command-line text editor written in C. Text is stored as a linked list of lines,
and undo is implemented using a stack of full document snapshots (deep copies).

## Features
- Append, insert, delete, and replace lines
- File open/save support
- Multi-level undo using snapshot stack
- Unit-tested editor library
- Memory checked with Valgrind (leak-free)

## Build
```bash
make
