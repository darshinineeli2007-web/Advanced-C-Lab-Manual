EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

```
#include <stdio.h>

int main() {
    int n;

    scanf("%d", &n);

    switch(n) {
        case 1: printf("one"); break;
        case 2: printf("two"); break;
        case 3: printf("three"); break;
        case 4: printf("four"); break;
        case 5: printf("five"); break;
        case 6: printf("six"); break;
        case 7: printf("seven"); break;
        case 8: printf("eight"); break;
        case 9: printf("nine"); break;
        default: printf("Greater than 9");
    }

    return 0;
}
```




Output:

<img width="562" height="531" alt="image" src="https://github.com/user-attachments/assets/3deb1872-742b-45ca-9287-e650f77eecb0" />







Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include <stdio.h>

int main() {
    char a[50];
    int i, j, count;

    scanf("%s", a);

    for (i = 0; i <= 9; i++) {
        count = 0;
        for (j = 0; a[j] != '\0'; j++) {
            if (a[j] == i + '0') {
                count++;
            }
        }
        printf("%d ", count);
    }

    return 0;
}
```




Output:
<img width="571" height="504" alt="image" src="https://github.com/user-attachments/assets/c6928eec-0638-471f-bdd7-f4a6124292e8" />







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include <stdio.h>
#include <string.h>

// function to swap characters
void swap(char *a, char *b) {
    char temp = *a;
    *a = *b;
    *b = temp;
}

// function to generate permutations
void permute(char *str, int l, int r) {
    int i;
    if (l == r) {
        printf("%s\n", str);
    } else {
        for (i = l; i <= r; i++) {
            swap((str + l), (str + i));
            permute(str, l + 1, r);
            swap((str + l), (str + i)); // backtrack
        }
    }
}

int main() {
    char str[50];

    scanf("%s", str);

    int n = strlen(str);
    permute(str, 0, n - 1);

    return 0;
}
```




Output:

<img width="493" height="461" alt="image" src="https://github.com/user-attachments/assets/30d4a04c-1c64-4f7c-ab91-04ab7fff2be9" />


Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

```
#include <stdio.h>

int main() {
    int n, i, j, min;

    scanf("%d", &n);

    int len = 2 * n - 1;

    for (i = 0; i < len; i++) {
        for (j = 0; j < len; j++) {
            int top = i;
            int left = j;
            int right = len - j - 1;
            int bottom = len - i - 1;

            min = top;
            if (left < min) min = left;
            if (right < min) min = right;
            if (bottom < min) min = bottom;

            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```



Output:


<img width="465" height="529" alt="image" src="https://github.com/user-attachments/assets/78091883-e8d4-4c31-b36e-8a904c686518" />






Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

```
#include <stdio.h>

int square() {
    int num;

    scanf("%d", &num);

    return num * num;
}

int main() {
    int result;

    result = square();

    printf("Square = %d\n", result);

    return 0;
}
```




Output:

<img width="303" height="389" alt="image" src="https://github.com/user-attachments/assets/3448d2b3-eaa8-4dbc-986d-31184d8d4396" />







Result:
Thus, the program is verified successfully



























