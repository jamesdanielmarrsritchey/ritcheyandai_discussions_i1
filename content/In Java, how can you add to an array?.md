jamesdanielmarrsritchey: In Java, how can you add to an array?

GitHub Copilot: In Java, arrays are fixed in size. Once they are created, they cannot be resized. If you need to add an element to an array, you have to create a new array with a larger size and copy the elements from the old array to the new one. Here's an example:

```java
int[] oldArray = {1, 2, 3};
int[] newArray = new int[oldArray.length + 1];

// Copy old array to new array
System.arraycopy(oldArray, 0, newArray, 0, oldArray.length);

// Add new element
newArray[newArray.length - 1] = 4; // Now newArray is {1, 2, 3, 4}
```

However, if you find yourself needing to add elements to an array frequently, you might want to consider using a dynamic data structure like `ArrayList` which can grow and shrink in size as needed.

```java
ArrayList<Integer> list = new ArrayList<Integer>();
list.add(1);
list.add(2);
list.add(3);
list.add(4); // Now list is [1, 2, 3, 4]
```

jamesdanielmarrsritchey: How to create an array list of bools?

GitHub Copilot: In Java, you can create an `ArrayList` of `Boolean` objects like this:

```java
ArrayList<Boolean> boolList = new ArrayList<Boolean>();
```

You can then add `Boolean` values to the list like this:

```java
boolList.add(true);
boolList.add(false);
```

Now `boolList` contains `[true, false]`.