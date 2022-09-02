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


- ## _peek()_

```
int peek(){

    if(top == -1){
        printf("Stack is empty\n");
        return -1;
    }

    return stack[top];
}
```

- ## _isFull()_

```
bool isFull(){
    if(top == N-1){
        return true;
    }

    return false;
}
```

## _isEmpty()_

```
bool isEmpty(){
    if(top == -1){
        return true;
    }

    return false;
}
```

## _display()_

```
void display(){
    for(int i=top; i>=0; i--){
        printf("%d ", stack[i]);
    }
}
```
