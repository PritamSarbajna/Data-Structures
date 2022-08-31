# Linked List

- ### Node structure :

```
class node{
    public:
        int data;
        node* next;

        node(int value){
            data = value;
            next = NULL;
        }
};
```

## Types :

- ### Singly Linked List :

```
class node{
    public:
        int data;
        node* next;

        node(int value){
            data = value;
            next = NULL;
        }
};
```

![ll_page-0001](https://user-images.githubusercontent.com/90236635/184378492-58ad2fc9-f0bb-4129-81f1-23ef41954251.jpg)


- ### Doubly Linked List :

```
class node{
    public:
        int data;
        node* prev;
        node* next;

        node(int value){
            data = value;
            next = NULL;
            prev = NULL;
        }
};
```

![ll_page-0001](https://user-images.githubusercontent.com/90236635/184379804-dfc16b37-a425-419c-a0fe-7768f676f404.jpg)


- ### Circular Linked List :

```
class node{
    public:
        int data;
        node* next;

        node(int value){
            data = value;
            next = NULL;
        }
};
```

![ll_page-0001](https://user-images.githubusercontent.com/90236635/184381377-d1e547db-f79c-4984-a1e3-daddf024ec58.jpg)


- ### Doubly Circular Linked List :

```
class node{
    public:
        int data;
        node* prev;
        node* next;

        node(int value){
            data = value;
            next = NULL;
            prev = NULL;
        }
};
```

![Presentation1](https://user-images.githubusercontent.com/90236635/184383882-42a44516-01fa-434b-bd0a-2e287d399b4d.jpg)
