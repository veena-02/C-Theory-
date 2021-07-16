## CONSTRUCTORS

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
