# Binary Search Trees (BST)
A Binary Search Tree (BST) is a tree in which all nodes have the following properties:
*   The `left sub-tree` of a node has a key `<=` it's parent's node's key
*   The `right sub-tree` of a node has a key `>` it's parent's node's key

```
left-sub-tree(keys) <= root-node(key) < right-sub-tree(keys)
```

## Sample Code
# Typescript
```typescript
export class Node {
    public data: number;
    public left: Node;
    public right: Node;

    public Node(data:int): void {
        this.data = data;
        this.left = null;
        this.right = null;
    }
}

```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|


## Characteristics
* A BST is an ordered data structure
* Nodes are inserted in an orderly fashion
* Searching is fast
    * We are able to cut the amount of data to sort through in half on each pass (Binary Search on an ordered array)
* Inserting, deleting and searching are fast for a BST
* Types of Search
    * Depth First
        * preOrder
        * inOrder
        * postOrder
    * Breadth First
## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
