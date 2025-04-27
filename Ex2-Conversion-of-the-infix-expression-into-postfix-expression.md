# Ex2 Conversion of the infix expression into postfix expression
## DATE: 26-04-25
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1. Start the program.  
2. Include the required libraries.  
3. Define a function to return the priority of a given operator.  
4. Initialize the postfix expression.  
5. Loop through each character of the expression.  
6. If the character is an operator, find its priority using the function.  
7. Print the operator along with its corresponding priority level (Highest, Second Highest, etc.).  
8. End the program.

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by: Varadaram SK
RegisterNumber: 212223040232  
*/

#include <limits.h>
#include <stdio.h>
#include <stdlib.h>
#define MAX 20

char stk[20];

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
    return stk[top];  
}

char Pop()  
{  
    if (isEmpty())  
        return -1;  

    char ch = stk[top];  
    top--;  
    return(ch);  
}

void Push(char oper)  
{  
    if (isFull())  
        printf("Stack Full!!!!");  
    else {  
        top++;  
        stk[top] = oper;  
    }  
}

int checkIfOperand(char ch)   
{   
    return (ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z') || (ch >= '0' && ch <= '9');   
}   

int precedence(char ch)   
{   
    switch (ch)   
    {   
    case '+':   
    case '-':   
        return 1;   
  
    case '*':   
    case '/':   
    case '%': 
        return 2;   
  
    case '^':   
        return 3;   
    case '&':  
        return 4;   
    }   
    return -1;   
}

void IntoPost(char* expression)   
{   
    int i, j = 0;
    char postfix[MAX];

    for (i = 0; expression[i]; ++i)   
    {   
        if (checkIfOperand(expression[i]))   
            postfix[j++] = expression[i];   
  
        else if (expression[i] == '(')   
            Push(expression[i]);   
  
        else if (expression[i] == ')')   
        {   
            while (!isEmpty() && Peek() != '(')   
                postfix[j++] = Pop();   
            if (!isEmpty() && Peek() != '(')   
                return; 
            else  
                Pop();   
        }  
        else   
        {   
            while (!isEmpty() && precedence(expression[i]) <= precedence(Peek()))   
                postfix[j++] = Pop();   
            Push(expression[i]);   
        }   
    }   
  
    while (!isEmpty())   
        postfix[j++] = Pop();   
  
    postfix[j] = '\0';  

    
    for (i = 0; postfix[i] != '\0'; i++) {
        printf("%c", postfix[i]);
    }
    printf("\n");
}

```
## Output:

![image](https://github.com/user-attachments/assets/93cb3e73-9a2b-4ce0-9f2e-e1694caff31f)


## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
