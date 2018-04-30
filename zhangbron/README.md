# 本笔记不在共同进度之内

*作者@棒棒*

## Week 1: 2018.04.30 ---- 2018.05.06

## 内容：监督学习：线性回归、逻辑回归、决策树、朴素贝叶斯



### *线性回归*

- 定义：给定一个点集，能够用一条曲线去拟合，如果这个曲线是直线，则称为线性回归
- 方法：最小二乘法、梯度下降法、岭回归、LASSO

#### 1. 最小二乘法

- 基于均方误差最小化获得参数估计结果

- 适用条件

  - 数据量比较少
  - 矩阵满秩满秩

  在满足上面两个条件时，通过矩阵运算可以较快得到解析解。

#### 2. 梯度下降

​	针对最小二乘法无法得到解析解的情况下，可以利用迭代法进行求解：梯度下降（一次逼近）、牛顿（二次逼近）

- 计算代价函数当前位置的梯度计算下一次参数更新的方向

- 梯度下降分类

  - 批量梯度下降(BGS)

    因为每一次的更新需要利用所有样本的数据进行计算，当数据量**很大**时，迭代速率**很慢**，当然它的迭代过程比较稳定

  - 随机梯度下降(SGD)

    每一次的更新仅利用某一个参数更新，计算速率**快**，但迭代过程比较**曲折**

  - 小批量梯度下降(MSGD) -- 两者的结合

    选取部分样本数据进行参数更新

  - Adagrad 

    前三种方法存在无法实现学习率动态变化的缺点

    Adagrad 利用历史的梯度信息作为学习率的分母实现学习率的动态变化，但是在**训练后期**，由于分母很大会使得学习率趋于0，学习速率**很慢**

#### 3. 岭回归(Ridge Regression)

​	其实是一种改良的最小二乘，抛弃了最小二乘的无偏性，以牺牲部分信息为代价获得回归系数，通过加一个L2正则项来约束代价函数，也就是对要估计的参数进行权衡(即权衡方差)

### 












