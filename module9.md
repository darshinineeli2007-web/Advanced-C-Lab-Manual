EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
#include <stdio.h>

#define MAX 5
int stack[MAX], top = -1;

void display() {
    if (top == -1) {
        printf("Stack is empty\n");
    } else {
        printf("Stack elements are:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

int main() {
    stack[++top] = 10;
    stack[++top] = 20;
    stack[++top] = 30;

    display();

    return 0;
}
```
Output:

<img width="1835" height="573" alt="image" src="https://github.com/user-attachments/assets/53d3a6ad-8386-4685-a328-3a2777298b92" />




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
#include <stdio.h>

#define MAX 5
float stack[MAX];
int top = -1;

void push(float x) {
    if (top == MAX - 1) {
        printf("Stack Overflow\n");
    } else {
        stack[++top] = x;
        printf("Pushed: %.2f\n", x);
    }
}

int main() {
    push(10.5);
    push(20.2);
    push(30.7);

    return 0;
}
```
Output:
<img width="1802" height="557" alt="image" src="https://github.com/user-attachments/assets/8e71e180-50f6-48e5-ae83-6d90d2776d68" />





Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
#include <stdio.h>

#define MAX 5
int queue[MAX], front = 0, rear = 2;

void display() {
    printf("Queue elements are:\n");
    for (int i = front; i <= rear; i++) {
        printf("%d\n", queue[i]);
    }
}

int main() {
    queue[0] = 10;
    queue[1] = 20;
    queue[2] = 30;

    display();

    return 0;
}
```
Output:

<img width="1847" height="502" alt="image" src="https://github.com/user-attachments/assets/dfe52847-2e8a-404e-b342-388c30999556" />



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>

#define MAX 5
float queue[MAX];
int front = -1, rear = -1;

void enqueue(float x) {
    if (rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        if (front == -1) front = 0;
        queue[++rear] = x;
        printf("Inserted: %.2f\n", x);
    }
}

int main() {
    enqueue(11.1);
    enqueue(22.2);
    enqueue(33.3);

    return 0;
}
```
Output:

<img width="1902" height="532" alt="image" src="https://github.com/user-attachments/assets/5d7e1729-1991-4cbf-9111-9c06555f0bfe" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
#include <stdio.h>
int queue[MAX];
int front = 0, rear = 2;

void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue is empty\n");
    } else {
        printf("Deleted element: %d\n", queue[front]);
        front++;

        if (front > rear) {
            front = rear = -1;
        }
    }
}

int main() {
    queue[0] = 10;
    queue[1] = 20;
    queue[2] = 30;

    dequeue();
    dequeue();

    return 0;
}
```
Output:

<img width="1856" height="603" alt="image" src="https://github.com/user-attachments/assets/2e09bc22-07f9-499e-9292-bad5086d211d" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
