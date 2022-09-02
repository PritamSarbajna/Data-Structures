# STACK OPERATIONS

- ## _push()_

```
void push(int val){
    struct node *newnode = (struct node*) malloc(sizeof(struct node));
    newnode->data = val;

    newnode->next = top;
    top = newnode;
}
```


- ## _pop()_

```
void pop(){
    struct node *toDelete = top;
    top = top->next;
    free(toDelete);
}
```

- ## _peek()_

```
int peek(){

    if(top == NULL){
        return -1;
    }

    return top->data;
}
```

