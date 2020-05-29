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

## Commonly used Properties
|Description|Code|
|---------|-----|
|Access|`const iLottoNumber:number = lottoNumbers[i]`|
|Length|`const length: number = lottoNumbers.length`|
|Append|`lottoNumbers.push(42)`|
|Remove/Replace|`lottoNumbers.splice(startIndex, deleteCount, items...)`|

## Characteristics
* Neither the length of a JavaScript array nor the types of its elements are fixed.
    * However, in Typescript, we restrict the array to only contain items of the same type
