# C++
***

### Tips
---

### Resources
---
Tutorials  
[Tech with Tim](https://www.youtube.com/playlist?list=PLzMcBGfZo4-lmGC8VW0iu6qfMHjy7gLQ3) - 15  
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

### For Loop / While Loop
---
```C++
// for loop condition
for (init; condition; change (increment/decrement) {
}

// foreach loop
for (int x : int [3] = {1, 2, 3}) {
}

// while loop
init
while (condition) {
  change (increment/decrement)
}
```

### Switch
---
```C++
char x = 'x';
switch (x) {
  case 'a':
    std::cout << "a" << std::endl;
    break;
  case 'x':
    std::out << "x" << std::endl;
    break;
  default:
    std::out << "not found" << std::endl;
    break;
}
```
If break caluse does not exist for a case statement, the program will continue to check the next case(s)  

### String
---
String can be think of as an array with characters
```C++
#include <string>

char str[] = "HELLO WORLD";
// Preferred, managed type
string str = "HELLO WORLD"; // double quotes
str [1] = 'e'; // single quote
```
Useful features
```C++
str.length ();
str.size ();
```

### &Reference
---
& references to a memory location
```C++
int a = 5;
int& b = a;

b = 1; // a becomes 1
```
You must initialize a reference variable with a variable

### *Pointer
---
\* points to a memory location (pointer variable has its <b>own memory location</b> and it points to memory location)
```C++
int a = 5;
int* b = &a;

*b = 1; // a becomes 1
```
You must deference a pointer variable to set new value as it must know the memeory location it is changing to
```C++
int a[] = {1, 2, 3};
int head = a;

for (int i = 0; i < 3; ++i) {
  head = a + i // from memory location of the first element of a, add i to get memory location of ith element
  cout << *head << endl;
}
```
Elements within the same array will have memory address of + 1 from previous

### Tuple
---
```C++
include <tuple>

tuple <string, int> person1 ("Shawn", 30);
tuple <string, int> person2 = make_tuple ("Shawn2", 30);
int index = 0;

get<index>person1 // get or assign value on index

person1.sawp (person2) // sawp two tuples

string name;
int age;
tie (name, age) = person1; // break down into individual elements
tuple <string, int, string, int> people = tuple_cat (person1, person2); // concatenate tuples
```

### Maps
---
```C++
map <char, int> mp = {
  {'S', 1},
  {'h', 2}
  };
  
mp ['h']; // 2
mp ['x']; // 0 not error

mp.insert (pair<char, int>('a', 3)); // insert
mp.erase ('a'); // erase
mp.clear (); // empty the map
mp.empty (); // check if empty
mp.size (); // size of map

for (map<char,int>::iterator itr = mp.begin (); itr != mp.end (); ++itr) {
  *itr.first; // key
  itr->first; // -> is equivalent to deferencing the variable 
  *itr.second; // value
  itr->second;
  
  if (mp.find ('w') == mp.end()) { // check if w is in the map, if not exist, initialize it
    mp ['w'] = 0;
  }
  
  mp ['w']++;
}
```
