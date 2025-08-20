# Ex18 B-Tree
## DATE:
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
1. Search for the item in the B-Tree node.
2. If the item exists, remove it from the node.
3. If the node becomes empty, update the root or adjust pointers accordingly.
4. Free memory of any node that becomes redundant. 
5. Ensure the B-Tree properties are maintained after deletion.  

## Program:
```
/*
Program to write a C function to delete an element in a B Tree
Developed by: SWETHA S
RegisterNumber: 212222230155
*/
```
```
/*
/*struct BTreeNode {
  int item[MAX + 1], count;
  struct BTreeNode *linker[MAX + 1];
};

struct BTreeNode *root;*/
void delete (int item, struct BTreeNode *myNode) {
    struct BTreeNode *temp;
    if(!delValFromNode(item,myNode))
    {
        printf("Not present.\n");
        return;
    }
    else
    {
        if(myNode->count==0)
        {
            temp=myNode;
            myNode=myNode->linker[0];
            free(temp);
        }
    }
    root=myNode;
    return;
    //type your code here
}
*/
```
## Output:
<img width="391" height="263" alt="image" src="https://github.com/user-attachments/assets/d9c44b0b-fc0e-46e4-a67d-f201b21299d4" />



## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
