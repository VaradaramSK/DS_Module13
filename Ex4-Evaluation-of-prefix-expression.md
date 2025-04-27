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
Start the program.
Check if n is greater than 0.
Recursively move n-1 disks from source (x) to auxiliary (z) using destination (y).
Print the move of the n-th disk from source (x) to destination (y).
Recursively move n-1 disks from auxiliary (z) to destination (y) using source (x).
The function is called initially with TOH(n, 'A', 'B', 'C') where 'A', 'B', and 'C' are the rods.
End
```

## Output:
![image](https://github.com/user-attachments/assets/0de011f0-86fb-4ef0-be7f-040df03c39a6)



## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
