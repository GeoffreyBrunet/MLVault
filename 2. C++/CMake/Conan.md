**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake  

# About
[Conan](https://conan.io) is package manager for C/C++, written in python.

# Commands
## Create user after installation
```shell
conan user
```

## Install package from repo
Repository for Conan can be found at this [here](https://conan.io/center/).
Create a file called `conanfile.txt` at root of project with package name and it's version.
Example:
```txt
[requires]
boost/1.80.0
```
Generators are specific components that provide the information of dependencies calculated by Conan in a suitable format for a build system.
```txt
[generators]
cmake
```
And install all packages with:
```shell
conan install .
```

# Use dependencies in [[CMakeLists.txt]]
```txt
target_link_libraries(
	${CONAN_LIBNAME}
)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()
```
