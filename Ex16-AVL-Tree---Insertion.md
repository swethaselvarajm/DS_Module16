# Ex16 AVL Tree - Insertion
## DATE:
## AIM:
To write a C function to insert the elements in an AVL Tree.

## Algorithm
1. If the tree is empty, create a new node with the given value.
2. If the value is greater than the current node, insert in the right subtree.
3. If the value is less than the current node, insert in the left subtree.
4. After insertion, check the balance factor:
  If unbalanced, perform appropriate rotations (LL, RR, LR, RL) to restore balance. 
5. Update the height of the current node and return the node.  

## Program:
```
/*
Program to insert the elements in an AVL Tree
Developed by: SWETHA S
RegisterNumber: 212222230155 
*/
```
```
/*
node * insert(node *T,int x)
{
if(T==NULL)
{
T=(node*)malloc(sizeof(node));
T->data=x;
T->left=NULL;
T->right=NULL;
}
else
if(x > T->data) // insert in right subtree
{
T->right=insert(T->right,x);
if(BF(T)==-2)
{
if(x>T->right->data)
T=RR(T);
else
T=RL(T);
}
}
else
if(x<T->data)
{
T->left=insert(T->left,x);
if(BF(T)==2)
{
    if(x < T->left->data)
T=LL(T);
else
T=LR(T);
}
}
T->ht=height(T);
return(T);
}
 
*/
```
## Output:

<img width="1198" height="213" alt="image" src="https://github.com/user-attachments/assets/cc0a2830-57b6-49ed-8502-e4f1a90bf11a" />


## Result:
Thus, the function to insert the elements in an AVL Tree is implemented successfully in C programming language.
