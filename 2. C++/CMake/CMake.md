**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake  

## What is it
CMake is a cross-platform, open-source build system generator.

## Command Line Tool
### Configure CMake
```shell
cmake .
# or
cmake -S <path_to_source> -B <path_to_build>
```
### Compile project

```shell
cmake build .
```
#### Compile project with library
```shell
cmake build . --target Library
```
#### Compile project with EXECUTABLE
```shell
cmake build . --target Executable
```

### Pass option in parameter
```shell
cmake -DCOMPILE_EXECUTABLE=ON
```