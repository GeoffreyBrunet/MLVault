**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# About
[VCPKG](https://vcpkg.io/en/index.html) is another package manager created by Microsoft. It works on all OS. The difference with [[Conan]] is VCPKG pre-build librairies on our local machine.
On macOS it can be installed with Homebrew:
```shell
brew install vcpkg
```
For installing a library with CLI:
```shell
vcpkg install lib_name
```
File for dependencies can be found at `~/cpp/vcpkg/scripts/vcpkg.cmake`