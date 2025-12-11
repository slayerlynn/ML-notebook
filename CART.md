# CART 决策树模型

## 1. 基本概念
CART(CLASSIFICATION AND REGRESSION TREE)是一种二叉树模型,是有监督的机器学习模型，对于分类和回归两种任务，通过解决最优化问题如MSE、基尼系数、信息增益和信息增益比来实现数据的划分和预测。
- 分类树
  给定特征 𝑋，预测类别标签 𝑦，如（是/否，高/中/低）等标签。
  损失函数主要使用**基尼系数**或**信息增量**。
  
  $$
  Gini = 1 - \sum p_k^2
  $$

  $$
  Gain(D, A) = Entropy(D) - \sum_{v=1}^{V} \frac{|D_v|}{|D|} Entropy(D_v)
  $$
  
- 回归树
  给定特征*X*,预测连续变量*y*。
  损失函数主要使用**MSE**。

$$
MSE=\frac{1}{V} \sum_{v=1}^{V}(y_v-\hat{y}_v)^2
$$

## 2. 损失函数
- 基尼系数（二分类）

$$
Gini = 1 - \sum p_k^2
$$

GAIN = 
- sigmoid(二分类）

  Sigmoid函数（逻辑回归激活函数）

$$p(x) = \sigma(f(x)) = \frac{1}{1 + e^{-f(x)}}$$
  
  损失函数:

  $$L(y,f(x)) = -[y\log(p)+(1-y)\log(1-p)] $$

  对f(x)求一阶梯度后:

  $$\frac{\alpha L(y,f(x))}{\alpha f(x)}$$


- MSE（回归）

$$
MSE=\frac{1}{V} \sum_{v=1}^{V}(y_v-\hat{y}_v)^2
$$
  
- 交叉熵+softmax(多分类）
  

## 3. 构建流程
1. 选择最优划分点
2. 递归生成子树
3. 剪枝优化


