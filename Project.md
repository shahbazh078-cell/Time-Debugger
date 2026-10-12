# Time-Debugger
# Project Progress

# 1: Stack Implementation and Pass 0x0 Validation


### Completed
- Set up the project in Visual Studio Community.
- Implemented a custom linked-list Stack class.
- Created helpers firstWord, secondWord that handle Windows `\r` line endings, spaces, and tabs.
- Implemented validateProgram to enforce func / func_end matching and reject nested function declarations.

### Concepts Learned
- Generic LIFO Stack data structure using linked nodes.
- Grammatical scoping validation and handling cross-platform line-ending issues in C++.

## 2: Pass 0x1 - Resolve & Patching

### Completed
- Wrote the writeResolveRecord and readResolveRecord functions.
- Finished `resolveProgram`. 
- Set up the `FuncEntry` and `PendingPatch` arrays to keep track of where functions are defined and where `call` instructions happen.
- Got the patching working! Used `fseek` to jump back in the binary file and overwrite the 8-byte offset field for `call` targets without messing up the string sizes.
-the program throws an error if there's no `main` function or if a called function doesn't exist.

