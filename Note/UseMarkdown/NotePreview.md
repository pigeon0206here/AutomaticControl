# 预习笔记
## 胡寿松版
### 自动控制的一般概念
#### 基本原理与方法
##### 这一段在阐释自动控制在现代社会活动中的重要存在意义
##### 在讲解自动控制技术这一门学科的发展历史。
1. 最早可追溯到我国的漏壶指南车等
2. 20世纪10年代PID控制器就被发明出来了。
3. 1927年反馈放大器诞生，“反馈”在控制技术中的核心地位被确立。
4. 20世纪40年代，贝塔朗菲提出《系统论》，维纳提出《控制论》。完整的控制理论体系形成。
   > 以传递函数为基础的经典控制理论，主要研究单输入单输出、线性定常系统的分析和设计问题。
5. 20世纪60年代，第二代控制理论诞生。
   - 现代控制论
   > 包括以状态为基础的状态空间法、贝尔曼的动态规划法和庞特里亚金的极小值原理，以及卡尔曼滤波器。
   > 现代控制理论主要研究具有高性能、高精度和多耦合回路的多变量系统的分析和设计问题。
6. 20世纪70年代以来，计算机控制的自动化控制技术逐渐发展。
   - 自动控制科学分支：自适应控制、混杂控制、模糊控制、神经网络控制
   - 控制理论的应用多元化
##### 在介绍反馈控制的重要性以及原理
1. 自动控制系统定义：把被控对象和控制装置以一定方式连接在一起。
  
   ```mermaid
   graph TD 

   A["控制装置"] --> |"以一定方式连接到"|B["被控对象"]
   A --> C[是对被控对象施加控制作用的机构的总体]

   

   B --> D
   E[某一恒定值,如温度/压力等]
   D(("被控对象
   的输出
   （物理量）")) -->|包括| E[某一恒定值,如温度/压力等]
   D --> |要求| G[按照某一给定规律运行,如飞行航线/记录曲线]

   ```
    >mermaid使用介绍（csdn版）：[mermaid绘制流程图介绍](https://blog.csdn.net/anzaigongzi/article/details/127993874?spm=1001.2014.3001.5502)

`要先去试试用LaTeX产出笔记啦，之后要画流程图/思维导图梳理的话再来这边了！`

手取书流程：

```mermaid
graph TD
A["输入信号（书位置）"] -->B["眼睛👀"]
B -->C["大脑🧠"]
C -->D["手✋"]
D -->E["输出量（手的位置）"]
E -->B["眼睛👀"]
E -->F["最终实现手与书的偏差为0，成功拿到书本"]
```


  