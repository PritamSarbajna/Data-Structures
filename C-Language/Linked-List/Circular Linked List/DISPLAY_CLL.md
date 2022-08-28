## _To Display circular linked list_

> NOTE : Same as singly linked list

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
