Create a lesson plan introducing the topic outlined above. The lesson plan needs to consist of the following material:

- An introduction of the topic to ‘stoke curiosity’ in the students (10 min. max.)
- 3 instructor demonstrations each introducing a different aspect of the topic (5 min. each)
- 3 hands-on activities that require students to implement demonstrated concepts to find a solution to a real-world problem (15 min. each)
- 3 review sessions of the concepts introduced in each activity (10 min. each)

You are free to make assumptions about prior knowledge of the students, but outline those assumptions at the beginning of your lesson plan. You are also free to define what is meant by ‘stoking curiosity’ and ‘real-world problem’. Feel free to create any additional materials or resources you think would be beneficial to students in learning this topic.

Please submit a repository containing any and all activity files, as well as the lesson plan composed in Markdown.

- - -

### Sources:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures
https://www.w3schools.com/js/js_function_closures.asp
https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36
https://medium.com/@prashantramnyc/javascript-closures-simplified-d0d23fa06ba4

### Closure concepts:
- It makes it possible for a function to have "private" variables.
- A closure is a function having access to the parent scope, even after the parent function has closed.
- Closures are frequently used in JavaScript for object data privacy
- A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.
- When you use closures for data privacy, the enclosed variables are only in scope within the containing (outer) function. You can’t get at the data from an outside scope except through the object’s privileged methods.
- Closures are important because they control what is and isn’t in scope in a particular function, along with which variables are shared between sibling functions in the same containing scope.
- It is unwise to unnecessarily create functions within other functions if closures are not needed for a particular task, as it will negatively affect script performance both in terms of processing speed and memory consumption.

### How-to:
To use a closure, define a function inside another function and expose it. To expose a function, return it or pass it to another function.
The inner function will have access to the variables in the outer function scope, even after the outer function has returned.

### Usage:
- Closures are commonly used to give objects data privacy.
- Closures can also be used to create stateful functions whose return values may be influenced by their internal state
    `const secret = msg => () => msg;`

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