# Arrays
Arrays allow us to store multiple items which we can then access via an index. 

## Usage
```
let lottoNumbers: number [] = [12, 3, 8, 1, 21, 7, 32];
```
OR
```
let lottoNumbers: Array<number> = [12, 3, 8, 1, 21, 7, 32];
```

## Characteristics
* Fixed size
* Hold items of the same type (C#)

## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
|Access|O(1)|Access by index|
|Insert|O(N)|If capacity reached, copy contents to new, larger array|
|Delete|O(N)|Create new array without deleted item|