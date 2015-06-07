# try-with resources

Prior to Java 7, whenever we have to do a cleanup, we used to put the code in try block and add a finally block that would close unnecessary resources.
something like this

```java```

BufferedReader br = new BufferedReader(new FileReader("path to file"));
try{
  return br.readline();
}finally{
  if(br!=null) br.close();
}

```
Java 7 has come up with, what you can call as a, shorthand to the above scenario **try-with-resources** statement

**try-with-resources** statement is a try statement that declares one or more resources. The try-with-resources statement ensures that each resource is closed after the statement.

> Any object that implements ```java.lang.AutoCloseable``` , which includes all objects which implement ```java.lang.Cloaseable```, can be used as a resource.

This is how you'll write the above code using try-with-resources statement

```java```

try(
  BufferedReader br = new BufferedReader(new FileReader("path to file"))
  ){
  return br.readline();
}
```

You can add as many declarations inside the try-with-resources statement.
