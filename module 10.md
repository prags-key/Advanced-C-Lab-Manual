EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.
PRAGATHI KUMAR
21222423200

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:


    struct Node {
        float data;
        struct Node* next;
    };
    
    struct Node* head = NULL;
    void search(char value) {
        struct Node* current = head;
        int position = 1;
        while (current != NULL) {
            if (current->data == value) {
                printf("item %c found at location %d\n", value, position);
                return;
            }
            current = current->next;
            position++;
        }
        printf("Item not found\n");
    }

Output:
<img width="753" height="501" alt="image" src="https://github.com/user-attachments/assets/776984d1-ff97-4806-8dd7-6a61505cdc2a" />




Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

    struct Node{
        char data; 
        struct Node *next;
    }*head;
    
    void insert(char data)
    {
        struct Node *n=(struct Node*)malloc(sizeof(struct Node));
        struct Node *temp;
        if(head==NULL)
        {
            head = n;
            head->data = data;
            n->next=NULL;
            return;
        }
        temp=head;
        while(temp->next!=NULL)
        {
            temp=temp->next;
        }
        n->data = data;
        n->next = NULL;
        temp->next= n;    
        
    }

Output:

<img width="523" height="520" alt="image" src="https://github.com/user-attachments/assets/f7b835ac-d4ae-4420-98d6-4a0c6c8e5070" />

 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

    struct Node
    {
        struct Node *prev;
        struct Node *next;
        char data;
    }*head;
    
    void display()
    {
        struct Node *ptr;
        //printf("\n printing values...\n");
        ptr = head;
        while(ptr != NULL)
        {
            printf("%c\n",ptr->data);
            ptr=ptr->next;
        }
    }

Output:

<img width="559" height="588" alt="image" src="https://github.com/user-attachments/assets/d1c38d6b-5423-4b02-bc3a-5c2c886a68fd" />


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

    struct Node
    {
        struct Node *prev;
        struct Node *next;
        char data;
    }*head;
    
    void insert(char data)
    {
       struct Node *ptr,*temp;
     //  int item;
       ptr = (struct Node *) malloc(sizeof(struct Node));
       if(ptr == NULL)
       {
           printf("OVERFLOW\n");
       }
       else
       {
           //printf("\nEnter value");
           //scanf("%d",&item);
            ptr->data=data;
           if(head == NULL)
           {
               ptr->next = NULL;
               ptr->prev = NULL;
               head = ptr;
           }
           else
           {
              temp = head;
              while(temp->next!=NULL)
              {
                  temp = temp->next;
              }
              
              temp->next = ptr;
              ptr ->prev=temp;
              ptr->next = NULL;
              }
    
           }
         //printf("\nnode inserted\n");
        }


Output:

<img width="501" height="560" alt="image" src="https://github.com/user-attachments/assets/083560ed-8ee3-47d1-84bb-2e75700a392c" />


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

    struct Node
    {
        struct Node *prev;
        struct Node *next;
        float data;
    }*head;
    
    void delete()
    {
        struct Node *ptr;
        if(head == NULL)
        {
            printf("UNDERFLOW\n");
        }
        else if(head->next == NULL)
        {
            head = NULL;
            free(head);
            printf("Node deleted\n");
        }
        else
        {
            ptr = head;
            head = head -> next;
            head -> prev = NULL;
            free(ptr);
            printf("Node deleted\n");
        }
    
    }

Output:

<img width="801" height="600" alt="image" src="https://github.com/user-attachments/assets/c8f35139-7e4a-4466-8b4c-6b539351b0fd" />





Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





