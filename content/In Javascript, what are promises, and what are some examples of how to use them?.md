jamesdanielmarrsritchey: In Javascript, what are promises, and what are some examples of how to use them?

GitHub Copilot: Promises in JavaScript are objects that represent the eventual completion (or failure) of an asynchronous operation, and its resulting value. They allow you to attach callbacks, instead of passing callbacks into a function. Here's a step-by-step explanation followed by examples:

### Explanation:
1. **Creating a Promise**: A new promise is created with the `new Promise()` constructor which takes a function (executor) that is called immediately with two arguments: `resolve` and `reject`. These are functions that, when called, resolve or reject the promise, respectively.
2. **Using a Promise**: Once a promise is created, it can be used by attaching callbacks using `.then()`, `.catch()`, and `.finally()` methods.
   - `.then()` is used to attach callback functions for the case when the promise is fulfilled.
   - `.catch()` is used to attach a callback function for the case when the promise is rejected.
   - `.finally()` is used to execute a callback function regardless of the promise's fate.
3. **Chaining Promises**: You can chain `.then()` calls to perform a sequence of asynchronous operations.

### Examples:

**Creating and Using a Promise:**

```javascript
// Creating a promise
let myPromise = new Promise((resolve, reject) => {
  let condition = true;
  if (condition) {
    resolve('Promise is resolved successfully.');
  } else {
    reject('Promise is rejected.');
  }
});

// Using the promise
myPromise
  .then((message) => {
    console.log(message); // Logs: Promise is resolved successfully.
  })
  .catch((message) => {
    console.log(message);
  });
```

**Chaining Promises:**

```javascript
function firstFunction() {
  return new Promise((resolve, reject) => {
    resolve('First function executed');
  });
}

function secondFunction(message) {
  return new Promise((resolve, reject) => {
    resolve(`${message}, then second function executed`);
  });
}

firstFunction()
  .then(result => secondFunction(result))
  .then(result => console.log(result))
  .catch(error => console.log(error));
// Logs: First function executed, then second function executed
```

**Async/Await Syntax for Promises:**

```javascript
async function asyncFunction() {
  try {
    const result = await firstFunction();
    console.log(result); // Logs: First function executed
    const finalResult = await secondFunction(result);
    console.log(finalResult); // Logs: First function executed, then second function executed
  } catch (error) {
    console.log(error);
  }
}

asyncFunction();
```

These examples demonstrate the basic usage of promises, chaining them for sequential asynchronous operations, and the modern `async/await` syntax for working with promises in a more synchronous-looking manner.