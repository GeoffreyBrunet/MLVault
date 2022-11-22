**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cmake 

# Public & Private
In CMake, **public** and **private** are visibility scope, like in OOP. For this example, we have 3 different librairies, A, B and C.
```cmake
# can use everything defined in B in A:
target_link_libraries(A PUBLIC B)
# can use everything defined in A and B (with inheritance) in C:
target_link_libraries(C PUBLIC A)

# In A, we can use everything in B
target_link_libraries(A PRIVATE B)
# In C, we can use everything in A, but not in B (no inheritance):
target_link_libraries(C PRIVATE A)
```

# Interface
**Interface** is used to combine several librairies into one common librairy, just for header files. It's not often used. Example for using it here:
```cmake
add_library(D INTERFACE)
target_include_directories(D INTERFACE {CMAKE_CURRENT_SOURCE_DIR}/include)
```
