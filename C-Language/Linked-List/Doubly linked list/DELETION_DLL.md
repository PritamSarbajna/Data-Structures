# DELETION IN A DOUBLY LINKED LIST

## _Delete at end_

- ### Function :

```
void deleteAtEnd(struct node** head){

    struct node* temp = *head;

    while(temp->next->next != NULL){
        temp= temp->next;
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

    deleteAtEnd(&head);
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
void deleteAtBegin(struct node** head){
    struct node* temp = *head;
    struct node* toDelete = temp;

    temp = temp->next;
    temp->prev = NULL;
    *head = temp;
    free(toDelete);
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

   deleteAtBegin(&head, 1);
}
```

## _Delete at Position_

- ### Function :

```
void deleteAtPosition(struct node** head, int pos){
    struct node* temp = *head;

    // If delete at the beginning
    if(pos == 0){
        struct node* toDelete = temp;
        temp = temp->next;
        temp->prev = NULL;
        *head = temp;
        free(toDelete);
        return;
    }

    while(pos--){
        temp = temp->next;
    }

    struct node* toDelete = temp;

    if(temp->next == NULL){
        temp->prev->next = NULL;
        free(toDelete);
        return;
    }
    temp->prev->next = temp->next;
    temp->next->prev = temp->prev;
    free(toDelete);

}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

   deleteAtPosition(&head, 1);
}
```
