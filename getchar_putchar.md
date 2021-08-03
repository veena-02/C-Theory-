Formatted input-output functions are scanf() and printf() and unformatted functions are getchar(), putchar(), gets(), puts(), etc.

### What is the getchar in c?
This is the input function in c programming. We can read only a single character using this getchar function from the console. See the following syntax.

Also Read: Reverse a Number in C

char getchar();
From the above syntax, the return type of getchar function is char. That means, it can read only character value. For example, ch=getchar(); will read a single character from a console and store that character in the character variable ch.
### What is putchar in c language?
This is output function in c programming which display a single character to the console. It has the following syntax.
```
int putchar(char);
```
from the above syntax, you can see that return type of putchar function is int.
That means it returns the ASCII value of the variable char that we are displaying on the console. 
For example, suppose, we have a integer variable i and the statement i=putchar(‘a’); will display the character ‘a’ to the console and the value of i will be 97. 
The ASCII value of ‘a’ is 97.

Parameters: This method accepts a mandatory parameter char which is the character to be written to stdout.

Return Value: This function returns the character written on the stdout as an unsigned char. It also returns EOF when some error occurs.

###C Program to Read and Write a Single Character
In this program, we are just reading a single character and displaying the same character on the console.

```
#include <stdio.h>
#include <stdlib.h>
main( )
{
 char ch;
 printf("Enter a character: ");
 ch=getchar();
 printf("You have entered a character: ");
 putchar(ch);
 return 0;
}
```
Output

```
Enter a character: C
You have entered a character: C
```
