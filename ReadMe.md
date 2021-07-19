
<a id="a2">## [Different ways to use Const with Reference to a Pointer in C++](https://www.geeksforgeeks.org/different-ways-to-use-const-with-reference-to-a-pointer-in-c/) </a>

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
