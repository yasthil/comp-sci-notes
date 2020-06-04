# Binary Search Trees (BST)
A Binary Search Tree (BST) is a tree in which all nodes have the following properties:
*   The `left sub-tree` of a node has a key `<=` it's parent's node's key
*   The `right sub-tree` of a node has a key `>` it's parent's node's key

```
left-sub-tree(keys) <= root-node(key) < right-sub-tree(keys)
```

## Sample Code
# C#
```c#
public class Node 
{
    public int data;
    public Node left;
    public Node right;

    public Node(int d)
    {
        data = d;
    }
}

```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|


## Characteristics


## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
