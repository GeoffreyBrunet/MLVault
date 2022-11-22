**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

> Works only on linux, can be computed by Github.

# Generate Code Coverage
1. Add options in root [[CMakeLists.txt]] file
```cmake
# OFF by default because don't work on all OS:
option(ENABLE COVERAGE "Enable a code coverage build" OFF)

# set flags for compilers
if(ENABLE_COVERAGE)
	include(CodeCoverage)
	append_coverage_compiler_flags()
endif()
```
2. In CMake folder, create a `CodeCoverage.cmake` file, a lot of templates can be found on web (like [here](https://github.com/franneck94/UdemyCmake/blob/master/2_CMake/12_Final/cmake/CodeCoverage.cmake).)
3. In **CMakeLists.txt** in **tests folder**, `if` statement is added for run coverage main executable, and create coverage report:
```cmake
if (ENABLE_COVERAGE)
	set(COVERAGE_MAIN "coverage")
	set(COVERAGE_EXCLUDES
		"${PROJECT_SOURCE_DIR}/app/*"
		"${PROJECT_SOURCE_DIR}/cmake/*"
		"${PROJECT_SOURCE_DIR}/docs/*"
		"${PROJECT_SOURCE_DIR}/external/*"
		"${PROJECT_SOURCE_DIR}/tests/*"
		"${CONAN_CATCH2_ROOT}/*"
		"${CONAN_CXXOPTS_ROOT}/*"
		"/usr/include/*")
	setup_target_for_coverage_lcov(
		NAME ${COVERAGE_MAIN}
		EXECUTABLE ${TEST_MAIN}
		DEPENDENCIES ${TEST_MAIN}
	)
endif()
```
4. Run command with flag for enable coverage:
```shell
cmake -DENABLE_COVERAGE .
```
5. Show coverage in `index.html` file, located in `build/coverage/`.
