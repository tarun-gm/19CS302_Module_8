# # Task

# # Given a positive integer denoting , do the following:

# If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 41 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Input Format

The first line contains a single integer, .

## Constraints

## Output Format

If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 4 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Sample Input

41
## Sample Output

forty one


## Program

```

#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    if(n==71)
    printf("seventy one\n");
    else if(n==72)
    printf("seventy two\n");
    else if(n==73)
    printf("seventy three\n");
    else if(n==74)
    printf("seventy four\n");
    else if(n==75)
    printf("seventy five\n");
    else if(n==76)
    printf("seventy six\n");
    else if(n==77)
    printf("seventy seven\n");
    else if(n==78)
    printf("seventy eight\n");
    else if(n==79)
    printf("seventy nine\n");
    else 
    printf("Greater than 79\n");
}

```
## Output

<img width="408" height="194" alt="Screenshot 2026-03-19 190848" src="https://github.com/user-attachments/assets/904bcf28-79ad-4af4-abca-fd85422dd174" />
