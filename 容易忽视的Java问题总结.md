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

> finally will be called after the execution of the try or catch code blocks.
The only times finally won't be called are:

1. If you invoke System.exit();
2. If the JVM crashes first;
3. If the JVM reaches an infinite loop (or some other non-interruptable, non-terminating statement) in the try or catch block;
4. If the OS forcibly terminates the JVM process; e.g. "kill -9 " on UNIX.
5. If the host system dies; e.g. power failure, hardware error, OS panic, etcetera.
6. If finally block is going to be executed by daemon thread and all other non daemon threads exit before finally is called.
