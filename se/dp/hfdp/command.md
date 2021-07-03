# Definition
**命令模式** 将”请求“封装成对象，以便使用不同的请求，队列或者日志来参数化其它对象。也可支持撤销操作

# Class Diagram
![cmd][cmd]
<center>Command Pattern</center>

# Thinkings
* `Null Object` pattern
* **命令模式** 将发出请求的对象和执行请求的对象解耦。两者之间通过Command对象沟通。Command对象封装了动作接收者和一个/一组动作
* **命令模式** 更多应用
  * Command队列
  * Command log

[cmd]:imgs/formal/cmd.png
