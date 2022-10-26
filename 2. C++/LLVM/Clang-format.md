**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #llvm
**Doc**:: [Clang-Format Style Options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html)
## Basic file
Create `.clang.format` in c++ project for set formatting parameters for [clang](https://clang.llvm.org).
Basic `.clang.format` file contains:
```
# set style formatting
BasedOnStyle: LLVM
# set number spaces when indent
IndentWidth: 4
# set langage
Language: Cpp
# set pointer on var type and not on name
DerivePointerAlignment: false
PointerAlignment: Left
```
