# POSTORDER TRAVERSAL

> Using recursion 


```
void postOrder(node *root){

    if(root == NULL){
        return;
    }

    preOrder(root->left);
    preOrder(root->right);
    cout << root->data << endl;
}
```
