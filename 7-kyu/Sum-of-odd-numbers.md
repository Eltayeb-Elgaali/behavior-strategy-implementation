# [Sum of odd numbers](https://www.codewars.com/kata/55fd2d567d94ac3bc9000064/solutions)

             1
          3     5
       7     9    11
   13    15    17    19
21    23    25    27    29
Given the triangle of consecutive odd numbers:
Calculate the row sums of this triangle from the row index (starting at index 1)
This function is to make a sum of the specific line members.

The script make the summation and give the value of the sum.

User will be required to enter which row he will make a summation for.

## Syntax

> rowSumOddNumbers(`number`) -> `number`

### Parameters

**n**: `number`

- A number representing the line's number.

### Return Value: `number`

The sum.

## Examples

The function is not complicated to understand. The exercise is so simple.

```js
console.log(rowSumOddNumbers(1)); // 1
console.log(rowSumOddNumbers(2)); // 3 + 5 = 8
```

---
---

## [AltenaMonk](https://www.codewars.com/users/AltenaMonk)

```js
function rowSumOddNumbers(n) {
  return n*n*n
}
```

### Strategy

This problem has only one parameter, and one variant possible return values.
AltenaMonk chose the strategy of Multiplying the argument 3 times by itself then return the result value.

### Implementation

AltenaMonk wrote his function using * operator to multiply the entered value 3X by itself.

**return value**: AltenaMonk use one line with`return` keyword.

### Possible Refactors

This strategy could also be implemented with these Implementation ...

- `Math.pow` function

---

## [user6239598](https://www.codewars.com/users/user6239598)

```js
const rowSumOddNumbers = n => Math.pow(n, 3);
```

### Strategy

user6239598 wrote a one-line implementation of his strategy that uses Mathematical `Math.pow` function.

### Implementation

**Math.pow**: This function use pow function to calculate the sum

**arrow**:  He used an arrow one line function.

### Possible Refactors

This strategy could also be implemented using these (but not only these) Implementation ...

- `* operator`

---

## Notes

Both solutions are relative looks like each other. the only difference is that user6239598 chose to use Math.pow function instead of multiplying the parameter 3 times.
