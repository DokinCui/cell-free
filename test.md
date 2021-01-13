# Basis of CF-MIMO

## CF 背景
- 关于6G不得不说的事: 虽然目前还远远没有达到6G定义的统一阶段，但是综合各国专家的研究进展，可以预见未来6G将主要从以下3个维度采取变革性技术:
  - 去蜂窝（CF）网络架构
  - 太赫兹技术
  - 人工智能技术
  
- 关于cell不得不说的事：蜂窝网络架构是美国**贝尔**实验室在**20世纪70年代**提出的跨时代概念。它通过`频率复用`和`小区分裂`技术**提高频谱资源的利用率**，支撑移动通信快速发展。然而随着蜂窝小区面积不断缩小（比如微小区和超密集部署），`小区间干扰`和`频繁越区切换`等问题愈发严重导致系统性能提升遭遇瓶颈。为了解决这些瓶颈问题，对蜂窝网络架构进行彻底变革的去蜂窝网络架构成为人们关注的可行技术方案之一。

- 关于CF不得不提的概念：
  - 蜂窝通信：由于频谱资源有限，蜂窝通信采用频率复用的方式实现有限频谱资源对无限区域的覆盖。**多小区的频率复用，每个小区采用一组频带。因此，使用相同频段的小区之间必然存在同频干扰。**
  - MIMO的核心思想是在`同一时频资源`下，利用空间自由度，部署具有大型天线阵列的基站，同时为多个用户终端服务。然而，多天线同时放置在一起可能会导致`信道内的相关性`。为了应对这一重大的实现挑战，提出了 DAS。
  - 分布式天线系统（DAS）：蜂窝小区内多个基站地理位置上分离，通过高性能的回程链路进行协作对多个用户同时进行传输。
  - 多点协同传输（CoMP）：本质上是协同的DAS。
  - 网络 MIMO：又称为`虚拟 MIMO`、`分布式 MIMO`。文献 `Cooperative multicell precoding: Rate region characterization and distributed strategies with instantaneous and statistical CSI` 介绍的模型。分布式基站协作的情况，其中每个基站只有本地CSI。通过协同基站在回程链路上共享重要数据，并联合下行传输给预定用户来实现干扰消除。CF系统与其类似。
  - CF：与CoMP设置相同，但没有`小区边界`的概念。（思考：小区边界意味着蜂窝通信的`频率复用`以及`小区间干扰`等特点存在。）上述的系统都存在**簇间干扰与交互开销**的问题。
  - Cell-free massive MIMO is a recent concept that conveniently combines elements from 
    - small cells
    - **TDD massive MIMO**
    - **user-centric** joint transmission coordinated multi-point (JT-CoMP)
  - > 因此，可以说 CF 就是大区域扩展的JT-CoMP，学术大佬也这样说：CF就是 **user-centric** JT-CoMP！



## 一些回答

> Cell-free MIMO is a new name for network MIMO and distributed MIMO. One purpose for the renaming is to impose new assumptions on how the system should operate to be practically implementable. You can think of it as Network MIMO 2.0.
