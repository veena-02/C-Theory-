## Stringize and Token-pasting operator in C

- The Stringize operator is a preprocessor operator. 
- It sends commands to compiler to convert a token into string. We use this operator at the macro definition.
- Using stringize operator we can convert some text into string without using any quotes.

Example Code
```
#include<stdio.h>
#define STR_PRINT(x) #x
main() {
   printf(STR_PRINT(This is a string without double quotes));
}
```
Output
This is a string without double quotes

### The Token Pasting operator is a preprocessor operator. It sends commands to compiler to add or concatenate two tokens into one string. We use this operator at the macro definition.

Example Code
```
#include<stdio.h>
#define STR_CONCAT(x, y) x##y
main() {
   printf("%d", STR_CONCAT(20, 50));
}
```
Output
2050
