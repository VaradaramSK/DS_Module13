# EX 1 Display operator precedence in the infix expression.
## DATE: 26-04-25
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

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
Program to find and display the priority of the operator in the given Postfix expression
Developed by: 
RegisterNumber:  212223040232
*/
#include <stdio.h>
#include <ctype.h>


char* fun(char x) {
    switch (x) {
        case '+':
        case '-':
            return "Second Lowest Priority";  
        case '*':
        case '/':
            return "Second Highest Priority"; 
        case '%':
            return "Second Highest Priority";  
        case '&':
            return "Second Lowest Priority";  
        case '|':
            return "Lowest Priority";  
        case '^':
            return "Highest Priority";  
        default:
            return "Invalid Operator";  
    }
}

int main() {
    char exp[] = "100 200 + 2 / 5 * 7 |";
    int i = 0;

    
    while (exp[i] != '\0') {
        if (isspace(exp[i])) { 
            i++;
            continue;
        }
        
        if (!isdigit(exp[i])) {  
            printf("%c  ----> %s\n", exp[i], fun(exp[i]));
        }
        i++;
    }

    return 0;
}

```


## Output:
![image](https://github.com/user-attachments/assets/1aee6f85-6a45-48b9-a756-d003db88d780)



## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
