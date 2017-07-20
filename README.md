# Javascript Cheat Sheet

## String

#### access

`charAt(index)` - returns the character at `index`

`substring(start, end)` - returns string from `start` to `end - 1`. if `start > end`, they are swapped

`slice(start, end)` - like substring, but without the swapping. instead if `start >= end`, an empty string is returned

`substr(start, count)` - returns string from `start` to `start + count`

#### search

`endsWith(str)` - returns whether end of string matches `str`

`startsWith(str)` - returns whether start of string matches `str`

`includes(str)` - returns whether string matches `str` anywhere


`indexOf(str)` - returns first index at where `str` was found

`lastIndexOf(str)` - returns last index at where `str` was found


`match(regex)` - returns `regex` matches for string

`search(regex/str)` - returns index of first `regex/str` match

#### map

`repeat(count)` - returns string repeated `count` times

`split(str)` - returns array of chunks, split on `str`

`replace(regex/str, str2)` - replaces `regex/str` matches with `str2`

## Array

#### mutation

`push(elem)` - adds `elem` to end of array, returns new array length

`unshift(elem)` - adds `elem` to beginnging of array, returns new array length

`pop()` - removes and returns last element in the array

`shift()` - removes and returns first element in array

`splice(start, count, ...elems)` - remove count number of elements starting at `start`, if `elems` provided, insert them at `start`

`reverse()` - reverses the array

`fill(elem, start, end)` - replace elems with `elem` from `start` to `end`

#### map

`map(iteratee(el, idx, arr))` - returns a new array with iteratee applied to each element

`concat(...elems)` - merges array with `elems` into new array, arrays in `elems` first unpacked to values

`slice(start, end)` - returns array from index `start` to `end - 1`. if `start >= end`, an empty array is returned

`filter(iteratee(el, idx, arr))` - returns an array composed of all elements for which iteratee returns true

#### reduce/search

`reduce(iteratee(acc, el, idx, arr), startAcc)` - returns a value composed of `startAcc` and running `iteratee` on each element in array

`reduceRight` - like `reduce` but then iterated from end of array to beginning

`indexOf(elem)` - returns first index at where `elem` was found (using `===`)

`lastIndexOf(elem)` - returns last index at where `elem` was found (using `===`)

`every(iteratee(el, idx, arr))` - returns whether iteratee returns true for every element in array

`some(iteratee(el, idx, arr))` - returns whether iteratee returns true for any element in array

`join(str)` - returns string with each elem in array joined by `str`

`includes(elem, start)` - find `elem` in array, if start is undefined or < 0, the entire array is searched

## async/await

```
async function foo() {
    return 42;
}
```

is syntactic sugar for:

```
function foo() {
    return new Promise(resolve => {
        resolve(42);
    });
}
```

and this:

```
const data = await something();
// ...do something...
```

is syntactic sugar for:

```
something().then(data => {
    // ...do something...
});
```

- `async` keyword makes a function return a promise which is `resolve`d when the function returns
- `await` keyword waits (locally blocks) for an async function (or promise) to resolve and then replaces the promise with the value it resolved to and continues code execution

More info, see: [Tips for using async functions](http://2ality.com/2016/10/async-function-tips.html)
