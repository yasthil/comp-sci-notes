# Stacks
Variable sized Last-In-First-Out (LIFO) collection of items of the same type.

## Usage
# C#
```c#
Stack<string> numbers = new Stack<string>();
numbers.Push("one");
numbers.Push("two");
numbers.Push("three");
Console.WriteLine(numbers.Pop()); // "three"
```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|
|Insert|`numbers.Push("four")`|Inserts an item at the top of the stack|
|Remove|`numbers.Pop()`|Removes an item at the top of the stack|
|Peek|`numbers.Peek()`|Returns the item at the top of the stack, but does not remove it|

## Characteristics
* Variable size
* Implemented as an array (in C#)

## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
|Push|O(1)|When Count is less than the capacity|
|Push|O(N)|When Count is more than the capacity, capacity needs to be increased. N=Count|
|Pop|O(1)||
