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
const int gravity = -9.8; // Can be deferred until run time
constexpr int gravity = -9.8 // Initialized at compile time. Can be used on class and function
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
int x [5]; // Declare an empty array with size 5
int x [5] = {1, 2, 3, 4, 5}; // Declare an array with size 5 and values
int x [] = {1, 2, 3, 4, 5}; // C++ will automatically set size to the number of values
int x [] {1, 2, 3, 4, 5}; // Same as above

// If you access an element that has not been initialized, it will return whatever is stored (random) at that memory location  
int x [5] = {2} // Declare an array with size 5 and value 2 to the first element and 0 to rest of the elements

x.begin (); / x.end ();
x.rebegin (); / x.rend ();
x.size ();
x.max_size ();
x.empty ();
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
```C++
#include <string>

char str[] = "HELLO WORLD";
// Preferred, managed type
string str = "HELLO WORLD"; // double quotes
str [1] = 'e'; // single quote

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

### Pair
---
```C++
pair<int, int> g1 = {1, 2};
g1 = make_pair (1, 2);
g1.first = 100;

g1.first;
g1.second;
```

### Tuple
---
Tuple can hold multiple data types
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

### Map
---
```C++
map <char, int> mp = {
  {'S', 1},
  {'h', 2}
  };
  
mp ['h']; // returns value 2
mp ['x']; // returns 0 not error

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

mp.insert (pair<char, int>('a', 3)); // insert
mp.erase ('a'); // erase
mp.clear (); // empty the map
mp.empty (); // check if empty
mp.size (); // size of map
```

### Vector
---
Vector has dynamic size
```C++
#include <vector>

vector <int> v1 = {1, 2, 3};

v1.sort (v1.begin(), v1.end());
v1.max_element (v1.being, v1.end());
v1.begin (); // iterator pointing at 0
v1.end (); // value at end
v1.front (); // value of the first element
v1.back (); // value of the last element
v1.last (); // iterator pointing at the last
v1.size ();
v1.push_back ();
v1.pop_back ();
v1.insert (pointer to the index, value); // ex. pointer = v1.begin()
v1.erase (pointer to the index); // ex. pointer = v1.beging() + 1


v1.capacity (); // current size which is not the number of elements
v1.shrink_to_fit (); // shink size to match the max of current elements vs min capacity
```

### Set
---
```C++
#include <set>

set <char> s1 = {'C', 'D'};

if (s1.find ('C') != s1.end()) {
  cout << "Not Found C";
} else {
  cout << "Found C" << endl;
}

s1.insert ('B');
s1.erase ('C');
```

### Lambda
---
[capture caluse](parameters){body}
```
[](int x){return x + 1}(5); // inline lambda execution notice ()

auto lam = [](int x){std::cout << "Hi and " << x << std::endl;};

function<void(int)> lam = [](int x){std::cout << "Hi and " << x << std::endl;};

lam(1);
```
