# Definition
**Adaptor Pattern**将一个类的接口，转换成客户期望的另一个接口。让原本接口不兼容的类可以合作无间

# Class Diagram
![adaptor-object][adaptor-object]
<center>Adaptor Pattern - Object</center>

![adaptor-class][adaptor-class]
<center>Adaptor Pattern - Class</center>

# Decorator v.s. Adapter
| Item\Pattern | Decorator | Adaptor |
| :-- | :-- | :-- |
| Purpose | 扩展行为 | 转换接口 |
| Behaviour | 解耦客户和被装饰者 | 解耦客户端和被适配者 |

# Thinkings
* **Adaptor Pattern** decouple `client` and `adaptee`
* **Object Adaptor** v.s. **Class Adaptor**
  * The `adaptor` **implements** the `target interface`, and delegate the request to the `adaptee`. **The `adaptor` combine an `adaptee`**
  * The `adaptor` **inherit** the `targe interface` and the `adaptee`
* Examples in Java:
  * collection v.s. Iterator


[adaptor-object]: imgs/formal/adaptor-object.png
[adaptor-class]: imgs/formal/adaptor-class.png
