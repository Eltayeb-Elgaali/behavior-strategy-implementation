# [Leap Years](https://www.codewars.com/kata/526c7363236867513f0005ca)

A leap year is the year that meets the following conditions:

    - year which divisible by 4 is a leap year
    - but year divisible by 100 is not leap year
    - but year divisible by 400 is leap year

The script determine, whether a given year is a leap year or not.

User will be required to enter a year then he will get true or false.

## Syntax

> isLeapYear(`number`) -> `boolean`

### Parameters

**year**: `number`

- A number of 4 digits representing the year.

### Return Value: `boolean`

True or False.

## Examples

The function is not complicated to understand. The exercise is so simple. Below is one leap year and the other is not leap year.

Leap year:

```js
const year2000 = isLeapYear(2000);
console.log(year2000); // true
```

Non Leap year:

```js
const year2003 = isLeapYear(2003);
console.log(year2003); // false
```

---
---

## [lcmaroni77](https://www.codewars.com/users/lcmaroni77@gmail.com)

```js
function isLeapYear(year) {
  if(0 == year%400) return true;
  if(0 == year%100) return false;
  if(0 == year%4) return true;
  return false;
}
```

### Strategy

This problem has only one argument, only 2 possible return values and three options.
lcmaroni77 chose the strategy of filtering which option is relative to the user choice then return the associated value.

### Implementation

lcmaroni77 wrote his function using if statement to filter the which value is related to the user choice.

**Default return value - false return**: lcmaroni77 set in his solution a default return value as false so if none of the 3 upper conditions were met, the function `return` false.

### Possible Refactors

This strategy could also be implemented with these Implementation ...

- `if else if else` statement
- `switch case`
- an arrow function

---

## [cloggy45](https://www.codewars.com/users/cloggy45)

```js
function isLeapYear(year) {
  return (year % 100 !== 0 && year % 4 === 0) || year % 400 === 0;
}
```

### Strategy

cloggy45 wrote a one-line implementation of his strategy that uses Mathematical Mod operator.

### Implementation

**year % 4, year % 100, year % 400**: This function use % operator to verify the divisibility

**parenthesis**:  He used parenthesis to set the two parties of && in one group.

### Possible Refactors

This strategy could also be implemented using these (but not only these) Implementation ...

- `switch case`

---

## Notes

In cloggy45's solution parenthesis have been used set a priority in  execution by mean to evaluate first the left side then come to the right side. In the beginning it seems that no need for the parenthesis.  Both solutions return boolean values `true` or `false` after examining 3 conditions.

The difference is that cloggy45 wrote his function in one line while lcmaroni77 wrote multi `if` statement.

One more difference is that lcmaroni77 set a default value to be returned if none of the 3.
 conditions is met.
