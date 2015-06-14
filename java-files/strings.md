## String is interned
```java```
String str0 = "yes",
str3 = "yes";
```
Because the underlying strings are identical, only one String object is constructed, and both str0 and str3 are references to that object. In such cases, we say that the String object has been **interned** .

