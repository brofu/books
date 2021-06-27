
# Definition
**Singleton Pattern** guarantee that there is ONLY 1 instance for a class, and provide a global access to this instance

# URL Graph
![sing][sing]

# Code 
```
// version 1
public class Singleton {
  private static Singleton uniqueInstance;

  // other attributes…

  private Singleton () {}
  public static synchronized Singleton getInsatnce() { // Q1
    if (uniqueInstance == nil) {
      uniqueInstance = new Singleton();
    }
    return uniqueInstance;
  }

  // other methods...
}


// version 2
public class Singleton {
  private static Singleton uniqueInstance = new Singleton(); 
  // other attributes...

  private Singleton () {}

  public static Singleton getInsatnce() { 
    return uniqueInstance;
  }

  // other methods...
}

// version 3
public class Singleton {
  private volatile static Singleton uniqueInstance;  // Q2

  // other attributes…

  private Singleton () {}

  public static Singleton getInsatnce() { 
    if (uniqueInstance == nil) {
      synchronized (Singleton.class) { 
        if (uniqueInstance == nil) {
          uniqueInstance = new Singleton();
        }
      }
    }
    return uniqueInstance;
  }

  // other methods...
}
```

* Q1. What's the problem of `synchronized`? Performance
* How to resolve? 
  * If performance is NOT a key point.
  * Eagerly initialize in **static initializer** ==> version 2 (JVM create the instance immediately when load the class)
  * **Double-checked Locking** ==> version 3
* Q2. What if `uniqueInstance` is declared without `volatile`? JVM指令无序性问题 [1][1]
  * JVM 并发内存模型[2][2]
  * CAS [3][3]

# Thinkings
* **Constructor** is **private**.
* **Static variable** `uniqueInstance` is provided to hold the instance
* **Static method** `getInstance()` is provided for global access. It's actually class method. Lazy instance is supported with this.
* **Double-Checked Locking** only work after java 1.5 and afterwards versions.
* Multiple class loader?
* Inheritance Singleton?
  * Constructor is **private**.
  * 单例的实现是利用静态变量。直接继承会导致多个派生类共享此变量

[sing]: imgs/formal/singleton.png
[1]: https://blog.csdn.net/anjxue/article/details/51038466?utm_medium=distribute.pc_feed_404.none-task-blog-2~default~BlogCommendFromBaidu~default-3.nonecase&depth_1-utm_source=distribute.pc_feed_404.none-task-blog-2~default~BlogCommendFromBaidu~default-3.nonecas
[2]: https://www.cnblogs.com/dolphin0520/p/3920373.html
[3]: https://zh.wikipedia.org/wiki/%E6%AF%94%E8%BE%83%E5%B9%B6%E4%BA%A4%E6%8D%A2#cite_note-11
