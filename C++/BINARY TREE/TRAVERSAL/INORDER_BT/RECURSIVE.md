# INORDER TRAVERSAL

> Using recursion 


```
void inOrder(node *root){

    if(root == NULL){
        return;
    }

    preOrder(root->left);
    cout << root->data << endl;
    preOrder(root->right);
}
```
