# C++
***

### Tips
---

### Resources
---
Tutorials  
[Tech with Tim](https://www.youtube.com/playlist?list=PLzMcBGfZo4-lmGC8VW0iu6qfMHjy7gLQ3) - 4  
[Caleb Curry - All-in-One](https://www.youtube.com/playlist?list=PL_c9BZzLwBRJ55lLw8PdPlTVblIlPKfX5)
[Caleb Curry - Intermediate](https://www.youtube.com/playlist?list=PL_c9BZzLwBRJkVDaJbLHrrjNH_phcbCy7)

### Include
---
Include libraries  
```C++
#include <iostream>
```

### Using Namespace
---
Include the namespace into current scope
```C++
using namespace std;
```
Cannot have same variable within same namespace

### std::cout
---
std::cout - characters output  
<< - stream insertion  
std::endl - \n
```C++
std::cout << "Hello World!" << std::endl;
```
std::cin - characters input  
\>\> - stream extraction  
```C++
str input;
std::cin >> input;
```

### Data Type
---
int  
float  
bool  
string (double quotes, need to include <string> library)  
char (single quotes)  
  
### Comment
---
single line comment
```C++
// Single comment
```
Multi line comment
```C++
/*
  Multiline comment
*/
```

### Constant
---
Memory location where value never changes
```C++
const int gravity = -9.8;
```
Value must be initialized

### Operator & Operands
---
Operator - mathmatical or logical symbols + - / * % ++ -- += -= /= *= %=  
Operands - expressions or values an operator operates  

### Array
---
Array has static size
```C++
  int x [5]; // Declare an array with size 5
  int y [5] = {1, 2, 3, 4, 5}; // Declare an array with size 5 and values
  int yy [] = {1, 2, 3, 4, 5}; // C++ will automatically set size to the number of values
  int yyy [] {1, 2, 3, 4, 5}; // Same as above
```
If you print an array, it will print memory location of the array not the values  
If you access an element that has not been set, it will return whatever is stored (random) at that memory location  
```C++
  int x [5] = {5} // Declare an array with size 5 and value 5 to the first element and 0 to rest of the elements
  
  sizeof(x) // Get the size of the array
```
