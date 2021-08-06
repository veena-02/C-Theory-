### Accepting String containing multiple words

When we use scanf with the format specification %s to accept String as input, by default it will not accept String with multiple words.
For example, when we enter the input as "Good Morning" to the below program it will print only "Good" as output.
It will omit Morning as it is after a space.
#include <stdio.h>    

```
int main() {
    char greeting[50];
    scanf("%s",greeting);
    printf("%s",greeting);
    return 0;
}
```

Hence we must use fgets function to accept a single String with multiple words in it as shown in the program below.

```
#include <stdio.h>    

int main() {
    char greeting[50];
    fgets(greeting,50,stdin);
    printf("%s",greeting);
    return 0;
}
```
Instead of printf("%s",greeting); we can also use puts(greeting); as shown below.

<b><i> Note: By default, the puts function always prints a new line at the end.</i></b>
```
#include <stdio.h>    

int main() {
    char greeting[50];
    fgets(greeting,50,stdin);
    puts(greeting);
    return 0;
}
```
