# EX3 Implementation of Tower of Hanoi
## DATE:
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1.Start the program.
2.Check if n is greater than 0.
3.Recursively move n-1 disks from source (x) to auxiliary (z) using destination (y).
4.Print the move of the n-th disk from source (x) to destination (y).
5.Recursively move n-1 disks from auxiliary (z) to destination (y) using source (x).
6.The function is called initially with TOH(n, 'A', 'B', 'C') where 'A', 'B', and 'C' are the rods.
7.End

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by: 
RegisterNumber:  212223040232
*/
#include <stdio.h>

void towerOfHanoi(int n, char A, char B, char C)
{
	if (n == 1)
	{
		printf("%c to %c\n", A, B);
		return;
	}
	towerOfHanoi(n-1, A,C, B);
	printf("%c to %c\n",A, B);
	towerOfHanoi(n-1, C,B,A);
}

int main()
{
	int n = 3; 
	towerOfHanoi(n, 'A', 'B', 'C'); 
	return 0;
}

```

## Output:
![image](https://github.com/user-attachments/assets/b9e7deff-1e84-443f-ad69-4785fd343a8d)



## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
