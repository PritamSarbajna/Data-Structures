# INSERTION IN SINGLY LINKED LIST

## _Insert at the end_

- ### Function :

```
void InsertAtEnd(struct node** head, int val){
    struct node* newNode = (struct node*) malloc(sizeof(struct node));
    newNode->data = val;
    newNode->next = NULL;

    if(*head == NULL){
        *head = newNode; return;   
    }

    struct node* temp = *head;
    while(temp->next != NULL){
        temp = temp->next;
    }
    temp->next = newNode;
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    InsertAtEnd(&head, 1);
    InsertAtEnd(&head, 2);
    InsertAtEnd(&head, 3);
    InsertAtEnd(&head, 4);
    
}
```


## _Insert at Begin_

- ### Function :

```
void InsertAtBegin(struct node** head, int val){
    struct node* newNode = (struct node*) malloc(sizeof(struct node));
    newNode->data = val;
    newNode->next = *head;
    *head = newNode;
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    InsertAtBegin(&head, 1);
    InsertAtBegin(&head, 2);
    InsertAtBegin(&head, 3);
    InsertAtBegin(&head, 4);
    
}
```


## _Insert at a given position_

- ### Function :

```
void InsertAtPosition(struct node** head, int val, int pos){
    struct node* newNode = (struct node*) malloc(sizeof(struct node));
    newNode->data = val;

    struct node* temp = *head;

    while(--pos){
        temp = temp->next;
    }

    newNode->next = temp->next;
    temp->next = newNode;
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;
    
    InsertAtPosition(&head, 4, 1);
    
}
```
