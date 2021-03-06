### 简介  

*在工厂方法模式中，所有的 具体产品类 都有一个共同的父类*。而在**抽象工厂**模式中，引入了**产品族**的概念，所谓产品族就是：**在不同的产品等级结构中，功能相关联的产品组成的家族**。<span style="color:green">***每个产品族都对应一个具体工厂***</span>。  
所以工厂方法模式 和 抽象工厂模式的区别就是：如果工厂的产品来自多个等级结构，就是抽象工厂模式；如果来自同一个等级结构，就是工厂方法模式。  

---

### 角色  
 
* 抽象工厂    
封装类中不易变的部分，并注入给具体产品类的对象，但是并不负责具体产品类对象的创建  
* 具体工厂    
继承或实现抽象工厂角色。负责创建具体产品类的对象  
* 抽象产品    
为所有的产品类提供共同的接口  
* 具体产品类    
继承或实现抽象产品角色。它是被创建对象的类  

---

### UML类图  
 
![abstract-factory.png](http://timd.cn/content/images/pictures/abstract-factory.png)
  
