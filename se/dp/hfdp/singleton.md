
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
  public static synchronize Singleton getInsatnce() { // Q1
    if (uniqueInstance == nil) {
      uniqueInstance = new Singleton();
    }
    return uniqueInstance;
  }

  // other methods...
}


// version 2
public class Singleton {
  private static Singleton uniqueInstance = new Singleton(); // Q2

  // other attributes...

  private Singleton () {}

  public static Singleton getInsatnce() { 
    return uniqueInstance;
  }

  // other methods...
}

// version 3
public class Singleton {
  private volatitle static Singleton uniqueInstance;  // Q3

  // other attributes…

  private Singleton () {}

  public static synchronize Singleton getInsatnce() { 
    if (uniqueInstance == nil) {
      synchronized (Singleton.class) { // Q4
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
# Thinkings
* Construct method is **private** 
* Static method `getInstance()` is provided for global access. It's actually class method. Lazy instance is supported with this.
*

[sing]: imgs/formal/singleton.png
