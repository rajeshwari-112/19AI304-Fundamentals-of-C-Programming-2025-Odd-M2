# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M2
# IAPR-2- Module 2 - FoC
3. Implementation of programs using conditional statements.
4. Implementation of programs using various control statements.
# Ex.No:6
  Build a C program to input a student’s marks in three subjects (Math, Science, and English). Calculate the average marks and determine the grade using nested if-else statements with safe floating-point comparisons based on the following grading criteria:
    
  A: 90 and above
  
  B: 75 to 89.99
  
  C: 50 to 74.99
  
  F: below 50
  
  The program should display the average marks up to two decimal places and the corresponding grade. 

## Aim:
 To build a C program that receives inputs for a student’s marks in three subjects, calculates the average, and determines the grade using nested if-else statements with safe floating-point comparisons.
## Algorithm:
Step 1: Start<br>
Step 2: Include the standard input-output library: #include<stdio.h>.<br>
Step 3: Declare float variables math, science, english to store marks of each subject.<br>
Step 4: Declare a float variable average to store the average marks.<br>
Step 5: Prompt the user to enter marks for Math, Science, and English.<br>
Step 6: Read the input marks.<br>
Step 7: Calculate the average marks using the formula:<br>
  average=(math + science + english​)/3.0f<br>
Step 8: Check if average is greater than or equal to 90.0f<br
  If yes, print Grade A.<br>
  Else, proceed to Step 9. <br> 
Step 9: Check if average is greater than or equal to 75.0f<br>
  If yes, print Grade B.<br>
  Else, proceed to Step 10.<br>
Step 10: Check if average is greater than or equal to 50.0f<br>
  If yes, print Grade C.<br>
  Else, print Grade F.<br>
Step 11: Stop<br>
## Program:
```
#include <stdio.h>

int main() {
    float math, science, english, average;
    printf("Enter marks for Math: ");
    scanf("%f", &math);

    printf("Enter marks for Science: ");
    scanf("%f", &science);

    printf("Enter marks for English: ");
    scanf("%f", &english);
    average = (math + science + english) / 3.0f;

    if (average >= 90.0f) {
        printf("Average = %.2f\nGrade = A\n", average);
    } else {
        if (average >= 75.0f) {
            printf("Average = %.2f\nGrade = B\n", average);
        } else {
            if (average >= 50.0f) {
                printf("Average = %.2f\nGrade = C\n", average);
            } else {
                printf("Average = %.2f\nGrade = F\n", average);
            }
        }
    }

    return 0;
}
```
## Output:
<img width="294" height="136" alt="image" src="https://github.com/user-attachments/assets/14afc185-4d9f-4a26-beb5-f53d58fce9e4" />

## Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# Ex.No:7
  Develop a C program to display the multiplication table of a given number (15) up to 10.
## Aim:
 To develop a C program that prints the multiplication table of the number 15 up to 10 using a for loop.
## Algorithm:
Step 1: Start<br>
Step 2: Include the standard input-output library: #include<stdio.h>.<br>
Step 3: Declare an integer variable number and initialize it with 15.<br>
Step 4: Declare another integer variable i to use as a loop counter.<br>
Step 5: Use a for loop to iterate from i = 1 to i = 10.<br>
  In each iteration:<br>
  a. Multiply number by i.<br>
  b. Print the result in the format: number x i = result.<br>
Step 6: Stop<br>
## Program:
```
#include <stdio.h>

int main() {
    int number = 15;  
    int i;            
    for (i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", number, i, number * i);
    }

    return 0;
}
```
## Output:
<img width="145" height="277" alt="image" src="https://github.com/user-attachments/assets/36223210-dd67-4854-905e-ca92edb9aa2e" />

## Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# Ex.No:8
  Develop a C program to check whether a given number is prime or not.
## Aim:
 To develop a C program that determines whether an input number is a prime number using a while loop.
## Algorithm:
Step 1: Start<br>
Step 2: Include the standard input-output library: #include<stdio.h>.<br>
Step 3: Declare integer variables:<br>
  n to store the number entered by the user<br>
  i to use as a counter (initialize to 2)<br>
  f as a flag to indicate whether the number is divisible (initialize to 0)<br>
Step 4: Read the value of n from the user.<br>
Step 5: Use a while loop to iterate while i <= n-1:<br>
  Check if n % i == 0:<br>
  If yes, set f = 1 (number is not prime) and break the loop.<br>
  Increment i by 1.<br>
