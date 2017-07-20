# Javascript Cheat Sheet

## String

#### access

[`charAt(index)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charAt) - returns the character at `index`

[`substring(start, end)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring) - returns string from `start` to `end - 1`. if `start > end`, they are swapped

[`slice(start, end)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice) - like substring, but without the swapping. instead if `start >= end`, an empty string is returned

[`substr(start, count)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr) - returns string from `start` to `start + count`

#### search

[`endsWith(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/endsWith) - returns whether end of string matches `str`

[`startsWith(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/startsWith) - returns whether start of string matches `str`

[`includes(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes) - returns whether string matches `str` anywhere


[`indexOf(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf) - returns first index at where `str` was found

[`lastIndexOf(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/lastIndexOf) - returns last index at where `str` was found


[`match(regex)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match) - returns `regex` matches for string (`regex` is converted to RegEx, if isn't one yet). Wrapper for `RegExp.exec`.

[`search(regex)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/search) - returns index of first `regex` match (`regex` is converted to RegEx, if isn't one yet)

#### map

[`repeat(count)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) - returns string repeated `count` times

[`split(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split) - returns array of chunks, split on `str`

[`replace(regex/str, str2)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace) - replaces `regex/str` matches with `str2`

## Array

#### mutation

[`push(elem)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push) - adds `elem` to end of array, returns new array length

[`unshift(elem)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift) - adds `elem` to beginnging of array, returns new array length

[`pop()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop) - removes and returns last element in the array

[`shift()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift) - removes and returns first element in array

[`splice(start, count, ...elems)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice) - remove count number of elements starting at `start`, if `elems` provided, insert them at `start`

[`reverse()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse) - reverses the array

[`fill(elem, start, end)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/fill) - replace elems with `elem` from `start` to `end`

#### map

[`map(iteratee(el, idx, arr))`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) - returns a new array with iteratee applied to each element

[`concat(...elems)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat) - merges array with `elems` into new array, arrays in `elems` first unpacked to values

[`slice(start, end)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) - returns array from index `start` to `end - 1`. if `start >= end`, an empty array is returned

[`filter(iteratee(el, idx, arr))`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) - returns an array composed of all elements for which iteratee returns true

#### reduce/search

[`reduce(iteratee(acc, el, idx, arr), startAcc)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce) - returns a value composed of `startAcc` and running `iteratee` on each element in array

[`reduceRight`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduceRight) - like `reduce` but then iterated from end of array to beginning

[`indexOf(elem)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf) - returns first index at where `elem` was found (using `===`)

[`lastIndexOf(elem)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/lastIndexOf) - returns last index at where `elem` was found (using `===`)

[`every(iteratee(el, idx, arr))`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every) - returns whether iteratee returns true for every element in array

[`some(iteratee(el, idx, arr))`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some) - returns whether iteratee returns true for any element in array

[`join(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join) - returns string with each elem in array joined by `str`

[`includes(elem, start)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) - find `elem` in array, if start is undefined or < 0, the entire array is searched

### RegExp

#### Creation

- `new RegExp(str, modifiers)`

- `/<str>/<modifiers>`

`str` is a regex which consists of one or more Tokens. `modifiers` are optional

#### Methods
[`test(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test) - returns whether the regex has any matches in `str`

[`exec(str)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/exec) - search for any matches in `str`, returns `null` if no match found. Updates regex object

#### Tokens

`abc…` - Letters

`123…` - Digits

`\d` - Any Digit

`\D` - Any Non-digit character

`.` - Any Character

`\.` - Period

`[abc]` - Only a, b, or c

`[^abc]` - Not a, b, nor c

`[a-z]` - Characters a to z

`[0-9]` - Numbers 0 to 9

`\w` - Any Alphanumeric character

`\W` - Any Non-alphanumeric character

`{m}` - m Repetitions

`{m,n}` - m to n Repetitions

`*` - Zero or more repetitions

`+` - One or more repetitions

`?` - Zero or one repetitions

`\s` - Any Whitespace

`\S` - Any Non-whitespace character

`^…$` - Starts and ends

`(…)` - Capture Group

`(a(bc))` - Capture Group and Sub-group

`(abc|def)` - Matches abc or def


#### Modifiers

`i` - performs case-insensitive matching

`g` - performs a global match (find all matches rather than stopping after the first match)

`m` - performs multiline matching

#### Reference

- [RegexOne tutorial](https://regexone.com/)

- [RegEx101 interactive regex tester](https://regex101.com/)


## async/await

```js
async function foo() {
    return 42;
}
```

is syntactic sugar for:

```js
function foo() {
    return new Promise(resolve => {
        resolve(42);
    });
}
```

and this:

```js
const data = await something();
// ...do something...
```

is syntactic sugar for:

```js
something().then(data => {
    // ...do something...
});
```

- `async` keyword makes a function return a promise which is `resolve`d when the function returns
- `await` keyword waits (locally blocks) for an async function (or promise) to resolve and then replaces the promise with the value it resolved to and continues code execution

More info, see: [Tips for using async functions](http://2ality.com/2016/10/async-function-tips.html)
