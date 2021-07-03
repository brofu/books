# Definition
**Adaptor Pattern**将一个类的接口，转换成客户期望的另一个接口。让原本接口不兼容的类可以合作无间

# Class Diagram

# Decorator v.s. Adapter

# Thinkings
* **Adaptor Pattern** decouple `client` and `adaptee`
* **Object Adaptor** v.s. **Class Adaptor**
  * The `adaptor` **implements** the `target interface`, and delegate the request to the `adaptee`. **The `adaptor` combine an `adaptee`**
  * The `adaptor` **inherit** the `targe interface` and the `adaptee`