Step 6: After the loop:<br>
  If f == 0, print that the number is prime.<br>
  Else, print that the number is not prime.<br>
Step 7: Stop<br>
## Program:
```
#include <stdio.h>

int main() {
    int n, i = 2, f = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    while (i < n ) {
        if (n % i == 0) {
            f = 1;   
            break;
        }
        i++;
    }
    if (f == 0 && n > 1) {
        printf("%d is a Prime number\n", n);
    } else {
        printf("%d is Not a Prime number\n", n);
    }

    return 0;
}
```
## Output:
<img width="212" height="57" alt="image" src="https://github.com/user-attachments/assets/bc947cae-3ec3-4e95-bb10-f7ac5c18e78e" />

## Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# Ex.No:9
  Generate the C code to display the pattern below.  
 ``` 
 12345  
 2   4  
 3   3  
 4   2  
 54321
 ```
## Aim:
 To build a C program that prints the required numeric pattern for a given value of n using nested loops.
## Algorithm:
Step 1: Start<br>
Step 2: Include the standard input-output library: #include<stdio.h>.<br>
Step 3: Declare variables i, j, n, and k.<br>
Step 4: Read the value of n from the user.<br>
Step 5: Set i = 1.<br>
Step 6: Repeat the following steps until i > n:<br> 
  Step 6.1: For j from i to n, print j if i == 1 or j == i, otherwise print a space.<br>
  Step 6.2: Set k = j - 2.<br>
  Step 6.3: For j from 1 to i - 1, print k if i == n or j == i - 1, otherwise print a space.<br>
  Step 6.4: Decrease k after each print.<br>
  Step 6.5: Move to the next line.<br>
Step 7: Increase i and repeat Step 6.<br>
Step 8: Stop<br>
## Program:
```
#include <stdio.h>
int main() {
    int n = 5, i, j;
    for (i = 1; i <= n; i++) {
        for (j = i; j <= n; j++)
            printf((i == 1 || j == i) ? "%d" : " ", j);
        for (j = 1; j < i; j++)
            printf((i == n || j == i - 1) ? "%d" : " ", n - j);
        printf("\n");
    }
    return 0;
}
```
## Output:
<img width="62" height="136" alt="image" src="https://github.com/user-attachments/assets/51dd7078-cb87-4e05-8f11-1cfcd340aa5e" />

## Result: 
  Thus, the program was implemented and executed successfully, and the required output was obtained.


# Ex.No:10
  Generate the C code to display the pattern below.  
```
 0
 7  0  7
 6  7  0  7  6
 5  6  7  0  7  6  5
 4  5  6  7  0  7  6  5  4
 3  4  5  6  7  0  7  6  5  4  3
 2  3  4  5  6  7  0  7  6  5  4  3  2
 1  2  3  4  5  6  7  0  7  6  5  4  3  2  1
```
## Aim: 
  To formulate a C program to print a symmetric numeric pattern in which each row contains an increasing sequence of numbers from the row value up to 7, followed by 0 in the center, and then a decreasing sequence of numbers back to the row value.
## Algorithm:
Step 1: Start<br>
Step 2: Include the standard input-output library: #include<stdio.h>.<br>
Step 3: Declare integer variables i and j.<br>
Step 4: Print 0 on the first line.<br>
Step 5: Set i = 7.<br>
Step 6: Repeat Steps 6.1 to 6.4 while `i >= 1`:<br>
   Step 6.1: For `j = i` to `7`, print `j`.<br>
   Step 6.2: Print `0` in the center.<br>
   Step 6.3: For `j = 7` down to `i`, print `j`.<br>
   Step 6.4: Move to the next line.<br>
Step 7: Decrease i by 1 and go back to Step 6.<br>
Step 8: Stop<br>
## Program:
```
#include <stdio.h>

int main() {
    int i, j;
    printf("0\n");
    for (i = 7; i >= 1; i--) {
        for (j = i; j <= 7; j++) {
            printf("%d ", j);
        }
        printf("0 ");
        for (j = 7; j >= i; j--) {
            printf("%d ", j);
        }
        printf("\n");
    }

    return 0;
}
```
## Output:
<img width="313" height="220" alt="image" src="https://github.com/user-attachments/assets/4e8e7424-48ed-473f-897d-53171a53d61c" />

## Result:
  Thus, the program was implemented and executed successfully, and the required output was obtained.
