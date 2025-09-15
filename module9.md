EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
PRAGATHI KUMAR 
21222423200
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

    int stack[100],top,i;
    void display()
    {
        for(int i=top;i>=0;i--)
        {
            printf("%d->",stack[i]);
        }
    }


Output:

<img width="707" height="663" alt="image" src="https://github.com/user-attachments/assets/1a42d6bb-ff92-4da2-aab2-c6bdb49bcf84" />



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

    int size=3,top=-1;
    float stack[100];
    void push (float data)
    {
        if(top==size-1)
        {
            printf("stack overflow");
        }
        else
        {
            top++;
            stack[top]=data;
        }
    }
Output:

<img width="551" height="643" alt="image" src="https://github.com/user-attachments/assets/d0aa4a4a-09d8-4f83-b09e-25ed7719e4d5" />




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

    int queue[50], rear, front;
    void display()
    {
        if(front==-1 || front> rear)
        {
            printf("No elements to display");
        }
        else
        {
            for(int i=front;i<=rear;i++)
            {
                printf("%d\n",queue[i]);
            }
        }
        
    }
Output:

<img width="781" height="561" alt="image" src="https://github.com/user-attachments/assets/89aedd02-c6fd-4121-afc5-daf5f463766c" />


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

    int rear,front,size=10;
    char queue[50];
    void enqueue(char data)
    {
        if(rear<size)
        {
            if(front==-1)
            {
            front=0;
            }
            rear++;
        queue[rear]=data;
            
        }
        
    }
Output:

<img width="759" height="452" alt="image" src="https://github.com/user-attachments/assets/e59ac9c3-5a89-489d-92bb-76c985473cda" />

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

    int front, rear;
    void dequeue()
    {
        if(front==-1||front>rear)
        {
            printf("Queue Underflow.\n");
            return;
        }
        else
        {
            front=front+1;
        }
    }
Output:

<img width="806" height="650" alt="image" src="https://github.com/user-attachments/assets/1d7fb2bc-1912-473a-8dd6-01c99887aad5" />


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully
