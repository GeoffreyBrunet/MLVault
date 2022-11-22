**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

> A library is a binary file that contains informations about code, and is not executable.

# Shared library
- Shared libraries reduce the amount of code that is duplicated in each program that makes use of the library, keeping the binaries small. It also allows you to replace the shared object with one that is functionally equivalent, without needing to recompile the program that makes use of it.
- Shared libraries will however have a small additional cost for the execution.
- _Examples_:
	- Linux: .so
	- macOS: .dylib
	- Windows: .dll

# Static library
- Static libraries increase the overall size of the binary, but it means that you don't need to carry along a copy of the library that is being used.
- As the code is connected at compile time there are not any additional run-time loading costs. The code is simply there.
- _Examples_:
	- Linux / macOS: .a
	- Windows: .lib
