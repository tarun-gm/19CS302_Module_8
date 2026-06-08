# # Hackerrank problem - 2

Your task is to take two numbers of int data type, two numbers of float data type as input and output their sum:

Declare 4 variables: two of type int and two of type float.

Read 2 lines of input from stdin (according to the sequence given in the 'Input Format' section below) and initialize your variables.

Use the + and - operator to perform the following operations:

Print the sum and difference of two int variable on a new line.

Print the sum and difference of two float variable rounded to one decimal place on a new line.

## Input Format

The first line contains two integers.

The second line contains two floating point numbers.

## Constraints 

1 ≤ integer variables ≤ 104

1 ≤ float variables ≤ 104

## Output Format

Print the sum and difference of both integers separated by a space on the first line, and the sum and difference of both float (scaled to 1 decimal place) separated by a space on the second line.

Sample Input 

10 4

4.0 2.0

Sample Output 

14 6

6.0 2.0

Explanation

When we sum the integers 10 and 4, we get the integer 14. When we subtract the second number 4 from the first number 10, we get 6 as their difference.

When we sum the floating-point numbers 4.0 and 2.0, we get 6.0. When we subtract the second number 2.0 from the first number 4.0, we get 2.0 as their difference.



## Program

```
#include <stdio.h>

int main()
{
    int a, b;
    float c, d;
    scanf("%d %d", &a, &b);
    scanf("%f %f", &c, &d);
    printf("%d %d\n", a + b, a - b);
    printf("%.1f %.1f", c + d, c - d);
    return 0;
}

```

## Output

<img width="352" height="198" alt="Screenshot 2026-03-19 191821" src="https://github.com/user-attachments/assets/4f7ad09a-2e1f-48f8-b507-25c1e039d018" />
