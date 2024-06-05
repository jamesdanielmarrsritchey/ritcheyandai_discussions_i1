jamesdanielmarrsritchey: What are some common mistakes in Javascript writing?

GitHub Copilot: 1. **Not Using '===' for Comparison**: JavaScript has two types of equality operators: `==` and `===`. The `==` operator performs type coercion, meaning that it converts the operands to the same type before making the comparison. On the other hand, `===` (strict equality) does not perform type coercion.

    ```javascript
    0 == false   // true
    0 === false  // false, because they are of a different type
    ```

2. **Not Declaring Variables**: If you assign a value to a variable that has not been declared, it will automatically become a GLOBAL variable. This can lead to unexpected results.

    ```javascript
    x = 5; // x is a global variable now
    ```

3. **Not Using Semicolons**: JavaScript does automatic semicolon insertion, but it's considered good practice to always include them to avoid unexpected results.

    ```javascript
    let x = 3
    let y = 4
    // should be
    let x = 3;
    let y = 4;
    ```

4. **Not Understanding Hoisting**: In JavaScript, variables and function declarations are moved to the top of their containing scope during the compile phase, this is known as "hoisting". Not understanding this can lead to unexpected results.

    ```javascript
    console.log(x); // undefined
    var x = 5;
    ```

5. **Mutating Objects Passed as Function Arguments**: JavaScript objects are passed by reference, not by value. If a function changes an object property, it changes the original value.

    ```javascript
    function change(obj) {
      obj.prop1 = function() {};
      obj.newProp = true;
    }
    var obj = { prop1: {} };
    change(obj);
    console.log(obj); // { prop1: [Function], newProp: true }
    ```

6. **Not Understanding Event Delegation**: Event delegation is a technique involving adding event listeners to a parent element instead of adding them to the descendant elements. The listener will fire whenever the event is triggered on the descendant elements due to event bubbling up the DOM.

7. **Not Understanding Closures**: A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In JavaScript, closures are created every time a function is created, at function creation time. Not understanding how closures work can lead to unexpected results.

8. **Not Handling Asynchronous Code Properly**: JavaScript is single-threaded, but it can handle tasks asynchronously using callbacks, promises, and async/await. Not handling asynchronous code properly can lead to callback hell or unhandled promise rejections.

9. **Not Using Array and Object Destructuring**: Destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables. This can make your code more readable and understandable.

10. **Not Using Template Literals**: Template literals are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them. They were called "template strings" in prior editions of the ES2015 specification.