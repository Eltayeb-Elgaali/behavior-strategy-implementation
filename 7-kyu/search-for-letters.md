# [Search for letters](https://www.codewars.com/kata/52dbae61ca039685460001ae)

This function is to accepts one arbitrary string as an argument, and return a string of length 26.

The objective is to set each of the 26 characters of the output string to either '1' or '0' based on the fact whether the Nth letter of the alphabet is present in the input.

So if an 'a' or an 'A' appears anywhere in the input string (any number of times), set the first character of the output string to '1', otherwise to '0'. if 'b' or 'B' appears in the string, set the second character to '1', and so on for the rest of the alphabet.

## Syntax

> change(`string`) -> `string`

### Parameters

**s**: `string`

- A string representing the arbitrary string.

### Return Value: `string`

## Examples

The function is simple.

```js
"a   **&  cZ"  =>  "10100000000000000000000001"
```

---
---

## [tezcatlipoca](https://www.codewars.com/users/tezcatlipoca)

```js
function change(string) {
  string = string.toLowerCase()
  return 'abcdefghijklmnopqrstuvwxyz'.split('').map(function (c) { 
    return string.indexOf(c) !== -1 ? 1 : 0;
  }).join('');
}
```

### Strategy

This problem has only one parameter, and one returned string value.
tezcatlipoca chose the strategy of all the alphabets to be used.

### Implementation

tezcatlipoca wrote his function using the building split function of string.

**return value**: tezcatlipoca use `return` keyword 2 times.

### Possible Refactors

This strategy could also be implemented with these Implementation ...

- arrow function

---

## [e.mihaylin](https://www.codewars.com/users/e.mihaylin)

```js
const change = s => {
  s = s.toLowerCase().replace(/[^a-z]/g, '');
  return Array.from(Array(26), (_, i) => +s.includes(String.fromCharCode(96 + ++i))).join``;
}
```

### Strategy

e.mihaylin use arrow function, array of letters and some built-in javascript string functions and one variable.

### Implementation

**toLowerCase**: This function convert to lower case.

**includes**:  This built-in function verify whether an item exist or not .

**join('')**:  This built-in function set separated elements as one string.

---

## Notes

Both have been using the whole alphabets list with different that e.mihaylin use an array in his implementation.
