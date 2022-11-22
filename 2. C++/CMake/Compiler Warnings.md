**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# About
Goal of this not is to be sure our [[CMake]] project can be compiled with 3 main compilers:
- **Clang** (LLVM)
- **G++** (GCC)
- **MSVC**

For configure warnings, example here show code for using warnings, a lot of other can be added: [Warning examples](https://github.com/franneck94/UdemyCmake/blob/master/2_CMake/12_Final/cmake/Warnings.cmake). **Clang** and **GCC** have common warnings.

This following code check which compiler we are currently using:
```CMAKE
if(CMAKE_CXX_COMPILER_ID MATCHES "MSVC")
	set(PROJECT_WARNINGS ${MSVC_WARNINGS})
elseif(CMAKE_CXX_COMPILER_ID MATCHES "Clang")
	set(PROJECT_WARNINGS ${CLANG_WARNINGS})
elseif(CMAKE_CXX_COMPILER_ID MATCHES "GNU")
	set(PROJECT_WARNINGS ${GCC_WARNINGS})
endif()
```

Target can be specified with this following function:
```cmake
target_compile_options(${target_set_warnings_TARGET} PRIVATE ${PROJECT_WARNINGS})
```

In main CMakeLists.txt, enable warnings:
```cmake
option(ENABLE_WARNINGS "Enable to add warnings to a target" ON)
```

For stopping compiling and get error if a warning is emitted, add in main CMakeLists.txt:
```cmake
if (${ENABLE_WARNINGS})
	target_set_warnings(TARGET ${EXECUTABLE_NAME} ENABLE ON AS_ERROR ON)
endif()
```
