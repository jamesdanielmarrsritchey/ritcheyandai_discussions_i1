jamesdanielmarrsritchey: How do you create a string in Javascript?

GitHub Copilot: In JavaScript, you can create a string in three ways:

1. Using double quotes: `"Hello, World!"`
2. Using single quotes: `'Hello, World!'`
3. Using backticks (template literals): `` `Hello, World!` ``

Here's an example:

```javascript
let str1 = "Hello, World!";
let str2 = 'Hello, World!';
let str3 = `Hello, World!`;
```

Each of these variables (`str1`, `str2`, `str3`) now holds a string.

jamesdanielmarrsritchey: What are some common string methods in JavaScript?

GitHub Copilot: Here are some common string methods in JavaScript:

1. `charAt(index)`: Returns the character at the specified index.
2. `concat(string2, string3, ..., stringX)`: Joins two or more strings, and returns a new joined strings.
3. `includes(searchvalue, start)`: Checks whether a string contains the specified string/characters.
4. `indexOf(searchvalue, start)`: Returns the position of the first found occurrence of a specified value in a string.
5. `slice(start, end)`: Extracts a part of a string and returns the extracted part in a new string.
6. `split(separator, limit)`: Splits a string into an array of substrings.
7. `toLowerCase()`: Converts a string to lowercase letters.
8. `toUpperCase()`: Converts a string to uppercase letters.
9. `trim()`: Removes whitespace from both ends of a string.

Here's an example of how you might use some of these:

```javascript
let str = "Hello, World!";

console.log(str.charAt(0)); // "H"
console.log(str.concat(" How are you?")); // "Hello, World! How are you?"
console.log(str.includes("World")); // true
console.log(str.indexOf("World")); // 7
console.log(str.slice(0, 5)); // "Hello"
console.log(str.split(",")); // ["Hello", " World!"]
console.log(str.toLowerCase()); // "hello, world!"
console.log(str.toUpperCase()); // "HELLO, WORLD!"
console.log("   Hello, World!  ".trim()); // "Hello, World!"
```