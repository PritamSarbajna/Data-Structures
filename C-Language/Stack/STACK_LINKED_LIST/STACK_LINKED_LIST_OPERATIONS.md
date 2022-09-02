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

