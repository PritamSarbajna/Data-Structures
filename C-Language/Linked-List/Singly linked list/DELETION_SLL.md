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
