

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
int max_of_four(int a, int b, int c, int d)
{
    if(a>b && a>c && a>d)
        return a;
    else if(b>a && b>c && b>d)
        return b;
    else if(c>a && c>b && c>d)
        return c;
    else
        return d;
}
int main()
{
    int a,b,c,d;
    scanf("%d\n%d\n%d\n%d",&a,&b,&c,&d);
    printf("%d",max_of_four(a,b,c,d));
}
```
Output:
![Screenshot 2025-04-27 174439](https://github.com/user-attachments/assets/66d9eca9-06b7-4698-890a-639e29cdacb8)


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include<stdio.h>
void calculate_the_maximum(int n,int k)
{
    int max_and=0,max_or=0,max_xor=0;
    for(int i=0;i<n;i++)
    {
        for(int j=i+1;j<=n;j++)
        {
            int and_result=i&j;
            int or_result=i|j;
            int xor_result=i^j;
            if(and_result<k && and_result>max_and)
                max_and=and_result;
            if(or_result<k && or_result>max_or)
                max_or=or_result;
            if(xor_result<k && xor_result>max_xor)
                max_xor=xor_result;
        }
    }
    printf("%d\n%d\n%d",max_and,max_or,max_xor);
}
int main()
{
    int n,k;
    scanf("%d %d",&n,&k);
    calculate_the_maximum(n,k);
}
```
Output:

![Screenshot 2025-04-27 174527](https://github.com/user-attachments/assets/64eec9a0-7397-4f42-913f-2d4e6f1e75fb)

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int n,q;
    scanf("%d %d",&n,&q);
    int** shelves=(int**)malloc(n*sizeof(int*));
    int* book_counts=(int*)calloc(n,sizeof(int));
    for(int i=0;i<n;i++)
    {
        shelves[i]=(int*)malloc(1100*sizeof(int*));
    }
    for(int i=0;i<q;i++)
    {
        int type;
        scanf("%d",&type);
        if(type==1)
        {
            int x,y;
            scanf("%d %d",&x,&y);
            shelves[x][book_counts[x]++]=y;
        }
        else if(type==2)
        {
            int x,y;
            scanf("%d %d",&x,&y);
            printf("%d\n",shelves[x][y]);
        }
        else if(type==3)
        {
            int x;
            scanf("%d",&x);
            printf("%d\n",book_counts[x]);
        }
    }
    for(int i=0;i<n;i++)
    {
        free(shelves[i]);
    }
    free(shelves);
    free(book_counts);
}
```
Output:
![Screenshot 2025-04-27 174621](https://github.com/user-attachments/assets/1bb52757-19d5-4412-b915-81d577ea125a)



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include<stdio.h>
int main()
{
    int a;
    scanf("%d",&a);
    int arr[a];
    int sum=0;
    for(int i=0;i<a;i++)
    {
        scanf("%d",&arr[i]);
        sum=sum+arr[i];
    }
    printf("%d",sum);
}
```
Output:
![Screenshot 2025-04-27 174708](https://github.com/user-attachments/assets/41dfd3fb-6996-4b19-a575-84163cc24b26)


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    scanf("%[^\n]s",str);
    int count=0;
    int n=strlen(str);
    for(int i=0;i<=n;i++)
    {
        if((str[i]==' ' || str[i]=='\n' || str[i]=='\t')&&(i>0 && str[i-1]!=' ' && str[i-1]!='\n' && str[i-1]!='\t'))
        {
            count++;
        }
    }
    if(n>0 && str[0]!=' ' && str[0]!='\n' && str[0]!='\t')
    {
        count++;
    }
    printf("Total number of words in the string is :%d",count);
}
```
Output:

![Screenshot 2025-04-27 174800](https://github.com/user-attachments/assets/04c34cde-6f7d-4350-b578-4544ede9a976)



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
