# Arrays
Arrays allow us to store multiple items which we can then access via an index. 

## Usage
# C#
```c#
int [] lottoNumbers = new int[7] {12, 3, 8, 1, 21, 7, 32};
```

## Cheat Sheet
|Description|Code|
|---------|-----|
|Access|`int iItem = lottoNumbers[i]`|
|Length|`int length = lottoNumbers.Length`|
|Sort|`Array.Sort(lottoNumbers)`|
|Copy|`Array.Copy(sourceArray, sourceIndex, destinationArray, destIndex, length)`|

## Characteristics
* Fixed size
* Hold items of the same type (C#)

# Notes
- `Array.Copy(sourceArray, sourceIndex, destinationArray, destIndex, length)`
    - If `sourceArray` and `destinationArray` are both reference-type arrays or are both arrays of type Object, 
        - a  shallow copy is performed.    
        - A shallow copy of an Array is a new Array containing references to the same elements as the original Array. The elements themselves or anything referenced by the elements are not copied. 
    - In contrast, a deep copy of an Array copies the elements and everything directly or indirectly referenced by the elements.

## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
|Access|O(1)|Access by index|
|Insert|O(N)|If capacity reached, copy contents to new, larger array|
|Delete|O(N)|Create new array without deleted item|