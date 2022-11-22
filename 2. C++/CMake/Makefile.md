**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# About
Makefile is file used for created commands with [make](https://en.wikipedia.org/wiki/Make_(software)).

# Run commands before build
First line in command used after `cmake` call in CLI. Following lines are executed when calling `prepare` option here.
```makefile
prepare:
	rm -rf build
	mkdir build
```
and run following command:
```shell
make prepare
```
