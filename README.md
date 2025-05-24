## EX-21-POINTERS
# AIM:
Write a C program to convert a 15.50 into 15 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (15.50).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 15.
4.	Print the modified value.

## PROGRAM:
```
#include <stdio.h>

int main() {
    float num ;
    scanf("%f",&num);
    int *ptr;
    int val = (int)num;  // convert float to int
    ptr = &val;          // point to the integer

    printf("the integer equivalent of %.2f =%d\n", num, *ptr);
    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/a0b54dde-6bde-4182-b6bd-344ff6fba259)

## RESULT:
Thus the program to convert a 15.50 into 15 using pointer has been executed successfully.
 
 
# EX-22-FUNCTIONS AND STORAGE CLASS
## AIM:
Write a C program to calculate the Product of first 12 natural numbers using Recursion
## ALGORITHM:
1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
#include <stdio.h>

unsigned long long factorial(int n) {
    if (n == 1)
        return 1;
    else
        return n * factorial(n - 1);
}

int main() {
    int num = 12;
    unsigned long long result = factorial(num);

    printf("Product is = %llu\n", result);
    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/9379af4e-89b0-4ffd-b489-f0519424b10f)

## RESULT:
Thus the program has been executed successfully.
 
 
## EX-23-ARRAYS AND ITS OPERATIONS
## AIM:
Write C Program to find Minimum element of each row of a Matrix

## ALGORITHM:
1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the minimum elements in each row.
4.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int m, n;
    scanf("%d %d", &m, &n);
    int mat[m][n];

    // Input matrix
    for (int i = 0; i < m; i++)
        for (int j = 0; j < n; j++)
            scanf("%d", &mat[i][j]);

    // Find and print minimum of each row
    for (int i = 0; i < m; i++) {
        int min = mat[i][0];
        for (int j = 1; j < n; j++) {
            if (mat[i][j] < min)
                min = mat[i][j];
        }
        printf("Minimum element of the row %d is: %d\n", i + 1, min);
    }
    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/4e1f30be-e607-4a2b-b0ae-16b6b7128e57)

## RESULT
Thus the program has been executed successfully.


# EX-24-STRINGS
## AIM:
Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:
1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows;
    fgets(str, sizeof(str), stdin);
    str[strcspn(str, "\n")] = '\0'; 
    scanf("%d", &rows);

    int len = strlen(str);
    int k = 0; 

    for (int i = 1; i <= rows+1; i++)
    {
        for (int j = 1; j <= rows - i+3; j++)
        {
            printf(" ");
        }
        for (int j = 0; j < i; j++) {
            printf("%c ", str[k % len]);
            k++;
        }

        printf("\n");
    }

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/2267da00-dbf3-4dce-91c0-a82c8ab811c0)

## RESULT
Thus the C program to String process executed successfully.
 

## EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM
Write a c program to read and display a string of an elements using pointer

## ALGORITHM
```
1. Declare a character array str[] 
2.Declare a character pointer ptr.
3.Point ptr to the base address of the string str (i.e., ptr = str).
4.Print the message: "The entered string is ::".
5.Repeat the following until the character pointed by ptr is the null character ('\0').
6.Print the character pointed by ptr.
7.Move the pointer to the next character (ptr++).
8.Print a newline character for formatting.
```

## PROGRAM
```
#include <stdio.h>
int main()
{
    char str[100];
    char *ptr;

    
    scanf("%s",str);

    //assign address of str to ptr
    ptr=str;

    printf("The entered string is :: ");

    while(*ptr!='\0')
        printf("%c",*ptr++);

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/168d7a56-9e98-4437-bf61-218f1f58abcf)

## RESULT
Thus the C program to read and display a string of an elements using pointer has been executed


