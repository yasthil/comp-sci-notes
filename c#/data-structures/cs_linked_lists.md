# Linked lists
A Linked List is made up of independent nodes that may contain any type of data. Each node has a reference to the next node in the link.

## Characteristics
* Form of a sequential collection
* Does not have to be in order
* Fast insertions and deletions, without rearranging items or reallocation of space (more performant than arrays)
    * Insertions at the beginning or end of a linked list is fast - operating in constant time
        * Create a new Node with a value
        * Rearrange our reference variables
        * Reset the node which is now the head/tail
    * It's important to note that we're updating references here not moving the items in the list (unlike an array)
    * These allow for fast insertions for collections, push for stacks, and enqueue for queues.
* Types of LinkedLists:
    * Circularly Linked: Tail has reference to the Head and the Head to the Tail
    * Doubly Linked: Each node has a value and references to the next Node and the previous Node.


## Sample Code
# C#
* In .NET the `LinkedList<T>` provides separate nodes of type `LinkedListNode<T>`
* Each node in a `LinkedList<T>` object is of the type `LinkedListNode<T>`. Because the `LinkedList<T>` is **doubly linked**, each node points forward to the `Next` node and backward to the `Previous` node.
```c#
string [] maraudersMapAccessWords = {"solemnly", "swear", "that", "I", "am", "up", "to", "no", "good" };
LinkedList<string> incantation = new LinkedList<string>(maraudersMapAccessWords);

// add to beginning of list
incantation.AddFirst("I");

// remove
incantation.Remove("no"); 

// count
Console.WriteLine("Number of words in incantation: " + incantation.Count;

```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|
|Get First node|`incantation.First`||
|Get Last node|`incantation.Last`||
|Get Count|`incantation.Count`||

## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
|Insertion|O(1)| At the head/tail |
|Insertion|O(1)| If a specific Node is known, `AddAfter` |
|Deletion|O(1)| Head |
|Deletion|O(N)| If the Node is not Known |
|Count|O(1)||
|Traversing|O(N)||

