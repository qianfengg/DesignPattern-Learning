# 设计模式学习

## 参考资料

* [常用设计模式有哪些](https://refactoringguru.cn/design-patterns)

## 白话解释各案例

* 1-工厂模式
  * 利用抽象汉堡工厂制造汉堡(开放封闭原则用这个案例很好理解，因为普通工厂就是不封闭)！！

* 2-单例模式
  * 登录框有且只有一个可以使用单例！！  

* 3-适配器模式 - 为被封装对象提供不同的接口
  * 有个圆孔，可以放入圆柱体，什么？还可以放入立方体(只要对角线的一半小于等于圆孔半径就可以啦)？

* 4-装饰器模式 - 为对象提供加强的接口，ES7有装饰器语法
  * 有些猫在叫之前还要先卖萌，那我们就装饰器模式额外增加这个功能！！
  
* 5-代理模式 - 为对象提供缩减版的接口，代理嘛，就是有的东西不想让你直接用
  * 事件代理: ul下多个li添加点击事件，为什么不交给ul一个元素去处理呢?
  * 虚拟代理(对象提供相同的接口): 图片预加载，ProxyImage帮我们调度了预加载相关的工作！！
  * 缓存代理: 计算量较大的场景里，我们需要“用空间换时间”，比如我们已经计算过1+2+3，下次再计算的时候可以直接从缓存里取~不用再次计算！！
  * 保护代理(对象提供相同的接口): ES6中的Proxy登场，保护女孩的隐私吧！！

* 6-外观模式 - 不符合单一职责原则和开放封闭原则，谨慎使用
  * 随机数 - 可以传入一个参数(子系统，0到该数范围随机)，可以传入2个参数(a<b, 子系统，a到b范围随机)， 也可以这样传2个参数(a>b, 子系统，b到a范围随机)，提供一个函数，使用外观模式，实现上述功能
  
* 7-观察者模式 - 发布订阅模式(这2种模式是有区别的)
  * 观察者模式： 产品把前端后端测试拉了个群，然后发了个需求，然后你们懂的~注意这里的产品和前端后端测试是直接联系的！！
  * 发布订阅模式： 产品把需求丢到了公司管理项目的平台上，前端后端测试通过平台就知道要干什么了~注意这里产品就不直接和前后端测试沟通(解耦)，通过第三方平台！！
  * 发布订阅模式： 大家可以根据上述例子，脑补第三方平台是直播平台，主播和粉丝肯定是通过平台实现订阅发布的！！

* 8-迭代器模式 - 就是为了遍历
  * 排队等号，下一位,下一位....直到迭代到最后，所有人都进场了！！
  
* 9-状态模式
  * 一台咖啡机的故事
    - 美式咖啡态（american)：只吐黑咖啡
    - 普通拿铁态(latte)：黑咖啡加点奶
    - 香草拿铁态（vanillaLatte）：黑咖啡加点奶再加香草糖浆
    - 摩卡咖啡态(mocha)：黑咖啡加点奶再加点巧克力

* 10-原型模式
  * 细胞有丝分裂 （还记得生物学知识吗？） 或许是恰当的类比。 有丝分裂会产生一对完全相同的细胞。 原始细胞就是一个原型， 它在复制体的生成过程中起到了推动作用。

* 11-桥接模式
  * 我们要做一个有不同颜色也有不同形状的模具
  * 先做了这样的设计
    * 最大的父类为shape
    * 其有2个子类，分别继承它，一个正方形，一个圆形
    * 然后我们有2种颜色，比如红色和黄色，那接下去的操作就厉害了
    * 红色正方形，黄色正方形继承正方形，红色圆形，黄色圆形继承圆形
    * 此时我们在扩展加一种颜色或者加一个形状，代码就变得非常的复杂
  * 桥接模式登场
    * 形状归形状，颜色归颜色，最后在汇总        
