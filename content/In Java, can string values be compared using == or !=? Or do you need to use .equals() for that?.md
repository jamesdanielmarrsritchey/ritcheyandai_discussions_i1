jamesdanielmarrsritchey: In Java, can string values be compared using == or !=? Or do you need to use .equals() for that?

GitHub Copilot: In Java, you should use `.equals()` to compare the contents of two Strings. The `==` and `!=` operators compare the references, not the actual values. If you use `==` or `!=` to compare strings, you're checking to see if they point to the exact same object, not whether they have the same value.

Here's an example:

```java
String str1 = new String("Hello");
String str2 = new String("Hello");

// This will print "false" because str1 and str2 reference different objects
System.out.println(str1 == str2);

// This will print "true" because str1 and str2 contain the same characters in the same order
System.out.println(str1.equals(str2));
```

So, always use `.equals()` when you want to compare the actual contents of the strings.