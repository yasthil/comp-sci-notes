# Arrays
Arrays allow us to store multiple items which we can then access via an index. 

## Usage
### C#
```
int [] lottoNumbers = new int[7] {12, 3, 8, 1, 21, 7, 32};
```

## Commonly used Properties (.Net)
|Description|Code|
|---------|-----|
|Access|`int iItem = lottoNumbers[i]`|
|Length|`int length = lottoNumbers.Length`|
|Sort|`Array.Sort(lottoNumbers)`|
|Copy|`Array.Copy(sourceArray, sourceIndex, destArray, destIndex, length)`|

## Characteristics
* Fixed size
* Hold items of the same type (C#)

## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
|Access|O(1)|Access by index|
|Insert|O(N)|If capacity reached, copy contents to new, larger array|
|Delete|O(N)|Create new array without deleted item|