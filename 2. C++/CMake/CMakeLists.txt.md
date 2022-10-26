**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake

## What is it
It's file need to be present at root of C/C++ project for using it. It contain a lot of informations for compiler and about project, as dependencies for example. If project contains multiple folders, create a `CMakeLists.txt` in each folder.

## Directives and instructions
### CMake version check:
```txt
cmake_minimum_required(VERSION 3.16)
```

### Create project "simple_example":
```txt
project(simple_example VERSION 1.0.0 LANGAGES CXX)
```

### Add library
```txt
add_library(Library STATIC my_lib.cc) 
```

### Add executable target with source files listed in SOURCE_FILES variable :
```txt
add_executable(Executable main.cc)
```
or it can be in folder so:
```txt
add_executable(Executable src/main.cc)
```

### Takes a target (library) and adds a dependency if a target is given.
```txt
target_link_libraries(Executable PUBLIC Library)
```

## CMakeLists.txt in children folder
Move `add_library()` in children library folder, and `add_executable` in children folder where main function is present. For executable folder, in `CMakeLists.txt`, add `target_link_libraries()` too. In main `CMakeLists.txt`, add subdirectories:
```txt
add_subdirectory(src)
add_subdirectory(app)
```
List for specific target library where to find the header files where also use one of them.
```txt
target_include_directories(Library PUBLIC "./")
```

## Variables in CMake
Use `set()` for create variable, with key in first, and value after.
```txt
set(VAR_NAME name)
```
For using variable:
```txt
${VAR_NAME}
```
It can be used for set option and force it for compiler, like C++ version:
```txt
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
```
Disables the use of compiler-specific extensions.
```txt
set(CMAKE_CXX_EXTENSIONS OFF)
```

## Options in CMake
Option provides an option that the user can optionally select.
Example:
```txt
option(COMPILE_EXECUTABLE "Whether to compile executable" OFF)

if(COMPILE_EXECUTABLE)
	do_anything()
else()
	message("w/o exe.compiling")
endif()
```