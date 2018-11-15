### finally
```java
  try {
//            something();
      return 111;
  }
  catch (Exception e) {
      return 222;
  }
  finally {
      System.out.println(333);
  }
```
>打印结果：
333
111
