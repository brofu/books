# Definition
** Facade Pattern** 提供了一个统一的接口，用来访问子系统中的一群接口。外观定义了一个高层接口，让子系统更容易的使用

# Class Diagram

# OO Principles

# Decorator v.s. Adapter v.s. Facade
| Item\Pattern | Decorator | Adaptor | Facade |
| :-- | :-- | :-- | :-- |
| Purpose | 扩展行为 | 转换接口 | 简化接口 |
| Behaviour | 解耦客户和被装饰者 | 解耦客户端和被适配者 | 解耦客户和组件的子系统 |


# Thinkings
* **Facade Pattern** 提供简化接口的同时，依然将系统完整的功能暴露出来.
* 通常情况下，外观会被指派给客户使用，而不需要由客户自行创造外观。
*
