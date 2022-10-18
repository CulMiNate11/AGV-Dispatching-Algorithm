# AGV-Dispatching-Algorithm
This is one of the algorithms I have implemented individually in the 2022 surf project in XJTLU

![image](https://user-images.githubusercontent.com/99118599/196332314-6f45530f-34d5-430e-a57a-92c544ed0878.png)
![image](https://user-images.githubusercontent.com/99118599/196332595-d5e983cf-1d46-4666-8133-c80ebab657d6.png)

此AGV调度算法的目标是在指定原点向多条路径进行调度AGV派送任务。
如何用更快、成本更小地调度AGV？ 当变量足够多、情况足够复杂时, 很难从数学的角度找到一个通式或是最优解。主要探讨AGV调度算法的两种模式——basic模式和handover模式。
![image](https://user-images.githubusercontent.com/99118599/196332739-08f6f593-f916-4e2b-9326-d895139383ba.png)


Basic模式
Basic模式指在一条路径上仅用一辆AGV进行调度,  是一种最简单的模式并且可以根据参数给出一个普遍的数学公式求解系统的运行时间：

 ![image](https://user-images.githubusercontent.com/99118599/196332779-b57dce8b-f5b3-4d63-ba99-f071130b003f.png)

并且可由此得到AGV运动总距离：

 ![image](https://user-images.githubusercontent.com/99118599/196332798-b8a9cda9-16c9-4ddb-8a64-84930571db88.png)


Handover模式
Handover模式指对任意路径的AGV调度数量无上限, 且在路径上的碰撞认定为任务的交接。交接完成后运行方向改变。
在现实中根据任务不同, 交接时间也不相同。当然, 本文主要讨论给定条件与参数的Handover模式, 只需要考虑交接时间平均值, 即交接时间固定. 以后研究实时AGV调度时,会考虑灵活交接时间的Handover情况。
当变量足够多，情况足够复杂时，很难得到一个普遍的数学公式。
首先从交接时间为0的理想情况入手, 此模式称为理想Handover模式。
理想Handover模式为Handover模式的极限情况。

理想Handover模式的特例
在理想情况下, 当系统有足够数量的AGV，满足为可连续派发AGV的特例时, 可给出一个数学公式计算系统运行时间：

![image](https://user-images.githubusercontent.com/99118599/196332853-9ade0f38-7bf1-4c33-bad0-384391625f20.png)

可用归纳法证明。

下面给出1-path Handover模式的单一变量研究

![ac42cd41519d2ab20490a409e5dd7c6](https://user-images.githubusercontent.com/99118599/196333373-1106a4e4-7886-4e05-b55b-3fe38392d3b3.jpg)


