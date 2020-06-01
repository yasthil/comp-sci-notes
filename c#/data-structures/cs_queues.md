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
|Enqueue|``||
|Dequeue|``||
|Peek|``||

## Characteristics

## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|

