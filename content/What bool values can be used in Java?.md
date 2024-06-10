jamesdanielmarrsritchey: What bool values can be used in Java?

GitHub Copilot: In Java, the boolean data type has two possible values: `true` and `false`. Here's an example of how you can use them:

```java
boolean isTrue = true;
boolean isFalse = false;
```

jamesdanielmarrsritchey: Is there any concept of null values in Java?

GitHub Copilot: Yes, in Java, `null` is a special value that represents the absence of a value or object instance. It is not the same as `false` or zero. It can be assigned to any reference type variables, but not to primitive types like `int`, `char`, or `boolean`. Here's an example:

```java
String str = null; // valid
int i = null; // invalid, will cause a compile error
```

jamesdanielmarrsritchey: Can you change the type reference of a variable?

GitHub Copilot: In Java, once a variable is declared, you cannot change its type. Java is a statically typed language, which means that the type of each variable is checked at compile-time. However, you can assign a new value of the same type to the variable. If you need a variable of a different type, you must declare a new variable. Here's an example:

```java
int num = 10; // num is of type int
num = "Hello"; // This will cause a compile error

String str = "Hello"; // str is of type String
str = 10; // This will cause a compile error
```

In the above example, trying to assign a `String` to an `int` variable or an `int` to a `String` variable will cause a compile error because the types are incompatible.