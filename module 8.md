## EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
## NAME:PANGA THANUJA
## REG NO:212224040231
## Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

```
#include<stdio.h>
int main() {
    int n;
    scanf("%d",&n);
    if(n>=71 && n<=79) {
        switch(n)
        {
            case 71:
            printf("seventy one");
            break;
            case 72:
            printf("seventy two");
            break;
            case 73:
            printf("seventy three");
            break;
            case 74:
            printf("seventy four");
            break;
            case 75:
            printf("seventy five");
            break;
            case 76:
            printf("seventy six");
            break;
            case 77:
            printf("seventy seven");
            break;
            case 78:
            printf("seventy eight");
            break;
            case 79:
            printf("seventy nine");
            break;
        }
    }
    else if(n>79){
        printf("Greater than 79");
    }
}
```



Output:



![Screenshot 2025-04-27 171235](https://github.com/user-attachments/assets/0e019172-0f1d-45e5-af58-23bf4c4f590d)







Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include<stdio.h>
void digit_frequency(const char *s)
{
    int freq[10]={0};
    for (int i=0;s[i]!='\0';i++)
    {
        if(s[i]>='0' && s[i]<='9')
        {
            freq[s[i]-'0']++;
        }
    }
        for(int i=0;i<10;i++)
        {
            printf("%d ",freq[i]);
        }
 printf("\n");
 }
 int main()
    {
        char s[100];
        scanf("%s",s);
        digit_frequency(s);
    }
```




Output:



![Screenshot 2025-04-27 171353](https://github.com/user-attachments/assets/fd3a16cf-f521-4c18-b5b9-64cc52a7fef5)







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
void swap(char **a,char**b)
{
    char *temp=*a;
    *a=*b;
    *b=temp;
}
void reverse(char*arr[],int start,int end)
{
    while(start<end){
        swap(&arr[start],&arr[end]);
        start++;
        end--;
    }
}
int next_permutation(char*arr[],int n){
    int i=n-2;
    while (i >= 0 && strcmp(arr[i],arr[i+1])>=0)i--;
    if(i<0)return 0;
    int j=n-1;
    while(strcmp(arr[i],arr[j])>=0)j--;
    swap(&arr[i],&arr[j]);
    reverse(arr,i+1,n-1);
    return 1;
}
int compare(const void *a,const void*b){
    return strcmp(*(const char **)a,*(const char **)b);
}
int main()
{
    int n;
    scanf("%d",&n);
    char *strings[n];
    for(int i=0;i<n;i++){
        strings[i]=malloc(101);
        scanf("%s",strings[i]);
    }
    qsort (strings,n,sizeof(char*),compare);
    do{
        for(int i=0;i<n;i++)printf("%s ",strings[i]);
        printf("\n");
    }while(next_permutation(strings,n));
    for(int i=0;i<n;i++)free(strings[i]);
    return 0;
}
```



Output:





![Screenshot 2025-04-27 171452](https://github.com/user-attachments/assets/365cee8e-e9be-445e-8fbe-1ce704ef330d)







Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include<stdio.h>
void pattern(int n)
{
    int size=2*n-1;
    for(int i=0;i<size;i++)
    {
        for(int j=0;j<size;j++)
        {
            int min=i<j?i:j;
            min=min<size-i?min:size-i-1;
            min=min<size-j?min:size-j-1;
            printf("%d ",n-min);
        }
        printf("\n");
    }
}
int main()
{
    int n;
    scanf("%d",&n);
    pattern(n);
}
```



Output:



![Screenshot 2025-04-27 171601](https://github.com/user-attachments/assets/86c82c7a-1d3c-48da-9378-a6786fd00a6d)







Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:
```
#include <stdio.h>
int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}
int main() {
    int result;
    result = square(); 
    printf("Square of the number is: %d\n", result);
    return 0;
}
```



Output:



![Screenshot 2025-04-27 171658](https://github.com/user-attachments/assets/dcfdb0bd-e284-44ec-be3c-9face43c3d14)







Result:
Thus, the program is verified successfully



























