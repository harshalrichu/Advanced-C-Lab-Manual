

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```

#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* head = NULL;

void display() {
    struct Node* p = head;

    if (p == NULL) {
        printf("Stack is empty\n");
        return;
    }

    printf("Stack elements:\n");
    while (p != NULL) {
        printf("%d ", p->data);
        p = p->next;
    }
}

int main() {
    // manually creating stack
    head = (struct Node*)malloc(sizeof(struct Node));
    head->data = 30;

    head->next = (struct Node*)malloc(sizeof(struct Node));
    head->next->data = 20;

    head->next->next = (struct Node*)malloc(sizeof(struct Node));
    head->next->next->data = 10;
    head->next->next->next = NULL;

    display();

    return 0;
}
```

Output:

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/c1aa6617-0dd9-4e1d-85d4-1bf91d07d959" />



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* head = NULL;

void pop() {
    if (head == NULL) {
        printf("Stack is empty\n");
        return;
    }

    struct Node* temp = head;
    printf("Popped element: %d\n", temp->data);

    head = head->next;
    free(temp);
}

int main() {
    // create stack
    head = (struct Node*)malloc(sizeof(struct Node));
    head->data = 10;

    head->next = (struct Node*)malloc(sizeof(struct Node));
    head->next->data = 20;

    head->next->next = NULL;

    pop();
    pop();

    return 0;
}
```

Output:

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/ddb5eeba-7b3b-4e38-91c5-e4240a27c335" />




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node *front = NULL, *rear = NULL;

void display() {
    struct Node* temp = front;

    if (temp == NULL) {
        printf("Queue is empty\n");
        return;
    }

    printf("Queue elements:\n");
    while (temp != NULL) {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}

int main() {
    // sample queue
    front = rear = (struct Node*)malloc(sizeof(struct Node));
    front->data = 10;

    rear->next = (struct Node*)malloc(sizeof(struct Node));
    rear = rear->next;
    rear->data = 20;

    rear->next = (struct Node*)malloc(sizeof(struct Node));
    rear = rear->next;
    rear->data = 30;
    rear->next = NULL;

    display();

    return 0;
}
```

Output:

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/f9898b0d-1ff9-41da-aeb8-270017d03eea" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node *front = NULL, *rear = NULL;

void enqueue(int value) {
    struct Node* p = (struct Node*)malloc(sizeof(struct Node));
    p->data = value;
    p->next = NULL;

    if (front == NULL) {
        front = rear = p;
    } else {
        rear->next = p;
        rear = p;
    }

    printf("Inserted: %d\n", value);
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);

    return 0;
}
```

Output:
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/fce37544-64b3-42e6-b0ea-eff8c66a2ac7" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node *front = NULL, *rear = NULL;

int peek() {
    if (front == NULL) {
        printf("Queue is empty\n");
        return -1;
    }
    return front->data;
}

int main() {
    // create queue
    front = rear = (struct Node*)malloc(sizeof(struct Node));
    front->data = 10;

    rear->next = (struct Node*)malloc(sizeof(struct Node));
    rear = rear->next;
    rear->data = 20;
    rear->next = NULL;

    printf("Front element: %d\n", peek());

    return 0;
}
```

Output:

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/70980263-dd32-4090-933d-83b80e5c6452" />




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


