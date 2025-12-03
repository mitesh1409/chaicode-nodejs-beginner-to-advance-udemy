# Data Types, Variables and Constants in JavaScript

## Built-in Data Types

There are total eight data types in JavaScript.  

**7 primitive data types:**  

* `number` for numbers of any kind: integer or floating-point, integers are limited by ±(253-1).
* `bigint` for integer numbers of arbitrary length.
* `string` for strings. A string may have zero or more characters, there’s no separate single-character type.
* `boolean` for true/false.
* `null` for unknown values – a standalone type that has a single value null.
* `undefined` for unassigned values – a standalone type that has a single value undefined.
* `symbol` for unique identifiers.

**1 Non-primitive data type:**  

* `object` for more complex data structures.

---

**Number**  
The number type represents both integer and floating point numbers.
Besides regular numbers, there are so-called “special numeric values” which also belong to this data type: `Infinity`, `-Infinity` and `NaN`.

**BigInt**  
When we need numbers outside the range of Number data type we can use BigInt.

Floating-Point Numbers:  

* Maximum Value: Number.MAX_VALUE represents the largest possible positive floating-point number, approximately 1.79E+308.
* Minimum Value: Number.MIN_VALUE represents the smallest possible positive floating-point number (closest to zero without being zero), approximately 5E-324. Negative floating-point numbers have the same magnitude range.

Integers:  

* Maximum Safe Integer: Number.MAX_SAFE_INTEGER represents the largest integer that can be safely and precisely represented, which is 2^53 - 1 (9,007,199,254,740,991).
* Minimum Safe Integer: Number.MIN_SAFE_INTEGER represents the smallest integer that can be safely and precisely represented, which is -(2^53 - 1) (-9,007,199,254,740,991).

**String**  
A string in JavaScript must be surrounded by quotes - '' (single quotes), "" (double quotes), `` (backticks).

**Boolean**  
The boolean type has only two values: true and false.

**null**  
The special null value does not belong to any of the types described above.

```javascript
console.log(typeof null); // object
```

**undefined**  

**object**  

**symbol**  

---

## JavaScript is Dynamically Typed

We can put any type in a variable. For example, a variable can at one moment be a string and then store a number:

```javascript
// no error
let message = "hello";
message = 123456;
```

Programming languages that allow such things, such as JavaScript, are called “dynamically typed”,  meaning that there exist data types, but variables are not bound to any of them.

---

## Printing Data

```javascript
console.log('Monday');
console.log('Sunday');

console.table({
    day1: 'Monday',
    day2: 'Tuesday',
    day3: 'Wednesday'
});

process.stdout.write('One');
process.stdout.write('Two');
process.stdout.write('Three');
```

## Reference

* [Javascript.info > Data Types](https://javascript.info/types)

---

## `var`, `let` and `const`

In modern JavaScript, we must declare variables using `let` or `const`.  
First declare them with `const`, if later on we found that it needs to be re-assigned in the  
application then use `let`. Do not use `var`.
