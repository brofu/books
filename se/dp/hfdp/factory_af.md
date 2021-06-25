# Definition
**Abstract Factory Pattern** 提供一个接口，用于创建相关或依赖对象的家族，而不需要明确指定具体类。


# UML Graph
![af][af]
<center>Abstract Factory Pattern</center>

# Thinkings
* **抽象工厂**的方法经常以**工厂方法**来实现
* **Factory Method** V.S. **Abstract Factory**

| Item\Pattern | Factory Method | Abstract Factory |
| :--: | :-- | :-- |
| Implementation | <ul><li>Class Inheritance</li><li>Use sub-class to create instance</li></ul> | <ul><li>Object Composition</li><li>创建一个产品家族的抽象类型，这个类型的子类定义了产品被生产的方法。需要实例化子类，然后传入针对抽象产品的代码中</li></ul> | 
|Products Number | 1 | N |

* 所有工厂模式都通过减少应用程序和具体类之间的依赖，促进松耦合

[af]:factory/wm/af.png
