# Error handling in Egypt

以前发布过《[C语言的错误处理](551-C%E8%AF%AD%E8%A8%80%E4%B8%8B%E7%9A%84%E9%94%99%E8%AF%AF%E5%A4%84%E7%90%86%E7%9A%84%E9%97%AE%E9%A2%98.md)》一文，不过今天想说的是Egypt的“错误处理”。埃及的事闹得挺大的，国外和中文twitter上更是炸了锅。不要以为程序员就只会写程序——看看程序员举出来的标语吧。呵呵。

[![](https://coolshell.cn/uploads/2011/02/Error-handling-in-Egypt.jpg "Error handling in Egypt")](https://coolshell.cn/wp-content/uploads/2011/02/Error-handling-in-Egypt.jpg)

Error handling in Egypt

当然，作为程序员来说，这段代码显然还需要重构：  



```java
try{
    elections(free,fare);
} catch(DemocracyNotFoundException){
    System.err.println("Time for Mubarak to leave");
}
```

也有的程序员说，System.err.println不是处理错误的最好方法，正确的方法应该是：

```java
try {
    elections(free,fair);
} catch (DemocracyNotFoundException e) {
    throw new MubarakDepartureParty(e);
}
```

最后，我们希望Egypt不要出现：

```java
...
finally {
    Security.shootProtesters();
}
```

**（转载本站文章请注明作者和出处 [酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**
