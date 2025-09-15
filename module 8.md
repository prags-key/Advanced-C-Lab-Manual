EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
PRAGATHI KUMAR
212224230200
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
   
    #include <stdio.h>
    
     int main() {
     int n;
 
     printf("Enter a number: ");
     scanf("%d", &n);
 
     switch (n) {
         case 5:
             printf("seventy one\n");
             break;
         case 6:
             printf("seventy two\n");
             break;
         case 7:
             printf("seventy three\n");
             break;
         case 8:
             printf("seventy four\n");
             break;
         case 9:
             printf("seventy five\n");
             break;
         case 10:
             printf("seventy six\n");
             break;
         case 11:
             printf("seventy seven\n");
             break;
         case 12:
             printf("seventy eight\n");
             break;
         case 13:
             printf("seventy nine\n");
             break;
         default:
             printf("Greater than 13\n");
             break;
     }
 
     return 0;
 }




Output:


<img width="516" height="320" alt="image" src="https://github.com/user-attachments/assets/ca5179cc-89d5-48d0-abbd-d6a91c517e08" />






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

    #include <stdio.h>
    #include <string.h>
    
    int main() {
        char a[50];
        int count[4] = {0};  
        int i, len;
    
        printf("Enter a string of digits: ");
        scanf("%s", a);
    
        len = strlen(a);
    
        for (i = 0; i < len; i++) {
            if (a[i] >= '0' && a[i] <= '3') {
                count[a[i] - '0']++;
            }
        }
    
        for (i = 0; i <= 3; i++) {
            printf("%d ", count[i]);
        }
    
        printf("\n");
    
        return 0;
    }





Output:


<img width="520" height="326" alt="image" src="https://github.com/user-attachments/assets/a4e927a5-d4a8-46e9-aa03-5b175510de89" />






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

    #include <stdio.h>
    #include <string.h>
    #include <stdlib.h>
    void swap(char **a, char **b) {
        char *temp = *a;
        *a = *b;
        *b = temp;
    }
    int next_permutation(char *arr[], int n) {
        int i = n - 2;
        while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0) {
            i--;
        }
        if (i < 0) {
            return 0; 
        }
        int j = n - 1;
        while (strcmp(arr[i], arr[j]) >= 0) {
            j--;
        }
    
        swap(&arr[i], &arr[j]);
    
        int left = i + 1, right = n - 1;
        while (left < right) {
            swap(&arr[left], &arr[right]);
            left++;
            right--;
        }
    
        return 1; 
    }
    
    int main() {
        int n;
        scanf("%d", &n);
    
        char *arr[n];
        for (int i = 0; i < n; i++) {
            arr[i] = (char *)malloc(101 * sizeof(char)); 
            scanf("%s", arr[i]); 
        }
        for (int i = 0; i < n; i++) {
            printf("%s ", arr[i]);
        }
        printf("\n");
        while (next_permutation(arr, n)) {
            for (int i = 0; i < n; i++) {
                printf("%s ", arr[i]);
            }
            printf("\n");
        }
        for (int i = 0; i < n; i++) {
            free(arr[i]);
        }
    
        return 0;
    }





Output:


<img width="620" height="454" alt="image" src="https://github.com/user-attachments/assets/a2aa51be-be61-4961-9e79-c4b516c2b9de" />






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
    #include <stdio.h>
    void printPattern() {
        int n;
        scanf("%d", &n);
        
        for (int i = 0; i < (2 * n - 1); i++) {
            for (int j = 0; j < (2 * n - 1); j++) {
                int min = i < j ? i : j;
                min = min < (2 * n - 2 - i) ? min : (2 * n - 2 - i);
                min = min < (2 * n - 2 - j) ? min : (2 * n - 2 - j);
                printf("%d ", n - min);
            }
            printf("\n");
        }
    }
    
    int main() {
        printPattern(); 
        return 0;
    }





Output:

<img width="747" height="589" alt="image" src="https://github.com/user-attachments/assets/a0a679cb-ef0f-409f-97dd-fa685929a60a" />







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

    #include <stdio.h>
    
    int square() {
        int num;
        printf("Enter a number: ");
        scanf("%d", &num);
        return num * num;
    }
    
    int main() {
        int result = square();
        printf("Square of the number is: %d\n", result);
        return 0;
    }




Output:


<img width="528" height="295" alt="image" src="https://github.com/user-attachments/assets/9f03cd8e-de31-45a7-95c9-38e419b3bfe7" />






Result:
Thus, the program is verified successfully



























