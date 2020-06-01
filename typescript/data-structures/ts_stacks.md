# Stacks
Variable sized Last-In-First-Out (LIFO) collection of items of the same type.

## Sample Code:
```typescript
export class Stack <T> {
    private _stack: T[];
    public push(item: T);
    public pop(): T;
    public peek(): T; 
}   
```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|
|Insert|`stack.push(item)`|Inserts an item at the top of the stack|
|Remove|`stack.pop()`|Removes an item at the top of the stack|
|Peek|`stack.peek()`|Returns the item at the top of the stack, but does not remove it|

## Characteristics
* Variable size