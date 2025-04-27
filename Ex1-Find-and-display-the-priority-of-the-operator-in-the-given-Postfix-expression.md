# EX 1 Display operator precedence in the infix expression.
## DATE:
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. 
2. 
3. 
4.  
5.   

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
