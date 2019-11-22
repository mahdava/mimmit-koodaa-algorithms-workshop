# Resources to get familiar with JavaScript

To have a better experience throughout the workshop, we need you to be familiar with JavaScript syntax.

This section will go through the basics of JavaScript providing useful resources and will help you familiarize with the code syntax.

## Vocabulary

**Expression:**  
**Value:**  
**Operator:**  
**Syntax:**  
**Algorithm:**  
**Data Structure:**

## Syntax and styles

To familiarize with JavaScript syntax, please [read this page on how JavaScript syntax works](https://www.w3schools.com/js/js_syntax.asp).

## Chapter 1 - Commenting and uncommenting

In JavaScript, you can comment code lines with `//` to comment one single line, and `/*` with `*/` to mark more than one line of code to comment.

`// I'm a single commented line`

```
/*
and multiple lines like this
and multiple lines like this
and multiple lines like this
*/
```

It's useful to comment code when you are testing different things and want to see different outcomes, as well as when you want to add a description about what your code does.

**To comment code, use cmd + k and while still pressing cmd press c**  
**To uncomment code, use cmd + k and while still pressing cmd press u**

Great! Now you're able to comment and uncomment code!

## Chapter 2 - Console and console.log()

Let's learn about console.log() and first, what's the [Chrome devtools console](https://developers.google.com/web/tools/chrome-devtools/console/javascript).

While we're using Code Sandbox, we can open the in-built console tab!

`console.log("Hi, this is a console log message");`

You can also write direct statements in the console log, such as `2 + 2`.

The console allows you to also test arbitrary code that is not written within the page:

**JavaScript ES5**  
`function multiplyNumbers(x, y) { return x * y; }`

**JavaScript ES6**  
`const multiplyNumbersES6 = (x, y) => { return x * y; };`

Note: ES6 syntax works only in the actual Chrome Dev tools console, but that's the better way to write code, as ES5 lacks few good features. You can of course write ES6 code in the actual code editor of CodeSandbox.

Write/Copy the following function inside the console:

`function multiplyNumbers(x, y) { return x * y; }`

The console will return a message **undefined** because the entered code didn't generate any value to display, but if you now type

`multiplyNumbers(2, 3)`

the console will reply with 6.

While working with algorithms, using `console.log()` becomes useful to check that the code is looping the information correctly and that your code is returning the right values at all the stages.

## Chapter 3 - Variable types and declaration

Time to move on to variables! Surprisingly enough, there's so much to say about variables and that's why we're linking [JavaScript.info page about JavaScript Data Types](https://javascript.info/types). What we need to get out of this page is that there are 7 basic data types in JavaScript, and in our workshop we're going to use almost all of them.

**Primitive:**  
`number` integer or floating-point.  
`string` for strings.  
`boolean` for true/false.  
`null` for unknown values – a standalone type that has a single value null.  
`undefined` for unassigned values – a standalone type that has a single value undefined.

**Reference:**  
`arrays` a list that can hold multiple values, accessible through their index  
`object` for more complex data structures.  
`functions`  
`dates`  
anything else

If you are familiar with another programming language, or if you have time and feel curious, I suggest reading [this article about JavaScript variable declarations and scope](https://blog.pragmatists.com/let-your-javascript-variables-be-constant-1633e56a948d) to familiarize with variable scope and better understand the difference between the old `var`, `const` and `let`. For the sake of this workshop, you mainly need to know that you can declare variables with `const`and `let` keywords - feel free to ask to a coach about the differences between the two.

```
const onePoundInKg = 0,453592;
let apples = 10; const applesStack = [1, 4, 5];
```

## Chapter 4 - Operators

Please read [this page about operations in JavaScript](https://www.w3schools.com/js/js_operators.asp).

## Chapter 5 - Arrays

Please read [this page about arrays](https://www.w3schools.com/js/js_arrays.asp). There's also [this page for a more in-depth reading about arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).

### Array properties

One array property commonly used for arrays is `.length`, and as you might guess it allows us to access the number of items contained in the array.

```
const fruits = ['Banana', 'Apple', 'Lemon'];
console.log(fruits.length); // will return the number of fruits
```

### Array methods

In the Section 2 of this repository, you will encounter these two methods.

`push()` function is used to insert an element at the top of the stack.
The element is added to the stack container and the size of the stack is
increased by 1.

`pop()` function is used to remove an element from the top of the
stack(newest element in the stack). The element is removed to the stack
container and the size of the stack is decreased by 1.

Please read [this page on how to use arrays](https://www.w3schools.com/js/js_array_methods.asp). [Here's a list of other methods applicable to arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Instance_methods).

## Chapter 6 - Objects

[Read more about objects here](https://www.w3schools.com/js/js_objects.asp).

## Chapter 7 - If condition

Please [read this page about If statement](https://www.w3schools.com/js/js_if_else.asp).

## Chapter 8 - Switch statement

Please [read this page about Switch statement](https://www.w3schools.com/js/js_switch.asp).

## Chapter 9 - For loop

```
for (let i = 0; i < 10; i++) {
    console.log(i);
  }
```

## Chapter 10 - Functions

Functions are used to reuse code, you define what the code should do once and use it as many times as needed with different arguments (parameters) to produce different results.

A [good explanation about functions can be found here](https://www.w3schools.com/js/js_functions.asp), however please notice that the guide uses ES5 syntax. Check the following code examples to see how to use ES6 syntax.

```
const exampleFunctionWithoutParameters = () => {
const result = 1;
return result;
};
```

```
const exampleFunctionWithTwoNumberParameters = (
firstParameter,
secondParameter
) => {
return firstParameter + secondParameter;
};
```

```
const printTenTimes = () => {
  for (let i = 0; i < 10; i++) {
    console.log(i);
  }
};
```

## Chapter 11 - Merge all this knowledge to create your own thing

This is an example that summarizes all the things we've been working on so far. Take it as a guideline to create your own set of scripts!

```
let products = [
  {
    name: "chair",
    inventory: 5,
    unit_price: 45.99
  },
  {
    name: "table",
    inventory: 10,
    unit_price: 123.75
  },
  {
    name: "sofa",
    inventory: 2,
    unit_price: 399.50
  }
];
function listProducts(prods) {
  let product_names = [];
  for (let i=0; i<prods.length; i+=1) {
   product_names.push(prods[i].name);
  }
  return product_names;
}
console.log(listProducts(products));
function totalValue(prods) {
  let inventory_value = 0;
  for (let i=0; i<prods.length; i+=1) {
    inventory_value += prods[i].inventory * prods[i].unit_price;
  }
  return inventory_value;
}
console.log(totalValue(products));
```

This [example code was taken from teamtreehouse](https://teamtreehouse.com/library/create-an-array-of-objects).
