

## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## NAME:PANGA THANUJA
## REG NO:212224040231
## Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
struct Node   
{  
    char data[100];  
    struct Node *next;  
}*head;  
void display()  
{
    struct Node *current=head;
    while(current!=NULL)
    {
        printf("%s\n",current->data);
        current=current->next;
    }
}
```
Output:


![Screenshot 2025-04-27 175519](https://github.com/user-attachments/assets/8a9f2f65-34c4-4e97-abb0-7a64a7232aa6)


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
struct Node   
{  
    float data;  
    struct Node *next;  
}*head;  
void pop()  
{  
    struct Node *ptr=head;  
    if(head==NULL)  
    {  
        printf("stack is empty");  
    }  
    else  
    {  
        head=head->next;
        free(ptr);
        ptr=NULL;
    }  
}
```
Output:

![Screenshot 2025-04-27 175610](https://github.com/user-attachments/assets/d37a921e-a9a9-4987-be17-a783600a3a33)




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *current=front;
    if(front==NULL)
    {
        printf("queue is empty");
        return;
    }
    else
    {
        printf("Queue elements:\n");  
        while(current!=NULL)
        {
            printf("%.3f\n",current->data);
            current=current->next;
        }
    }
}
```
Output:

![Screenshot 2025-04-27 175704](https://github.com/user-attachments/assets/e380f4c6-ea26-4e4c-a8b2-46d6bbb4f611)


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *current=malloc(sizeof(struct Node));
    current->data=data;
    current->next=NULL;
    if(front==NULL)
    {
        front=rear=current;
    }
    else
    {
        rear->next=current;
        rear=current;
    }
}
```
Output:

![Screenshot 2025-04-27 175757](https://github.com/user-attachments/assets/a4186a2f-8c27-4164-a924-09480ec1af28)


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
struct Node   
{  
    float data;  
    struct Node *next;  
}*head;
void peek()
{
    struct Node *current=head;
    printf("%.2f",current->data);
}
```
Output:

![Screenshot 2025-04-27 175851](https://github.com/user-attachments/assets/cbf9c5aa-528a-466d-9278-abb2010a42f0)




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


