## Given an array of strings sorted in lexicographical order, print all of its permutations in strict lexicographical order. If two permutations look the same, only print one of them. See the 'note' below for an example.

Complete the function next_permutation which generates the permutations in the described order.

## For example, s=[ab,bc,cd]. The six permutations in correct order are:

ab bc cd
ab cd bc
bc ab cd
bc cd ab
cd ab bc
cd bc ab
Note: There may be two or more of the same string as elements of .
## For example, s=[ab,bc,cd]. Only one instance of a permutation where all elements match should be printed. In other words, if s[0]==s[1], then print either s[0]  or s[1] but not both.

A three element array having three distinct elements has six permutations as shown above. In this case, there are three matching pairs of permutations where ab and ba are switched. We only print the three visibly unique permutations:

ab ab bc
ab bc ab
bc ab ab
## Input Format

The first line of each test file contains a single integer , the length of the string array .

Each of the next  lines contains a string .

Constraints

 contains only lowercase English letters.
Output Format

Print each permutation as a list of space-separated strings on a single line.

## Sample Input 0

2
ab
cd
## Sample Output 0

ab cd
cd ab
## Sample Input 1

3
a
bc
bc
## Sample Output 1

a bc bc
bc a bc
bc bc a



## Program

```
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
void swap(char **a,char**b)
{
    char *temp=*a;
    *a=*b;
    *b=temp;
}
int compare(const void *a,const void *b)
{
    return strcmp(*(const char **)a,*(const char **)b);
    
}
int next_permutation(char **arr,int n)
{
    int i=n-2;
    while(i>=0 && strcmp(arr[i],arr[i+1])>=0)
    
        i--;
    if(i<0) return 0;
    int j=n-1;
    while(strcmp(arr[j],arr[i])<=0)
        j--;
    swap(&arr[i],&arr[j]);
    int start =i+1,end=n-1;
    while(start<end)
    {
        swap(&arr[start],&arr[end]);
        start++;
        end--;
        
    }
    return -1;
    
}
void print_array(char **arr,int n)
{
    for(int i=0;i<n;i++)
    {
        printf("%s",arr[i]);
        if(i!=n-1) printf(" ");
    }
    printf("\n");
}
int main()
{
    int n;
    scanf("%d",&n);
    char **arr=malloc(n*sizeof(char *));
    for(int i=0;i<n;i++)
    {
        arr[i]=malloc(100*sizeof(char));
        scanf("%s",arr[i]);
    }
    qsort(arr,n,sizeof(char *),compare);
    print_array(arr,n);
    while(next_permutation(arr,n))
    {
        print_array(arr,n);
    }
    for(int i=0;i<n;i++) free(arr[i]);
    free(arr);
    return 0;
    
}

```

## Output

<img width="297" height="253" alt="Screenshot 2026-03-19 191355" src="https://github.com/user-attachments/assets/dde2a44c-6289-4708-a452-84aaaad85ec2" />
