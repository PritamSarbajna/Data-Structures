# PREORDER TRAVERSAL

> Using recursion 


```
void preOrder(node *root){

    if(root == NULL){
        return;
    }

    cout << root->data << endl;
    preOrder(root->left);
    preOrder(root->right);
}
```
