### 线性模型 ###
#### 约束 ####
1、行向量 (x1,x2,x3,……)<br>
2、列向量 (y1;y2;y3;……)<br>
#### 3.1 基本形式 ####
&emsp;f(x) = w<sub>1</sub>x<sub>1</sub>+w<sub>2</sub>x<sub>2</sub>+……+w<sub>d</sub>x<sub>d</sub>+b <br>
一般写成：<br>
&emsp;f(x) = W<sup>T</sup>X+b
#### 3.2 线性回归 ####
&emsp;线性回归试图学的一个线性模型以准确的预测实值输出标记<br>
对于离散属性：<br>
&emsp;若存在序的关系：连续化转化为连续值：{高，矮} => {1.0,0.5}<br>
&emsp;不存在序的关系：转化为k维向量：{西瓜，冬瓜，南瓜} =>{(1,0,0),(0,1,0),(0,0,1)} <br>
线性模型试图学的：f(xi) =wxi+b => f(x<sub>i</sub>)≈y<sub>i</sub><br>
如何确定w和b：<br>
&emsp;均方误差最小化<br>
&emsp;(w*,b*) = argmin∑(f(xi)-yi)<sup>2</sup>=argmin∑(yi-wxi-b)<sup>2</sup>
&emsp;求解w和b使得误差最小化的过程称为最小二乘法<br>
&emsp;∂E/∂w = 2(w∑xi2-∑(yi-b)xi)<br>
&emsp;∂E/∂b = 2(mb-∑(yi-wxi)<br>
写成向量形式<br>
&emsp;w* = argmin(y-XW)<sup>T</sup>(y-XW)<br>
&emsp;当XTX为满秩矩阵或者正定矩阵时<br>
&emsp;W* = (X<sup>T</sup>X)<sup>-1</sup>X<sup>T</sup>y<br>
&emsp;如果不满足时，则可能求出多组解，选择那一组解作为输出，则由算法的归纳偏好决定，常见做法是引入正则化<br>
广义线性模型：<br>
&emsp;y=g<sup>-1</sup>(w<sup>T</sup>x+b)<br>
&emsp;当g(.)=ln(.)时为对数线性回归
#### 3.3对数几率回归 ####
单位阶跃函数：
$$y=\begin{cases}
0 & z<0 \\
0.5 & z=0 \\
1 & z>0
\end{cases}$$

