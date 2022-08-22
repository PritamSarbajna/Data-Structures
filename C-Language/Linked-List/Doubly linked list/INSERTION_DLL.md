# INSERTION IN DOUBLY LINKED LIST

## _Insert at the end_

- ### Function :

```
void insertAtEnd(struct node** head, int val){
    struct node* newNode = (struct node*) malloc(sizeof(struct node));
    newNode->data = val;
    newNode->prev = NULL;
    newNode->next = NULL;

    if(*head == NULL){
        *head = newNode;
        return;
    }

    struct node* temp = *head;
    while(temp->next != NULL){
        temp = temp->next;
    }

    temp->next = newNode;
    newNode->prev = temp;
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
void insertAtBegin(struct node** head, int val){
    struct node* newNode = (struct node*) malloc(sizeof(struct node));
    newNode->data = val;
    newNode->prev = NULL;
    newNode->next = NULL;

    if(*head == NULL){
        *head = newNode;
        return;
    }

    newNode->next = *head;
    (*head)->prev = newNode;
    *head = newNode;
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;
    insertAtBegin(&head, 1);
    insertAtBegin(&head, 2);
    insertAtBegin(&head, 3);
    insertAtBegin(&head, 4);
    
}
```


## _Insert at a given position_

- ### Function :

```
void InsertAtPosition(struct node** head, int val, int pos){
    struct node* newNode = (struct node*) malloc(sizeof(struct node));
    newNode->data = val;

    struct node* temp = *head;

    while(pos--){
        temp = temp->next;
    }

    if(temp->next == NULL){
       temp->next = newNode;
       newNode->prev = temp;
       return;
    }

    newNode->next = temp->next;
    temp->next->prev = newNode;
    temp->next = newNode;
    newNode->prev = temp;
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;
    
    InsertAtPosition(&head, 4, 1);
    
}
```
