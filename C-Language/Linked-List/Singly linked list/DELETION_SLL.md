# DELETION IN A SINGLY LINKED LIST

## _Delete at end_

- ### Function :

```
void DeleteAtEnd(struct node** head){
    struct node* temp = *head;

    while(temp->next->next != NULL){
        temp = temp->next;
    }
    struct node* toDelete = temp->next;
    temp->next = NULL;
    free(toDelete);
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    DeleteAtEnd(&head);
}
```


## _Delete at Begin_

- ### Function :

```
void DeleteAtBegin(struct node** head){
    struct node* temp = *head;
    *head = temp->next;
    free(temp);
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    DeleteAtBegin(&head);
}
```

## _Delete at Begin_

- ### Function :

```
void DeleteAtPosition(struct node** head, int pos){
    struct node* temp = *head;

    while(pos--){
        temp = temp->next;
    }

    struct node* toDelete = temp->next;
    temp->data = temp->next->data;
    temp->next = temp->next->next;
    free(toDelete);
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    DeleteAtPosition(&head, 1);
}
```
