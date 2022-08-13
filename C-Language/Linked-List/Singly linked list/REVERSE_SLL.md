# REVERSE A SINGLY LINKED LIST

## _Iterative method_

- ### Function :

```
struct node* reverse(struct node* head){
    struct node* prevNode = NULL;
    struct node* currNode = head;
    struct node* nextNode;

    while(currNode != NULL){
        nextNode = currNode->next;
        currNode->next = prevNode;

        prevNode = currNode;
        currNode = nextNode;
    }
    return prevNode;
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    display(Reverse(head));
}
```
