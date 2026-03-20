

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

    printf("Stack elements are:\n");
    while (p != NULL) {
        printf("%d\n", p->data);
        p = p->next;
    }
}

int main() {
    struct Node *temp;

  
    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 10;
    temp->next = head;
    head = temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 20;
    temp->next = head;
    head = temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 30;
    temp->next = head;
    head = temp;

    display();

    return 0;
}

Output:

<img width="698" height="471" alt="image" src="https://github.com/user-attachments/assets/204d7e35-e297-4158-a438-ea1699aa112b" />



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
    struct Node *temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 10;
    temp->next = NULL;
    head = temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 20;
    temp->next = head;
    head = temp;

    pop();

    return 0;
}

Output:

<img width="562" height="392" alt="image" src="https://github.com/user-attachments/assets/c0acadfa-205f-4a1d-bcad-034853bab1d8" />




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

    printf("Queue elements are:\n");
    while (temp != NULL) {
        printf("%d\n", temp->data);
        temp = temp->next;
    }
}

int main() {
    struct Node *temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 10;
    temp->next = NULL;
    front = rear = temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 20;
    temp->next = NULL;
    rear->next = temp;
    rear = temp;

    display();

    return 0;
}

Output:

<img width="537" height="327" alt="image" src="https://github.com/user-attachments/assets/8f46160e-5df3-48a9-9093-c4e0cb6e559b" />


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
    enqueue(5);
    enqueue(15);
    enqueue(25);

    return 0;
}

Output:

<img width="408" height="332" alt="image" src="https://github.com/user-attachments/assets/c7f1eccf-80f8-4133-8e12-bcb067007ccb" />


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
    struct Node *temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 100;
    temp->next = NULL;
    front = rear = temp;

    temp = (struct Node*)malloc(sizeof(struct Node));
    temp->data = 200;
    temp->next = NULL;
    rear->next = temp;
    rear = temp;

    printf("Front element: %d\n", peek());

    return 0;
}

Output:

<img width="567" height="323" alt="image" src="https://github.com/user-attachments/assets/54a32ab6-d1c9-49e3-8a6f-464b1e04cd4a" />




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


