**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# About
Doxygen is the de facto standard tool for generating documentation from annotated C++ sources

# Using
1. Doxygen use docstrings for create documentation, so need to add it on top of our classes / functions:
```cpp
/**
 * @brief function descr.
 *
 * @param Example param
 *
 * @return description of the return value
 */
void my_function() {
	do_something()
}
```
2. Create at root a folder called **docs**, and a file called **doxyfile**. Template for this file can be found [here](https://github.com/ibab/cpp-template/blob/master/docs/Doxyfile.in).
3. For generate documentation, run in docs folder the command:
```shell
doxygen
```
4. Create in **docs** folder a new file called **Docs.cmake** with following content:
```cmake
find_package(Doxygen)

if(DOXYGEN_FOUND)
	configure_file(
		${CMAKE_CURRENT_SOURCE_DIR}/docs/Doxyfile
		${CMAKE_CURRENT_BINARY_DIR}/Doxyfile @ONLY)
	add_custom_target(docs
		${DOXYGEN_EXECUTABLE} ${CMAKE_CURRENT_BINARY_DIR}/Doxyfile
		WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/docs)
endif()
```
This file find `doxygen` file and execute custom target.
5. For build documentation when building project, and in [[CMakeLists.txt]] root file following line:
```cmake
include(Docs)
```
