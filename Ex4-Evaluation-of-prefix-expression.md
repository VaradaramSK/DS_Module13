# Ex4 Evaluation of prefix expression
## DATE: 26-02-25
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1.  Start
2.	Initialize an empty stack s with a variable top for tracking the stack index.
3.	Define a push() function to add an element to the stack.
4.	Define a pop() function to remove and return the top element from the stack.
5.	In evalprefix(), loop through the given prefix expression from right to left.
6.	For each character, if it’s an operator (+, *), pop two operands from the stack, perform the operation, and push the result.
7.	If it's a digit, convert it to an integer and push it onto the stack; finally, print the result after the loop ends.
8.	End

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: Varadaram SK
RegisterNumber:  212223040232
*/
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#define MAX 100  

void evalprefix(char* expr) {
    int stack[MAX]; 
    int top = -1;   

    int length = strlen(expr);

    
    for (int i = length - 1; i >= 0; i--) {
        char ch = expr[i];

        
        if (isdigit(ch)) {
            stack[++top] = ch - '0'; 
        }
        
        else if (ch == '*' || ch == '-') {
            int operand1 = stack[top--]; 
            int operand2 = stack[top--]; 

            int result = 0;
            if (ch == '*') {
                result = operand1 * operand2;  
            } else if (ch == '-') {
                result = operand1 - operand2;  
            }

            stack[++top] = result;
        }
    }

    
    int finalResult = stack[top];
    printf("%d\n", finalResult);
}
```

## Output:
![image](https://github.com/user-attachments/assets/0de011f0-86fb-4ef0-be7f-040df03c39a6)



## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
