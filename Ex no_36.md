# # #Task - Hackerrank Problem

This challenge requires you to print Hello Saveetha! on a single line, and then print the already provided input string to stdout. If you are not familiar with C, you may want to read about the printf() command.

# # Example:

Saveetha

The required output is: Hello, Saveetha! C Programming

## Program

```
#include<stdio.h>
#include<string.h>
int main()
{
    char s[100];
    scanf("%[^\n]s",s);
    printf("Hello, Saveetha!\n");
    printf("%s",s);
}

```

## Output

<img width="497" height="203" alt="Screenshot 2026-03-19 190342" src="https://github.com/user-attachments/assets/69bd1969-dddb-4f40-81ec-6896ff07ddcf" />
