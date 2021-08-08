[What is the difference between ASCII Chr(10) and Chr(13)](https://www.petefreitag.com/item/863.cfm#:~:text=The%20ASCII%20character%20code%2013,that%20compose%20a%20proper%20CRLF%20.)

### <b>Note</b>: tolower() or toupper() functions when applied to non alphabets return the same characters.
```
int main()
{
    char x='[';
    printf("%c",tolower(x));
    printf("\n%c",toupper(x));
    return 0;
}
```
OUTPUT:
```
[
[
```
