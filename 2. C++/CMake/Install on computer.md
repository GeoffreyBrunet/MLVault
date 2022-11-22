**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# Use with CMake
Cmake use default path for installation of our operating system.
- Add lines for create binary / library in this default path:
```cmake
install(TARGETS ${EXECUTABLE_NAME}
	EXPORT ${LIBRARY_NAME}
	ARCHIVE DESTINATION lib
	LIBRARY DESTINATION lib
	RUNTIME DESTINATION bin)
	
install(TARGETS ${LIBRARY_NAME}
	ARCHIVE DESTINATION lib
	LIBRARY DESTINATION lib)
```
- And run CMake build command with **sudo** for having rights to write on folders.

>Binary is create in `/usr/local/bin` by default on Linux and macOS.
  Library is create in `/usr/local/lib` by default on Linux and macOS.