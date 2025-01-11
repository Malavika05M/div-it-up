# 1-data-types

### 🚀 Challenge

## 'Gotchas' in Javascript

1. Case Sensitivity
```javascript
let age = 1;
let Age = 2;
console.log(age == Age);         //returns false
```

The variables `age` and `Age` with different values `1` and `2` are two distinct variables due to case sensitivity. Therefore it returns false on the console.

2. `==` vs `===`

The `==` operator performs type coercion, while `===` checks for strict equality(value and type).
```javascript
console.log(1 == "1");    // true (type coercion) 
console.log(1 === "1");   // false (strict equality)
```

The `==` operator performs type coercion when 2 different data types are used to check for equality. Here, `12` is a number and `'12'` being a string. Therefore it converts the string `"1"` into a number and returns a true value for the equality check. But the `===` operator enforces strict data type equality check where both the arguments have to be of the same data type along with the same value to return true otherwise the console returns as false.

3. Adding Strings and Numbers

In case of addition, when adding a string Javascript converts the number to a string.
```Javascript
console.log(1 + "2");   // "12"
```
### Gotcha:
We have to ensure all operands are numbers to do arithmetic.

4. `null` and `undefined`

- `null` represents intentional absence of a value.
- `undefined` means a variable has been declared but a value is not assigned.
```Javascript
console.log(null == undefined);  // true (type coercion)
console.log(null === undefined);   // false (strict equality)
```

### Gotcha:
`null` and `undefined` are not interchangeable.

## Javascript Exercise

### Empty an Array (https://css-tricks.com/snippets/javascript/empty-an-array/)
```Javascript
var myArray = ["one", "two", "three"];
console.log(myArray);     //[ 'one', 'two', 'three' ]
myArray.length = 0;
console.log(myArray);     // []
```

## Assignment

Imagine you are building a shopping cart. Write some documentation on the data types that you would need to complete your shopping experience. How did you arrive at your choices?

### Solution

| Data type | Use |
| :-:       | :-: |
| String    | productName, productId, name, email|
| Numbers   | price, quantity|
| Object    | Objects are used to represent items in a shopping cart and other entities that has multiple related properties.|
| Array     | Arrays are used to manage lists such as product categories, store collections|
| Null      | Indicate the absence of a product or no discount applied|
| Boolean   | Booleans represent logical states like whether a user is logged in, a product is on sale and so on|


# 2-functions-methods

### 🚀 Challenge

### Articulate in one sentence the difference between functions and methods.

Function is a standalone block of code independent of object whereas method is a function linked to an object as it's property.

## Assignment

Create different functions, both functions that return something and functions that don't return anything.

See if you can create a function that has a mix of parameters and parameters with default values.

### Solution

### //Function that returns value
```Javascript
function add(a, b) {
return a + b;
}
```

### //Function that does not return anything (void function)
```Javascript
function print(message) {
    console.log(message);
}
const result = print("Hello");
console.log(result);
```

### //Function with default parameters
```Javascript
function multiply(a, b = 1) {
return a * b;                     //uses default b = 1 when no other value for b is given
}         
```

### //Function with mix of parameters
```Javascript
function divide(a, b = 1, roundTo = 2) {
return Number((a/b).toFixed(roundTo));
}
```

# 3-making-decisions

### 🚀 Challenge

Create a program that is written first with logical operators, and then rewrite it using a ternary expression

### //Program using logical operators
```Javascript
const value = '200';
if(value === 200) {
console.log('OK!');
} else if(value === 300) { 
console.log('Error');
} else {
console.log('Unknown value');
}
```

### //Program using ternary expression
```Javascript
const message = (value === 200) ? 'OK!' : 'Error';
```

Ternary expressions replaces multiple lines of `if-else` statements reducing clutter for simple logical decisions.
 
On the other hand , while working on large codebases it is better to the traditional `if-else` statements to avoid complexity and easier readability.

## Assignment
Grading System

```Javascript
let allStudents = ['A', 'B-', 1, 4 , 5 , 2];
let studentsWhoPass = [];

for(let i = 0; i < allStudents.length; i++) {
    let grade = allStudents[i];

    if(typeof grade === 'number') {                  //Checks if grade is a number
        if(grade >= 3) {
            studentsWhoPass.push(grade);
        }
    } else if (typeof grade === 'string') {          //Checks if grade is a string   
        if(['A', 'A-', 'B', 'B-', 'C', 'C-'].includes(grade)) {
            studentsWhoPass.push(grade);
        }
    }
}

console.log(studentsWhoPass);              // Output = ['A', 'B-', 4, 5]
```

# 4-arrays-loops

### 🚀 Challenge
There are other ways of looping over arrays other than for and while loops. There are forEach, for-of, and map. Rewrite your array loop using one of these techniques.

### Using for loop
```Javascript
let fruits = ['apple', 'banana', 'orange', 'mango', 'grape']

for(let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```

### Using forEach loop
```Javascript
let fruits = ['apple', 'banana', 'orange', 'mango', 'grape']

fruits.forEach(function(fruit) {
    console.log(fruit);
});
```

### Using for-of loop
```Javascript
let fruits = ['apple', 'banana', 'orange', 'mango', 'grape']

for(let fruit of fruits) {
    console.log(fruit);
}
```

### Using map
```Javascript
let fruits = ['apple', 'banana', 'orange', 'mango', 'grape']
let fruit = fruits.map((a) => a);
console.log(fruit);
```

## Assignment 
Create a program that lists every 3rd number between 1-20 and prints it to the console.

```Javascript
for(let i = 1; i <= 20; i+=3) {
    console.log(i);
}
```
