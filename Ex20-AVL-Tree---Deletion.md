# Ex20 AVL Tree - Deletion
## DATE:
## AIM:
To write a C function to delete an element from an AVL Tree.
## Algorithm
1. Search for the node to be deleted in the AVL Tree.
2. If the node is found:
If it has no children, remove it directly.
If it has one child, replace it with its child.
If it has two children, replace it with its inorder successor and delete the successor.
3. After deletion, update the height of the ancestors.
4. Check the balance factor and perform rotations (LL, RR, LR, RL) to maintain AVL property. 
5. Return the updated root of the subtree.  

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: SWETHA S
RegisterNumber: 212222230155 
*/
```
```
/*
node * Delete(node *T,int x)
{
node *p;
if(T==NULL)
{
return NULL;
}
else
if(x > T->data) // insert in right subtree
{
T->right=Delete(T->right,x);
if(BF(T)==2)
{
if(BF(T->left)>=0)
T=LL(T);
else
T=LR(T);
}}
else
if(x<T->data)
{
T->left=Delete(T->left,x);
if(BF(T)==-2) //Rebalance during windup
{
if(BF(T->right)<=0)
T=RR(T);
else
T=RL(T);
}}
else
{
//data to be deleted is found
if(T->right!=NULL)
{ //delete its inorder succesor
p=T->right;
while(p->left!= NULL)
p=p->left;
T->data=p->data;
T->right=Delete(T->right,p->data);
if(BF(T)==2)//Rebalance during windup
{
if(BF(T->left)>=0)
T=LL(T);
else
T=LR(T);}}
else
return(T->left);
}
T->ht=height(T);
return(T);
}
*/
```
## Output:
<img width="1082" height="258" alt="image" src="https://github.com/user-attachments/assets/587e33e6-6d14-4273-9b03-eb7acba47f6d" />



## Result:
Thus, the C program to delete an element from an AVL Tree is implemented successfully.
