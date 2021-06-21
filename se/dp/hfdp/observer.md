# Definition
**Observer模式**在对象之间定义一对多的依赖，这样一来，当一个对象改变状态，依赖它的对象都会受到通知，并自动更新。

# OO原则
* 封装变化
  * 在Observer模式中，变化的是subject的状态，以及observer的数量和类型。用这个模式，可以改变依赖于主题状态的对象，却不必改变主题
* 多用组合，少用继承 (**has a** better than **is a**)
  * Observer模式利用**组合**将许多observers组合进subject中，对象之间的这种关系不是通过继承产生的，而是在运行时利用组合的方式产生的
* 针对接口编程，而不是实现
  * observer和subject都是用接口。observer利用subject接口向subject注册或者取消注册，subject利用observer接口通知observer.松耦合的优点
* 为交互对象之间的松耦合设计而努力

# Thinkings
* 一对多的关系
* 通过接口，实现松耦合(looscupling)
* Both **push** and **pull** from subject are OK, but **push** is considered better
