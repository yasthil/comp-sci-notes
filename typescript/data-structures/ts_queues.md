# Queues
Represents a first-in-first-out (FIFO) collection of objects.
Queues anad Stacks are useful when you need temporary storage for infromation - when you might want to discard an element after retrieving its value.

Use a `Queue` if you need to access the information in the same order that it is stored in the collection.

## Sample Code
# 
```typescript
export interface IQueue <T> {    
    public enqueue(item T): void;
    public dequeue(): T;
    public peek(): T;
}

export class Queue<T> implements IQueue<T> {
    private _queue: T[];
    public enqueue(item T): void {
        // Add an item to the end of the Queue
    }

    public dequeue(): T {
        // Removes the oldest element from the start of the Queue
        // and returns it        
    }

    public peek(): T {
        // returns the oldest element that is at the start of the Queue, but does not remove it
    }
}

const studentsWaiting: Queue<string> = new Queue <string>();
studentsWaiting.enqueue("Fred");
studentsWaiting.enqueue("George");
studentsWaiting.enqueue("Neville");
console.log(studentsWaiting.dequeue());     // Fred
```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|
|enqueue|`studentsWaiting.Enqueue(item)`|Adds an element to the end of the Queue|
|dequeue|`studentsWaiting.Dequeue()`|Removes the oldest element from the start of the Queue|
|peek|`studentsWaiting.Peek()`|Returns the oldest element that is at the start of the Queue, but does not remove it|

## Characteristics
- Objects stored in a Queue are inserted at one end and removed at the other