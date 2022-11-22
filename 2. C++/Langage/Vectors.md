**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #language 

# std::vector
## Definition
- A vector is a dynamic array of data.
- The continuity in memory of a vector will always be guaranteed, this guarantees a constant access time to an element.
- To access an element, the computer will look at the size of an element of the type contained in the vector, multiply by the index of the desired element, and add the start address of our vector, to finally find the address in memory of the desired element.
- If we want to add an element to our vector while the memory address after the current end of the vector is occupied, the vector will be moved in memory to a new available location.
- The capacity of a vector is greater than the size of a vector, and if the capacity of the vector is equal to the size of the vector, the operation of moving it in the memory is performed.

## Create a vector:
How to create a vector:
```cpp
# include <vector>

# create vector with default size
vector<int> v1;

# create vector with size 10 and default value with 2.
vector<int> v2(10, 2);

# array-like initialisation
vector<int> v3{10, 20, 30};
```
