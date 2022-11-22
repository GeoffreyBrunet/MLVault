**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# About
Catch2 is a modern, C++-native, test framework for unit-tests, TDD and BDD.

# Using
1. For using Catch2 in CPP project, create **tests** folder at root, contaning it's own [[CMakeLists.txt]] file, and all tests.
2. In root [[CMakeLists.txt]], add:
```cmake
add_subdirectory(tests)

option(ENABLE_TESTING "Wether to enable the unit testing build" ON)
```
3. In [[CMakeLists.txt]] file in **tests** folder, add:
```cmake
if (ENABLE_TESTING)
	set(TEST_MAIN "unit_tests")
	set(TEST_SOURCES
		"main.cc")
	add_executable(${TEST_MAIN}, ${TEST_SOURCES})
	target_link_librairies(${TEST_MAIN} PUBLIC
		${MIBRARY_NAME}
		${CONAN_CATCH2})
endif()
```
4. Include library in cpp test, for using it:
```cpp
# include <catch2/catch.hpp>
```
