### 简介  
客户端（*client*，**客户端是命令的请求者**）将命令封装成命令对象（*command*，**命令对象持有接收者的引用，通过调用接收者的功能来完成命令的执行**），并给命令对象设置接收者（*receiver*，**接收者是真正执行命令的对象**），然后将命令对象交给调用者（*invoker*，**调用者可以持有多个命令对象，相当于命令对象的入口**），***以后 客户端 通过调用 调用者 来执行命令，而不与 命令对象 直接交互***（调用路径为：client =&gt;  invoker =&gt; command =&gt; receiver）  
可以看出，命令模式的主要目的是：将命令的请求者（client）和命令的执行者（receiver）进行解耦。解耦之后，可以*对请求进行排队*、*记录请求日志*、*撤销请求*等。  
比如，人操作空调的过程是：人在遥控器上输入开机、制冷、关机等命令；遥控器通过红外线把命令发送给空调，然后空调执行命令。很显然，人是client，每个功能都是一个command，遥控器是invoker，空调是receiver。需要额外注意的是，遥控器是命令的唯一入口，人只会与遥控器进行交互，而不会与空调直接交互，这就是命令模式中invoker的作用。

---

### 角色

* Client  
* Command
* ConcreteCommand  
* receiver  
* invoker  

---

### UML类图  

![command.png](http://timd.cn/content/images/2017/07/command.png)  
