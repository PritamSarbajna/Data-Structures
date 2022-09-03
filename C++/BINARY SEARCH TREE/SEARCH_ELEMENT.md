# Searching an element in BST

```
bool searchInBST(node *root, int key){
    node *temp = root;

    while(temp != NULL){
        if(temp->data == key){
            return true;
        }

        if(temp->data > key){
            temp = temp->left;
        }
        else {
            temp = temp->right;
        }
    }

    return false;
}
```
