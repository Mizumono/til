# Spread & Rest Operators

The spread and rest operators actually use the same syntax:
> ...

## Spread operator:

Spread syntax allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.

## Examples:
```javascript
const oldArray = [1, 2, 3];
const newArray = [...oldArray, 4, 5]; // This now is [1, 2, 3, 4, 5];
```
```javascript
const oldObject = {
    name: 'Gevorg'
};
const newObject = {
    ...oldObject,
    age: 28
};
```

[MDN
docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

## Rest parameters:

The rest parameter syntax allows us to represent an indefinite number of arguments as an array.

A function's last parameter can be prefixed with ... which will cause all remaining (user supplied) arguments to be placed within a "standard" javascript array. Only the last parameter can be a "rest parameter".

## Examples:
```javascript
function fun1(...theArgs) {
  console.log(theArgs.length);
}

fun1();  // 0
fun1(5); // 1
fun1(5, 6, 7); // 3
```

```javascript
function multiply(multiplier, ...theArgs) {
  return theArgs.map(function(element) {
    return multiplier * element;
  });
}

var arr = multiply(2, 1, 2, 3); 
console.log(arr); // [2, 4, 6]
```

[MDN
docs](developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)