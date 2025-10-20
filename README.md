# MODULE-3
Module 3 repository
---

1.### Program: Calculate Age using Function (With Return Type and With Arguments)

**Aim:**  
To calculate the current age of a person using a function with return type and arguments.

**Algorithm:**  
1. Start the program.  
2. Define a function `cage(int num1, int num2)` that calculates the difference between the current year and the birth year.  
3. In the main function, initialize two integer variables:  
   - `num1` as the current year (2020).  
   - `num2` as the birth year (1983).  
4. Call the function `cage(num1, num2)` to compute the difference.  
5. Subtract 1 from the result to adjust the age according to the birth date.  
6. Print the calculated age.  
7. End the program.  

**Source Code:**  
```c
#include <stdio.h>

int cage(int num1, int num2)
{
    int age = num1 - num2;
    return age;
}

int main()
{
    int num1 = 2020, num2 = 1983;
    int age = cage(num1, num2);
    printf("Present Age is : %d", age - 1);
    return 0;
}
```
**output**
<img width="522" height="172" alt="image" src="https://github.com/user-attachments/assets/6af5eb8c-7173-4980-9815-a1c4202d086e" />

**Result:**
The program calculates and displays the current age of a person based on the given date of birth and current date.


---

2.### Program: Check Whether a Number is an Armstrong Number or Not

**Aim:**  
To check whether the entered number is an Armstrong number using loops and mathematical operations.

**Algorithm:**  
1. Start the program.  
2. Declare variables: `num`, `sum`, `count`, `original`, and `temp`.  
3. Read the integer number `num` from the user.  
4. Store the value of `num` in `original` to preserve the original number.  
5. Count the number of digits in `num` by dividing it repeatedly by 10.  
6. Reassign `temp = num`.  
7. Extract each digit of `temp` using modulus (`% 10`) and compute its power raised to the total digit count using `pow()`.  
8. Add each powered digit to `sum`.  
9. After the loop, compare `sum` with `original`:  
   - If both are equal → it is an Armstrong number.  
   - Otherwise → it is not an Armstrong number.  
10. Display the result.  
11. End the program.  

**Source Code:**  
```c
#include <stdio.h>
#include <math.h>

int main()
{
    int num, sum = 0, count = 0;
    int original, temp;

    scanf("%d", &num);
    original = num;

    for (temp = num; temp != 0; ++count)
    {
        temp = temp / 10;
    }

    for (temp = num; temp != 0; temp /= 10)
    {
        int digit = temp % 10;
        sum += pow(digit, count);
    }

    if ((int)sum == original)
    {
        printf("%d is armstrong number", original);
    }
    else
    {
        printf("%d is not a armstrong number", original);
    }

    return 0;
}
```
**output**
<img width="765" height="167" alt="image" src="https://github.com/user-attachments/assets/f57fb6d5-0fa0-4edd-bb3e-57219a162c97" />

**Result:**
The program determines whether the entered number is an Armstrong number and displays the corresponding message.

---

3.### Program: Print the Elements of the Last Column of an n × n Matrix

**Aim:**  
To read the elements of an `n × n` matrix and print the elements of its last column.

**Algorithm:**  
1. Start the program.  
2. Declare a two-dimensional array `a[n][n]`.  
3. Read the value of `n` (the size of the matrix).  
4. Use nested `for` loops to input all elements of the matrix.  
5. After reading the matrix, use a single `for` loop to access the last column elements.  
6. Print each element of the last column along with its position.  
7. End the program.  

**Source Code:**  
```c
#include <stdio.h>

int main()
{
    int n;
    scanf("%d", &n);
    int a[n][n];

    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            scanf("%d", &a[i][j]);
        }
    }

    for (int i = 0; i < n; i++)
    {
        printf("a[%d][%d] is %d\n", i, n - 1, a[i][n - 1]);
    }

    return 0;
}
```
**output**
<img width="731" height="310" alt="image" src="https://github.com/user-attachments/assets/73f99ec3-7945-45ee-aed1-307c579c33ce" />

**Result:**
The program successfully prints all the elements of the last column of the entered square matrix.
---

4.### Program: Sort Elements of an Array in Ascending Order

**Aim:**  
To write a C program that reads elements into an array and sorts them in ascending order using the Bubble Sort algorithm.

**Algorithm:**  
1. Start the program.  
2. Declare an integer array `arr[n]` and variables for loops and swapping.  
3. Read the size of the array `n`.  
4. Input `n` elements into the array.  
5. Use **Bubble Sort** technique:
   - Repeat the process `n-1` times.
   - Compare each pair of adjacent elements.
   - Swap them if they are in the wrong order.  
6. Print the sorted array elements.  
7. End the program.  

**Source Code:**  
```c
#include <stdio.h>

int main()
{
    int n;
    scanf("%d", &n);
    int arr[n];
    int i, j, temp;

    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }

    for (i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```
**output**
<img width="743" height="117" alt="image" src="https://github.com/user-attachments/assets/8aec992d-5091-43ab-aa6e-2757d25496cd" />

**Result:**
The program sorts the entered array elements in ascending order and displays the sorted array.
---

5.### Program: Count Even and Odd Numbers in an Array

**Aim:**  
To write a C program that reads an array of integers and counts the number of even and odd elements using loops.

**Algorithm:**  
1. Start the program.  
2. Declare variables for array size `n`, counter variables `count` (for even) and `acount` (for odd).  
3. Input the size of the array `n`.  
4. Read `n` integers into the array `arr`.  
5. Use a loop to traverse each element:  
   - If the element is divisible by 2, increment the even counter.  
   - Otherwise, increment the odd counter.  
6. Display the count of even and odd numbers.  
7. End the program.  

**Source Code:**  
```c
#include <stdio.h>

int main()
{
    int n, i, count = 0, acount = 0; // initialize acount = 0 to avoid garbage value
    scanf("%d", &n);

    int arr[n];

    for (i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }

    for (i = 0; i < n; i++)
    {
        if (arr[i] % 2 == 0)
        {
            count++;
        }
        else
        {
            acount++;
        }
    }

    printf("Even numbers: %d\n", count);
    printf("Odd numbers: %d\n", acount);
    return 0;
}
```
**output**
<img width="586" height="138" alt="image" src="https://github.com/user-attachments/assets/b2954207-3da5-44fd-beee-1dba311649bd" />

**Result:**
The program counts and displays the total number of even and odd elements in the entered array.
---
