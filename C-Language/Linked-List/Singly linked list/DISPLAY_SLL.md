## _To Display singly linked list_

- ### Function :

```
void display(struct node* head){
    struct node* temp = head;

    while(temp != NULL){
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    display(head);
    
}
```
