# EX 39 C program to find sum of digits.
## DATE:
## AIM:
To write a C program to find sum of digits.

## Algorithm

1.Declare integer variables n and sum, and initialize sum to 0.

2.Read the number n from the user.

3.Use a loop to repeat until n becomes 0.

4.In each iteration, extract the last digit using n % 10 and add it to sum, then remove the last digit using n = n / 10.

5.After the loop ends, display the value of sum. 

## Program:
```
#include<stdio.h>
int main()
{
    int n,sum=0;
    scanf("%d",&n);
    while(n!=0)
    {
        sum=sum+n%10;
        n=n/10;
    }
    printf("%d",sum);
    return 0;
}
```

## Output:

<img width="273" height="195" alt="Screenshot 2026-03-19 191103" src="https://github.com/user-attachments/assets/56949fac-1c2c-4ffd-ac16-155045b6914d" />


## Result:
Thus the program was executed and the output was verified successfully.
