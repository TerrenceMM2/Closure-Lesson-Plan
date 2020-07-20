# JavaScript Closures

## Overview

You will introduce students to the concept of Closures in JavaScript.

## Instructor Notes

-   With the introduction of closures, we now venture into more abstract programming concepts, namely the concept of private methods and a deeper dive into scoping within JavaScript. Expect students to be a little overwhelmed especially after learning about scope.

-   The slides will provide formal definitions, examples, and use cases that the students can refer back to. Also, think back to previous activities and show how you can refactor them to use closures.

### Assumptions

-   At this point, students should have a relative understanding of scope (local & global) as well as a firm grasp of callback functions, JavaScript objects, and for-loops.

## Learning Objectives

-   Understand how closures maintain and reference local scope variables.

-   Understand how closure functions interact with data at various scope levels and how they "remember" instantiated data.

## Slides

[JavaScript Closures](https://docs.google.com/presentation/d/1NsCVuBtyvZMqkGw824RcsK1XctRRw6zaq9BbHKpZsh0/edit?usp=sharing)

## Time Tracker

### 1. Instructor Do: Introduction to Closures - 5 min.

-   Give a gentle warning that the upcoming content is going to seem a bit odd at first but stress that it is a very important concept in the world of JavaScript programming. Students should understand the concept of scope from the previous activities. There is going to be some foreshadowing of object oriented programming concepts.

-   Go through the accompanying [slide deck](https://docs.google.com/presentation/d/1NsCVuBtyvZMqkGw824RcsK1XctRRw6zaq9BbHKpZsh0/edit?usp=sharing).

### 2. Instructor Do: Activity #1 - Intro to Closures - 5 min.

-   You are going to show the students a working example of a closure and outline the scope and syntax of a closure.

-   Use Chrome's DevTools to show that the browser categorizes the inner function as a "closure." Remember to use `console.dir()`.

### 3. Students Do: Activity #2 - Intro to Closures - 15 min.

-   Students will create a simple closure function that adds two numbers - one global, one local - and outputs them to the console.

-   Encourage them to use the previous activity, use `console.log` while building and testing their function, and work any errors output to the browser console.

### 4. Instructor Do: Review Activity #2 - Intro to Closures - 10 min.

-   Review the structure of a closure: function declaration, function instantiation, and function execution. Point out that the inner function and its return so that it can be used outside of the encapsulating function is what makes it a closure.

-   Feel free to mix it up by including other arithmetic closure functions (subtraction, multiplication, division, etc.).

### 5. Instructor Do: Activity #3 - Keep It Private - 5 min.

-   You are going to demonstrate how to keep an object's variables and methods private but still allow for outside interaction.

-   Inform the students that this is an important concept in object oriented programming and that you will circle back to this topic in the future.

### 6. Students Do: Activity #4 - Keep It Private - 15 min.

-   Students will create a simple payDay application that allows the user to make withdrawals, deposits, and view current balance.

-   Encourage the students to get creative with this application and use `console.log` thoroughly to view how each function affects the local scope variable.

### 7. Instructor Do: Review Activity #4 - Keep It Private - 10 min.

-   This activity is meant to emulate a class-based object found in object oriented programming. While `payDay` is a function, it contains properties and methods similar to an OOP object.

-   Point out the concept of "setters" and "getters" and how it interacts with the data. In short, the methods manipulate and return the data from within to prevent outside manipulation thus making the data private.

### 8. Instructor Do: Activity #5 - Closure Loop - 5 min.

-   Closures are commonly used with loops in order to "remember" the current state when the closure was first implemented.

-   Make sure to use `console.log` and `console.dir` to show what is happening "behind-the-scenes."

### 9. Students Do: Activity #6 - Closure Loop - 15 min.

-   Students will use a for-loop to store a closure function for each item in an array.

-   This activity closely mirrors the previous activity but uses an established dataset to create a more unique output.

### 10. Instructor Do: Review Activity #6 - Closure Loop - 10 min.

-   This activity demonstrates how closures capture the original data state at the time of invocation. The closure functions remember the value of `i` when it is added to the `funcArr` array. Thus, when it is subsequently called in the second for-loop, the closure function returns the value of `i` from its instantiation.

-   While abstract in its execution, point out how closures can be stored and used similar to other functions and data types.

### 11. Instructor Do: Review of Closures - 5 min.

-   Return to the [slide deck](https://docs.google.com/presentation/d/1NsCVuBtyvZMqkGw824RcsK1XctRRw6zaq9BbHKpZsh0/edit?usp=sharing).

-   Refer students to the supplemental resources.
