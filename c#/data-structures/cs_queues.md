# Queues
Represents a first-in-first-out (FIFO) collection of objects.
Queues anad Stacks are useful when you need temporary storage for infromation - when you might want to discard an element after retrieving its value.

Use a `Queue` if you need to access the information in the same order that it is stored in the collection.

## Usage
# C#
```c#
Queue<string> studentsWaiting = new Queue<string>();
studentsWaiting.Enqueue("Hermione");
studentsWaiting.Enqueue("Harry");
studentsWaiting.Enqueue("Ron");
Console.WriteLine(studentsWaiting.Dequeue());   // Hermione
```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|
|Enqueue|`studentsWaiting.Enqueue(item)`|Adds an element to the end of the Queue|
|Dequeue|`studentsWaiting.Dequeue()`|Removes the oldest element from the start of the Queue|
|Peek|`studentsWaiting.Peek()`|Returns the oldest element that is at the start of the Queue, but does not remove it|

## Characteristics
- Implemented as a circular array (C#)
- Objects stored in a `Queue<T>` are inserted at one end and removed at the other