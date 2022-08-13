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


## _Reverse a linked list in K groups_

- ### Function :

```
struct node* kReverse(struct node* head, int k){

    // Base condition
    if(head == NULL){
        return NULL;
    }

    // reverse first K nodes
    struct node* prev = NULL;
    struct node* curr = head;
    struct node* next;
    int count = 0;

    while(curr != NULL && count < k){
        next = curr->next;
        curr->next = prev;
        prev = curr;
        curr = next;
        count++;
    }

    // Rest will be reversed recursively
    if(next != NULL){
        head->next = kReverse(next, k);
    }

    return prev;
}
```

- ### Calling the function inside function :

```
int main(){
    struct node* head = NULL;

    display(kReverse(head, 3));
}
```
