### Sources:

-   https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures
-   https://www.w3schools.com/js/js_function_closures.asp
-   https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36
-   https://medium.com/@prashantramnyc/javascript-closures-simplified-d0d23fa06ba4
-   https://www.youtube.com/watch?v=1JsJx1x35c0
-   https://dmitripavlutin.com/simple-explanation-of-javascript-closures/
-   http://javascriptissexy.com/understand-javascript-closures-with-ease/
-   https://scotch.io/courses/10-need-to-know-javascript-concepts/closures#:~:text=Closures%20give%20us%20the%20ability,through%20the%20object

### Closure concepts:

-   It makes it possible for a function to have "private" variables.
-   A closure is a function having access to the parent scope, even after the parent function has closed.
-   Closures are frequently used in JavaScript for object data privacy
-   A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.
-   When you use closures for data privacy, the enclosed variables are only in scope within the containing (outer) function. You can’t get at the data from an outside scope except through the object’s privileged methods.
-   Closures are important because they control what is and isn’t in scope in a particular function, along with which variables are shared between sibling functions in the same containing scope.
-   It is unwise to unnecessarily create functions within other functions if closures are not needed for a particular task, as it will negatively affect script performance both in terms of processing speed and memory consumption.
-   Lexical scoping (or static) means that the accessibility of variables is determined by the position of the variables in the source code inside the nesting scopes.

### Definition

-   The closure is a function that accesses its lexical scope even executed outside of its lexical scope. In other words, the closure is a function that remembers the variables from the place where it is defined, regardless of where it is executed later.

### How-to:

To use a closure, define a function inside another function and expose it. To expose a function, return it or pass it to another function.
The inner function will have access to the variables in the outer function scope, even after the outer function has returned.

### Usage:

-   Closures are commonly used to give objects data privacy.
-   Closures can also be used to create stateful functions whose return values may be influenced by their internal state
    `const secret = msg => () => msg;`
-   Emulate private methods

**Event Handlers:**

```
let countClicked = 0;

myButton.addEventListener('click', function handleClick() {
  countClicked++;
  myText.innerText = `You clicked ${countClicked} times`;
});
```

**Callbacks**

```
const message = 'Hello, World!';

setTimeout(function callback() {
  console.log(message); // logs "Hello, World!"
}, 1000);
```

**Functional Programming - Currying**
_(Currying happens when a function returns another function until the arguments are fully supplied)_

```
function multiply(a) {
  return function executeMultiply(b) {
    return a * b;
  }
}

const double = multiply(2);
double(3); // => 6
double(5); // => 10

const triple = multiply(3);
triple(4); // => 12
```

#### Example 1:

```
var add = (function () {
  var counter = 0;
  return function () {counter += 1; return counter}
})();

add();
add();
add();

// the counter is now 3
```

#### Example 2:

```
function outer() {
   var b = 10;
   function inner() {

         var a = 20;
         console.log(a+b);
    }
   return inner;
}
var X = outer(); //outer() invoked the first time
var Y = outer(); //outer() invoked the second time
```
