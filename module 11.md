

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>

void calculate_the_maximum(int n, int k) {
    int max_and = 0, max_or = 0, max_xor = 0;

    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {

            if ((i & j) < k && (i & j) > max_and)
                max_and = i & j;

            if ((i | j) < k && (i | j) > max_or)
                max_or = i | j;

            if ((i ^ j) < k && (i ^ j) > max_xor)
                max_xor = i ^ j;
        }
    }

    printf("%d\n%d\n%d\n", max_and, max_or, max_xor);
}

int main() {
    int n, k;

    printf("Enter n and k: ");
    scanf("%d %d", &n, &k);

    calculate_the_maximum(n, k);

    return 0;
}
```

Output:
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/1dd77417-bf83-4fea-8751-5920acbab14a" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int noshel, noque;
    scanf("%d %d", &noshel, &noque);

    int *nobookarr = (int*)calloc(noshel, sizeof(int));
    int **shelarr = (int**)malloc(noshel * sizeof(int*));

    while (noque--) {
        int type;
        scanf("%d", &type);

        if (type == 1) {
            int x, y;
            scanf("%d %d", &x, &y);

            shelarr[x] = (int*)realloc(shelarr[x], (nobookarr[x] + 1) * sizeof(int));
            shelarr[x][nobookarr[x]] = y;
            nobookarr[x]++;
        }
        else if (type == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", shelarr[x][y]);
        }
        else if (type == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", nobookarr[x]);
        }
    }

    return 0;
}
```

Output:
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/04ad09a2-51f8-4614-a85d-f7fa181e0203" />

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>

int main() {
    int n, i, sum = 0;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n];

    printf("Enter elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }

    printf("Sum = %d", sum);

    return 0;
}

```

Output:
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/0548f010-f26c-4d32-8b49-bc5724fb864e" />




Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int count = 0, i;

    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++) {
        if ((i == 0 && str[i] != ' ' && str[i] != '\n') ||
            (str[i] != ' ' && str[i-1] == ' ')) {
            count++;
        }
    }

    printf("Number of words = %d", count);

    return 0;
}
```


Output:
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/16c27451-fd9a-484a-9bc2-60c1f09991fd" />



 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int count = 0, i;

    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++) {
        if ((i == 0 && str[i] != ' ' && str[i] != '\n') ||
            (str[i] != ' ' && str[i-1] == ' ')) {
            count++;
        }
    }

    printf("Number of words = %d", count);

    return 0;
}
```
Output:
<img width="1920" height="1020" alt="Screenshot 2026-03-20 160711" src="https://github.com/user-attachments/assets/3b6c8784-355e-46e1-9699-21abe83f1524" />




Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
