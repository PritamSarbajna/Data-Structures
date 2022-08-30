# STACK OPERATIONS

- ## _push()_

```
void push(int val){

    if(top == N-1){
        printf("Stack Overflow\n");
    }

    top++;
    stack[top] = val;
}
```

- ## _pop()_

```
void pop(){
    if(top == -1){
        printf("Stack Underflow\n");
    }

    top--;
}
```
