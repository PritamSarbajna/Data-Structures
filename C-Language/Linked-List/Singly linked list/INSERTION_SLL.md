# INSERTION IN SINGLY LINKED LIST

## Insert at the end

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
