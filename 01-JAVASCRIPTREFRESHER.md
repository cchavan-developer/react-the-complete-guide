# React - The Complete Guide

## **Javascript Refresher**

Next Generation Javascript Features / ECMAScript 6

### **Understanding "var", "let" and "const"**

Read more about let : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let


Read more about const : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const


| Differences | var | let | const |
| ----------- | ----------- | ----------- | ----------- |
| Scope | functional | block | block |
| Hoisting | Allowed | Not Allowed | Not Allowed |
Hoisting means that you can define a variable before its declaration
| Reassign the value | Allowed | Allowed |  Not Allowed |
| Redeclare the variable | Allowed | Not Allowed |  Not Allowed |

### **Arrow Functions**
Different syntax for creating Javascript functions.
```
const name_of_function = (parameters) => {

}
```
**Advantages of using Arrow Function**

The following points will describe the list of advantages which are associated with using Arrow functions instead of normal functions –

- The new arrow function syntax reduces lot of code and makes it more readable.

- Arrow function syntax automatically binds “this” to the surrounding code’s context.

The 'this' Operator in ES5.

*The value of this is determined by a function's execution context, which in simple terms means how a function is called.* 

*Arrow functions use the value of this in their lexical scope.*

**When should we use Arrow Functions ?**

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions

- https://stackabuse.com/arrow-functions-in-javascript/

- https://medium.com/tfogo/advantages-and-pitfalls-of-arrow-functions-a16f0835799e

**Limitations of using Arrow functions**

Following are the certain limitations of using an arrow function:

- An arrow function doesn’t have its own bindings with this or super.
- An Arrow function should not be used as methods.
- An arrow function can not be used as constructors.
- An arrow function can not use yield within its body.
- Arrow function cannot be suitable for call, apply and bind methods.
- Arrow functions do not have a prototype property and they cannot be used with new.

### **Exports and Imports**

In React projects (and actually in all modern JavaScript projects), you split your code across multiple JavaScript
files - so-called modules. You do this, to keep each file/ module focused and manageable.

To still access functionality in another file, you need export (to make it available) and import (to get
access) statements.

You got two different types of
exports: default (unnamed) and named exports:

default => ``` export default person; ```

named => ``` export const professor; ```


You can import default exports like this:

``` 
import someNameOfYourChoice from './path/to/file.js' 
```

Surprisingly, "someNameOfYourChoice" is totally up to you. 

Named exports have to be imported by their name: 

```
import { someData } from './path/to/file.js';
```
A file can only contain one default and an unlimited amount of named exports. 

You can also mix the one default with any amount of named exports in one and the same file.

When importing named exports, you can also import all named exports at once with the following syntax:
```
import * as upToYou from './path/to/file.js';
```

### **Understanding Classes, Properties and Methods**

Classes are a feature which basically replace constructor functions and prototypes. You can define blueprints for JavaScript objects with them.

Like this:
```
classPerson {
    constructor () {
        this.name = Max;
    }
}

const person = new Person();
console.log(person.name); // prints 'Max'
```

In the above example, not only the class but also a property of that class (=> name ) is defined. The syntax you see there, is the "old" syntax for defining properties. 

In modern JavaScript projects (as the one used in this course), you can use the following, more convenient way of defining class properties:

```
classPerson {
    name = 'Max';
}

const person = new Person();
console.log(person.name); // prints 'Max'
```

You can also define methods. Either like this:

```
class Person { 
    name = 'Max';
    printMyName () {
        console.log(this.name); // this is required to refer to the class!
    }
}

const person = new Person();
person.printMyName();
```
Or like this:
```
class Person { 
    name = 'Max';
    printMyName = () => {
        console.log(this.name); // this is required to refer to the class!
    }
}

const person = new Person();
person.printMyName();
```
The second approach has the same advantage as all arrow functions have: The "this" keyword doesn't change its reference.

You can also use inheritance when using classes:
```
class Human {
    species = 'human';
}

class Person extends Human {
    name = "max",
    printMyName = () => {
        console.log(this.name);
    }
}

const person = new Person();
person.printMyName();
console.log(person.species); //prints 'human'

```

### **Spread and Rest Operators**

| Spread Operator | Rest Operator |
| ----------- | ----------- |
| Used to split up array elements OR object properties | Used to merge a list of function arguments into an array |
|

Spread operator:

```
const oldArray = [1, 2, 3];
const newArray = [...oldArray, 4, 5]; 

console.log(newArray);
// newArray would then be [1, 2, 3, 4, 5];

const oldObject = { 
    name: 'Max'
}; 

const newObject = {
    ...oldObject,
    age: 28
};

console.log(newObject);

/* newObject would then be
{
    name: 'Max',
    age: 28
} */

```

Rest Operator:

```
const getArguments = (...args) => {
    return args.filter(element => element === 1);
}
```

### **Destructuring**

Destructuring allows you to easily access the values of arrays or objects and assign them to variables.

```
const array = [1, 2, 3];
const [a, b] = array;
console.log(a); // prints 1
console.log(b); // prints 2
console.log(array); // prints [1, 2, 3]

const person = {
    name: 'Max',
    age: 27
}

{ name, age } = person;
console.log(name) = // prints 'Max'
console.log(age) = // prints 27
```

### **Refreshing Array Functions**

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array

- map()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map

- find()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find

- findIndex()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/
findIndex
- filter()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter

- reduce()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce?v=b

- concat()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat?v=b

- slice()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice

- splice()  => https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice

