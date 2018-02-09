# 🎮 js实现2048小游戏。 🎮

## 1、游戏简介

2048是一款休闲益智类的数字叠加小游戏。

## 2、游戏玩法

在 4*4 的16宫格中，您可以选择上、下、左、右四个方向进行操作，数字会按方向移动，相邻的两个数字相同就会合并，组成更大的数字，每次移动或合并后会自动增加一个数字。

当16宫格中没有空格子，且四个方向都无法操作时，游戏结束。 

## 3、游戏目的

目的是合并出 2048 这个数字，获得更高的分数。

## 4、游戏截图

![](https://raw.githubusercontent.com/nnngu/FigureBed/master/2018/2/9/Snip20180209_1.png)

## 5、游戏实现原理

(1)首先，把16宫格看成是矩阵的形式

![](https://raw.githubusercontent.com/nnngu/FigureBed/master/2018/2/9/Snip20180209_2.png)

(2)在html中给每个格子添加类名及属性，来记录每个格子的位置

![](https://raw.githubusercontent.com/nnngu/FigureBed/master/2018/2/9/Snip20180209_4.png)

注：类名`item`是每个格子的类名，`emptyItem`是空格子的类名，`nonEmptyItem`是非空格子的类名。

(3)游戏开始时，随机生成两个数字，2或者4，出现在矩阵中任意位置
   
![](https://raw.githubusercontent.com/nnngu/FigureBed/master/2018/2/9/Snip20180209_5.png)

这部分是通过类名`emptyItem`及`nonEmptyItem`来实现的。

步骤：

①. 随机生成一个数字2或者4

②. 获取所有空元素（类名`emptyItem`）

③. 随机选择一个空元素，将生成的数字填充到空元素中，并将类名`emptyItem`移除，添加类名`nonEmptyItem`，即非空元素

④. 重复①、②、③步，再随机生成一个数字填充到随机的位置。



