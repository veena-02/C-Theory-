INDEX:

1. [CONSTRUCTOR](#a1)
2. [REFERENCES](#a2)
3. [C structures VS C++ structures](#a3)
## <a id="a2"> [Different ways to use Const with Reference to a Pointer in C++](https://www.geeksforgeeks.org/different-ways-to-use-const-with-reference-to-a-pointer-in-c/) </a>

- Reference to a const pointer
- const reference to a pointer

<i><b>When a function returns by reference, it can be used as lvalue. Since x is a static variable, it is shared among function calls and the initialization line "static int x = 10;" is executed only once. The function call fun() = 30, modifies x to 30. The next call "cout << fun()" returns the modified value.</b></i>
CODE:
```
#include<iostream>
using namespace std;
 
int &fun()
{
    static int x = 10;
    return x;
}
int main()
{
    fun() = 30;
    cout << fun();
    return 0;
}
```
OUTPUT: 30

<a id="a1">## CONSTRUCTORS</a>

### Initializer List
Initializer list is used to initialize data members.The initializer list does not end in a semicolon.
Syntax: 
```
Constructorname(datatype value1, datatype value2):datamember(value1),datamember(value2)
{
    ...
}

Base(int value):value(value)
    {
        cout << "Value is " << value;
    }
```

Eg.
```
class Point {
private:
    int x;
    int y;
public:
    Point(int i = 0, int j = 0):x(i), y(j) {}

    /*  The above use of Initializer list is optional as the
        constructor can also be written as:
        Point(int i = 0, int j = 0) {
            x = i;
            y = j;
        }
    */
 };
```
### Uses of Initializer List in C++:
There are situations where initialization of data members inside constructor doesn't work and Initializer List must be used. Following are such cases:
<i><b>POINT TO NOTE</b></i>
- a const variable must be initialized while declaring it as const always has a fixed value
- while creating a reference variable, it the variable it is refered to must be given in the same line i.e. 
- "int &x;" and "const int y" would throw an error, correct way is "int &x=t;" and "const int y=5;"
- So if data member variables are either a const variable or a reference variable, they must be initialized immediately on being created(during object creation) 
- which is done by the INITIALIZER LIST 

1) For initialization of non-static const data members: 
2) For initialization of reference members: 
3) 3) For initialization of member objects which do not have default constructor

[Visit this for details](https://www.geeksforgeeks.org/when-do-we-use-initializer-list-in-c/)

## <a id="a3">C structures and C++ structures</a>

- In C++, struct and class are exactly the same things, except for that struct defaults to public visibility and class defaults to private visibility. 
- <i>Member functions inside structure</i>: Structures in C cannot have member functions inside structure but Structures in C++ can have member functions along with data members.
- Using struct keyword: In C, we need to use struct to declare a struct variable. In C++, struct is not necessary. For example, let there be a structure for Record. In C, we must use “struct Record” for Record variables. In C++, we need not use struct and using ‘Record‘ only would work.
- Static Members: C structures cannot have static members but is allowed in C++.
- Constructor creation in structure: Structures in C cannot have constructor inside structure but Structures in C++ can have Constructor creation.
- sizeof operator: This operator will generate 0 for an empty structure in C whereas 1 for an empty structure in C++. 
- sizeof operator: This operator will generate 0 for an empty structure in C whereas 1 for an empty structure in C++. 

### STRUCTURE IN CPP VS CLASS IN CPP:

1) Members of a class are private by default and members of a structure are public by default. 
2) When deriving a struct from a class/struct, the default access-specifier for a base class/struct is public. And when deriving a class, the default access specifier is private. 
For example program 3 fails in compilation and program 4 works fine. 
3) Class can have null values but the structure can not have null values.
4) Memory of structure is allocated in the stack while the memory of class is allocated in heap.
5) Class requires constructor and destructor but the structure can not require it.
6) Classes support polymorphism and also be inherited but the structure cannot be inherited.
