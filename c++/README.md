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

