ML
sklearn
转化器(Transformer)
fit(x,y) :该方法接受输入和标签，计算出数据变换的方式。
transform(x) :根据已经计算出的变换方式，返回对输入数据x变换后的结果（不改变x）
fit_transform(x,y) :该方法在计算出数据变换方式之后对输入x就地转换。

1.scaling data 缩放数据
Standardization标准化  Normalization归一化 
standard deviation 标准偏差
￼
2. data preprocessing template (import libraries, import dataSet, splitting dataSet into Train/Test,[feature scaling])

二. Regression models 回归
1.Simple Linear Regression 简单线性回归
coefficient 系数
2.Mutiple Linear Regression 简单线性回归
￼
Assumptions of Linear Regression
1. Linearity 线性
2. Homoscedasticity 同方差
3. Multivariate normality 多元正态性 -多因素共同影响分布结果
4. Independence of errors 错误的独立性 -每一个变量产生的错误将会独立的影响预测结果，不会对其他变量产生影响
5. Lack of multicollinearity 多重共线性的缺乏-变量之间存在高度相关关系而使得回归估算不准确，如接下来要提到的虚拟变量陷阱（dummy variable trap）有可能触发多重共线性的问题

** Dummy variable 虚拟变量/哑变量
陷阱（线性相关影响线性回归）：如果D1，D2都写，因为D1= 1 - D2，这使得导致解的数量有无数种，你所以你计算出来的系数本身就不太可能是正确的那个系数，误差也显然会变大。
P-value
https://www.jianshu.com/p/4c9b49878f3d 
P-value的临界值0.05，即错误拒绝假设H0的概率，计算出chi-square当值并查找卡方分布表，
当对应p-value的值>0.05:H0成立
当对应p-value的值<0.05:H1成立
大部分时候p-value用于检验独立变量与输入变量的关系，H0假设通常为假设两者没有关系
当p值小于0.05时，我们就说这个独立变量重要（significant），因为这个独立变量与输出结果有关系。

3.Build a mode 建立模型
1. All-in（将所有自变量都考虑进去）
2. Backward Elimination 反向淘汰
3. Forward Selection 顺向选择
4. Bidirectional Elimination 双向淘汰
5. Score Comparison 信息量比较
https://www.jianshu.com/p/65ca62f4ce72
2，3，4是stepwise regression

Backward Elimination
￼

Forward Selection
￼

Bidirectional Elimination
￼
