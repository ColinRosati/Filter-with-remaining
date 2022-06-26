# Filter with remaining

Introduce a feature which additionally to filtered results, returns the unfiltered or remaining items in an array.

`Array.prototype.filter(callbackFN, {remaing: true}, thisArg)]`
`Array.prototype.filterWithRemaining()`

## Motivation
There are times where one needs to filter results and need to handle the remaining unfiltered results for some other purposes aswell. This could be achieved, in a round about way, doing an additional iteration with the inverted filter condition. This feature would return the filtered and remaing in the same array iteration.

## Example
```
const [filteredArray, remainingArray] = [1,2,3,4,5].filterWithRemaining( num => num % 2);

console.log(filteredArray) // [2,4]
console.log(remainingArray) // [1,3,5]
```

Alternatively we could make a optional parameter to the `filter` method.

```
const [filteredArray, remainingArray] = [1,2,3,4,5].filter( num => num % 2, {remaining: true})
```


[TC39 Discussion](https://es.discourse.group/t/filter-with-remaining-array-propotype-filterwithremaining/1380)
