**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# About
FetchContent can be used in [[CMakeLists.txt]] for download and use third party dependencies.
1.  **Declaring** the content to fetch with `FetchContent_Declare`. This can be a tarball (local or remote), a local folder, or a version control repository (Git, SVN, etc.).
2.  **Populating** the content with `FetchContent_MakeAvailable`. This commands _adds_ the targets declared in the external content to your build system.
```txt
include(FetchContent)

FetchContent_Declare(
	fmt
	GIT_REPOSITORY https://github.com/fmtlib/fmt
	GIT_TAG 8.1.1
)
FetchContent_MakeAvailable(fmt)
```

> Documentation can be found [here](https://cmake.org/cmake/help/latest/module/FetchContent.html).

