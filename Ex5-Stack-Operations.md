# Ex5 Stack Operations
## DATE:28-02-25
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1.   Initialize top as -1 and declare stack as a character array.
2.	To push, increment top and assign the character to stack[top].
3.	To pop, check if top is -1 and return -1 if true.
4.	If not, return stack[top] and decrement top.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Varadaram SK
RegisterNumber:  212223040232
*/
#include<stdio.h>
#define MAX 20

char stack[100];
int top = -1;

int isEmpty()  
{  
    return top == -1;  
}

int isFull()  
{  
    return top == MAX - 1;  
}

char Peek()  
{  
    return stack[top];  
}

char pop()  
{  
    if (isEmpty())  
        return -1;  

    char ch = stack[top];  
    top--;  
    return(ch);  
}

void push(char oper)  
{  
    if (isFull())  
        printf("Stack Full!!!!");  
    else {  
        top++;  
        stack[top] = oper;  
    }  
}

```

## Output:
![image](https://github.com/user-attachments/assets/e24dc902-7d6c-4fed-8942-e7af82db97fd)



## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
