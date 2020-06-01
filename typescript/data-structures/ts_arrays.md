# Arrays
Arrays allow us to store multiple items which we can then access via an index. 

## Usage
```typescript
let lottoNumbers: number [] = [12, 3, 8, 1, 21, 7, 32];
```
OR
```typescript
let lottoNumbers: Array<number> = [12, 3, 8, 1, 21, 7, 32];
```

## Cheat Sheet
|Description|Code|
|---------|-----|
|Access|`const iLottoNumber:number = lottoNumbers[i]`|
|Length|`const length: number = lottoNumbers.length`|
|Append|`lottoNumbers.push(42)`|
|Remove/Replace|`lottoNumbers.splice(startIndex, deleteCount, items...)`|
|Operation for each item (map)|`const specialNumbers = lottoNumbers.map(item => item * 2) // returns array with all items muliplied by 2`|
|Iteration|foreach: `lottoNumbers.forEach(item => console.log(item))`|
||for loop: `for(let i:number = 0; i < lottoNumbers.length; i++){}`|
|Merge Arrays|`const allNumbers: number [] = lottoNumbers.concat(specialNumbers);`|

## Characteristics
* Neither the length of a JavaScript array nor the types of its elements are fixed.
    * However, in Typescript, we restrict the array to only contain items of the same type
