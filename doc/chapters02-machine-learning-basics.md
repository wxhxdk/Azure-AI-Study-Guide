# 第2章 Machine Learning 基础

> 本章对应 AI-901 学习路线中的第 2 章，重点理解 Machine Learning 的基本概念、监督学习与无监督学习、Regression、Classification、Clustering，以及 Features、Labels 和模型训练、验证、测试与评估的完整流程。

---

# 0. AI-901 考试介绍

## 0.1 本章学习定位

Machine Learning（机器学习）是 Artificial Intelligence 的重要组成部分。

在第 1 章中，我们已经学习：

```text
Artificial Intelligence
        ↓
Machine Learning
        ↓
Deep Learning
```

本章进一步学习 Machine Learning 的核心知识。

重点理解：

```text
数据
 ↓
Features / Labels
 ↓
Training
 ↓
Validation
 ↓
Testing
 ↓
Model Evaluation
```

以及不同类型的 Machine Learning：

```text
Machine Learning
│
├── Supervised Learning
│   ├── Regression
│   └── Classification
│
└── Unsupervised Learning
    └── Clustering
```

---

# 1. 本章学习目标

学习完本章后，你应该能够：

* 理解 Machine Learning 的基本概念
* 区分 Supervised Learning 和 Unsupervised Learning
* 理解 Regression
* 理解 Classification
* 理解 Clustering
* 理解 Features 和 Labels
* 理解 Training、Validation 和 Testing
* 理解 Model Evaluation 的基本概念
* 根据实际场景选择合适的 Machine Learning 类型
* 理解 Machine Learning 模型从训练到评估的基本流程

---

# 2. Machine Learning

## 2.1 什么是 Machine Learning？

**Machine Learning（ML，机器学习）** 是 Artificial Intelligence 的一个重要分支。

机器学习的核心思想是：

> **让计算机通过数据学习模式，而不是为每一种情况手动编写明确的规则。**

传统编程：

```text
Rules
规则
+
Data
数据
 ↓
Program
程序
 ↓
Output
结果
```

Machine Learning：

```text
Data
数据
+
Training
训练
 ↓
Model
模型
```

使用训练好的模型：

```text
New Data
新的数据
 ↓
Trained Model
训练好的模型
 ↓
Prediction
预测结果
```

---

## 2.2 一个简单例子

假设我们想预测房屋价格。

我们收集历史数据：

| 面积   | 卧室数量 |  房龄 |    房价 |
| ---- | ---: | --: | ----: |
| 80㎡  |    2 | 10年 | 3000万 |
| 100㎡ |    3 |  5年 | 4000万 |
| 120㎡ |    3 |  3年 | 5000万 |

机器学习模型可以从这些数据中学习：

```text
房屋特征
   ↓
面积
卧室数量
房龄
   ↓
Machine Learning
   ↓
学习模式
   ↓
Model
```

然后输入新的房屋：

```text
100㎡
3个卧室
8年房龄
   ↓
Model
   ↓
预测价格
```

这里：

* 面积
* 卧室数量
* 房龄

属于 **Features**。

房价属于需要预测的 **Label**。

---

# 3. Supervised Learning

## 3.1 什么是 Supervised Learning？

**Supervised Learning（监督学习）** 是使用带有已知正确答案的数据训练模型。

训练数据通常包含：

```text
Features
特征
+
Labels
标签
```

基本流程：

```text
Features + Labels
        ↓
Training
        ↓
Model
        ↓
New Features
        ↓
Prediction
```

例如：

```text
房屋面积
卧室数量
房龄
+
历史房价
        ↓
Training
        ↓
Model
        ↓
新房屋信息
        ↓
预测房价
```

因为训练数据中已经知道正确答案，所以称为：

> **Supervised Learning**

可以理解为：

> **模型在“有答案”的数据上学习。**

---

## 3.2 Supervised Learning 的两种常见任务

AI-901 中需要重点理解：

```text
Supervised Learning
│
├── Regression
│   → 预测数值
│
└── Classification
    → 预测类别
```

---

# 4. Unsupervised Learning

## 4.1 什么是 Unsupervised Learning？

**Unsupervised Learning（无监督学习）** 使用没有明确 Labels 的数据寻找数据中的结构和模式。

基本过程：

```text
Data
数据
 ↓
Unsupervised Learning
 ↓
发现数据中的模式
 ↓
Groups / Clusters
```

例如一家商店拥有大量客户数据：

```text
客户 A
客户 B
客户 C
客户 D
客户 E
...
```

但是没有提前告诉模型：

```text
谁是高价值客户
谁是普通客户
谁是新客户
```

模型可以根据客户行为自动发现相似群体。

例如：

```text
Cluster 1
经常购买高价商品

Cluster 2
经常购买低价商品

Cluster 3
很少购买
```

这就是典型的 Unsupervised Learning。

---

## 4.2 Supervised vs Unsupervised

| 对比         | Supervised Learning       | Unsupervised Learning |
| ---------- | ------------------------- | --------------------- |
| 中文         | 监督学习                      | 无监督学习                 |
| 是否有 Labels | 通常有                       | 通常没有                  |
| 主要目标       | 预测结果                      | 发现结构                  |
| 常见任务       | Regression、Classification | Clustering            |
| 典型问题       | 预测房价                      | 客户分群                  |

记忆：

> **Supervised = 有答案，学习预测。**

> **Unsupervised = 没有答案，寻找模式。**

---

# 5. Regression

## 5.1 什么是 Regression？

**Regression（回归）** 是一种用于预测**连续数值**的 Machine Learning 任务。

关键词：

> **预测一个数值。**

例如：

* 房屋价格
* 温度
* 销售额
* 产品需求量
* 预计收入

---

## 5.2 Regression 示例

预测房屋价格：

```text
Features
│
├── 面积
├── 卧室数量
├── 房龄
└── 地理位置
       ↓
Regression Model
       ↓
预测房价
       ↓
4500 万日元
```

输出是一个数值：

```text
4500 万
```

因此属于 Regression。

---

## 5.3 Regression 的核心特点

Regression 的目标是：

> **预测连续的数值。**

例如：

```text
预测温度
→ 25.6°C

预测房价
→ 4500 万日元

预测销售额
→ 1200 万日元
```

这些都是数值预测。

---

## 5.4 回归模型的直观理解

可以把 Regression 简单理解为：

```text
输入 Features
      ↓
学习 Features 与目标值之间的关系
      ↓
Model
      ↓
预测新的数值
```

---

# 6. Classification

## 6.1 什么是 Classification？

**Classification（分类）** 是预测数据属于哪个**类别**的 Machine Learning 任务。

关键词：

> **预测类别。**

例如：

* 垃圾邮件 / 正常邮件
* 猫 / 狗
* 欺诈 / 正常
* 患病 / 健康
* 高风险 / 低风险

---

## 6.2 Classification 示例

垃圾邮件检测：

```text
邮件内容
 ↓
Classification Model
 ↓
Spam
或
Not Spam
```

输出不是连续数值，而是类别。

---

## 6.3 Binary Classification

如果只有两个类别，称为：

**Binary Classification（二分类）**

例如：

```text
Spam
Not Spam
```

或者：

```text
Fraud
Not Fraud
```

或者：

```text
Yes
No
```

---

## 6.4 Multiclass Classification

如果有多个类别：

```text
Cat
Dog
Bird
```

模型需要判断输入属于哪一个类别。

例如图像分类：

```text
图片
 ↓
Classification Model
 ↓
Cat
Dog
Bird
```

---

## 6.5 Classification 的核心特点

Classification 的目标：

> **预测输入属于哪个类别。**

简单记忆：

```text
Regression
→ 数值

Classification
→ 类别
```

---

# 7. Clustering

## 7.1 什么是 Clustering？

**Clustering（聚类）** 是一种常见的 Unsupervised Learning 任务。

它的目标是：

> **根据数据之间的相似性，将相似的数据自动分成不同的群组。**

基本过程：

```text
大量没有 Labels 的数据
        ↓
Clustering
        ↓
发现相似的数据
        ↓
Cluster 1
Cluster 2
Cluster 3
```

---

## 7.2 客户分群示例

假设我们有客户数据：

```text
客户
│
├── 购买频率
├── 消费金额
└── 购买类型
```

使用 Clustering 后可能得到：

```text
Cluster 1
高消费 + 高频购买

Cluster 2
低消费 + 高频购买

Cluster 3
低消费 + 低频购买
```

模型并没有提前知道这些类别。

它只是根据数据之间的相似性自动形成群组。

---

## 7.3 Clustering 的核心特点

Clustering：

* 通常属于 Unsupervised Learning
* 不需要预先提供 Labels
* 根据数据相似性形成群组
* 常用于客户分群
* 市场细分
* 异常模式探索
* 数据分析

记忆：

> **Clustering = 没有预先定义答案，根据相似性自动分组。**

---

# 8. Features

## 8.1 什么是 Feature？

**Feature（特征）** 是用于描述数据、帮助模型进行学习或预测的输入变量。

例如预测房价：

```text
房屋
│
├── 面积
├── 卧室数量
├── 房龄
├── 地理位置
└── 楼层
```

这些信息都是 Features。

---

## 8.2 Features 示例

预测汽车价格：

```text
Features
│
├── 品牌
├── 年份
├── 行驶里程
├── 发动机排量
└── 车型
```

目标：

```text
预测汽车价格
```

这里 Features 是：

```text
品牌
年份
里程
排量
车型
```

---

## 8.3 Feature 的作用

可以简单理解：

> **Feature 是模型用来进行预测或分析的输入信息。**

结构：

```text
Features
输入特征
 ↓
Machine Learning Model
 ↓
Prediction
预测结果
```

---

# 9. Labels

## 9.1 什么是 Label？

**Label（标签）** 是监督学习中模型需要预测的目标值或正确答案。

例如：

```text
Features
│
├── 面积
├── 卧室数量
└── 房龄

Label
│
└── 房价
```

模型学习：

```text
Features
   ↓
Label
```

然后对新的 Features 进行预测。

---

## 9.2 Classification 中的 Label

垃圾邮件检测：

```text
Features
│
└── 邮件内容

Label
│
├── Spam
└── Not Spam
```

这里 Label 是类别。

---

## 9.3 Regression 中的 Label

房价预测：

```text
Features
│
├── 面积
├── 房龄
└── 卧室数量

Label
│
└── 房价
```

这里 Label 是连续数值。

---

## 9.4 Features vs Labels

|      | Features | Labels |
| ---- | -------- | ------ |
| 中文   | 特征       | 标签     |
| 作用   | 输入信息     | 目标答案   |
| 例子   | 面积、年龄    | 房价     |
| 监督学习 | 输入       | 目标     |

记忆：

> **Features = 用什么信息进行预测。**

> **Label = 想预测什么。**

---

# 10. Training

## 10.1 什么是 Training？

**Training（训练）** 是使用训练数据让 Machine Learning 模型学习模式的过程。

例如：

```text
Training Data
│
├── Features
└── Labels
       ↓
Training
       ↓
Machine Learning Model
```

模型尝试学习：

```text
Features
    ↓
与
    ↓
Labels
之间的关系
```

---

## 10.2 Training 示例

房价预测：

```text
面积 + 房龄 + 卧室数量
        ↓
Training Data
        ↓
Training
        ↓
Regression Model
```

训练完成后：

```text
新房屋
 ↓
Model
 ↓
预测房价
```

---

# 11. Validation

## 11.1 什么是 Validation？

**Validation（验证）** 是在模型开发过程中使用验证数据检查和改进模型的过程。

通常用于：

* 比较不同模型
* 调整模型参数
* 选择更合适的模型
* 检查模型是否存在过拟合问题

基本流程：

```text
Training Data
      ↓
训练模型
      ↓
Validation Data
      ↓
检查模型表现
      ↓
调整模型
```

---

## 11.2 为什么需要 Validation？

假设我们训练了两个模型：

```text
Model A
Training 表现很好

Model B
Training 表现一般
```

不能只看 Training 结果。

因为 Model A 可能只是记住了训练数据。

需要使用 Validation 数据检查：

```text
哪个模型在没有参与训练的数据上表现更好？
```

因此 Validation 可以帮助：

> **在模型开发过程中选择和调整模型。**

---

# 12. Testing

## 12.1 什么是 Testing？

**Testing（测试）** 是使用独立的测试数据，对最终模型的实际表现进行评估。

基本流程：

```text
Training Data
      ↓
训练模型
      ↓
Validation Data
      ↓
选择和调整模型
      ↓
最终模型
      ↓
Test Data
      ↓
最终评估
```

Testing 数据通常不用于训练模型。

---

## 12.2 为什么需要 Test Data？

如果使用训练数据评价模型：

```text
模型可能已经见过这些数据
```

那么评价结果可能过于乐观。

因此，需要使用模型没有参与训练的独立数据测试模型。

目的：

> **估计模型在真实新数据上的表现。**

---

# 13. Model Evaluation

## 13.1 什么是 Model Evaluation？

**Model Evaluation（模型评估）** 是使用指标判断 Machine Learning 模型表现的过程。

不同的 Machine Learning 任务需要使用不同的评估方法。

例如：

```text
Regression
→ 评估预测数值与真实数值之间的差异

Classification
→ 评估分类预测是否正确
```

---

## 13.2 Regression 的评估

Regression 预测的是数值。

例如：

```text
真实房价
5000 万

模型预测
4800 万
```

可以计算预测值与真实值之间的误差。

常见指标包括：

* MAE
* MSE
* RMSE
* R²

AI-901 学习阶段重点理解：

> **回归模型需要衡量预测值与真实值之间的误差。**

---

## 13.3 Classification 的评估

Classification 需要判断类别预测是否正确。

例如：

```text
真实：
Spam

预测：
Spam
```

预测正确。

常见分类评估指标：

* Accuracy
* Precision
* Recall
* F1 Score

还可以使用：

**Confusion Matrix（混淆矩阵）**

来分析分类结果。

---

## 13.4 Accuracy

Accuracy 表示：

> **所有预测中，预测正确的比例。**

适用于类别分布比较均衡的情况。

例如：

```text
100 个样本
90 个预测正确
```

Accuracy：

```text
90%
```

---

## 13.5 Precision

Precision 关注：

> **模型预测为正类的样本中，有多少是真正的正类。**

例如垃圾邮件检测：

```text
模型认为是垃圾邮件
        ↓
其中真正是垃圾邮件的比例
```

当误报成本较高时，Precision 可能更加重要。

---

## 13.6 Recall

Recall 关注：

> **所有真正的正类中，模型成功识别出来的比例。**

例如疾病检测：

```text
真正患病的人
        ↓
模型成功检测出来的人
```

当漏掉正类的成本很高时，Recall 可能更加重要。

---

## 13.7 Precision 与 Recall

简单理解：

```text
Precision
→ 我预测为正的，有多少是真的？

Recall
→ 真正的正类，我找到了多少？
```

例如：

### 垃圾邮件过滤

如果误把正常邮件当成垃圾邮件很严重：

> 更关注 Precision。

### 疾病筛查

如果漏掉真正患病的人很严重：

> 更关注 Recall。

---

## 13.8 Model Evaluation 的核心思想

模型评估不是简单地问：

> 模型有没有预测正确？

而是需要根据业务场景考虑：

* 哪些错误更严重？
* False Positive 是否严重？
* False Negative 是否严重？
* 数据是否平衡？
* 模型是否能泛化到新数据？

因此：

> **选择评估指标应该结合实际业务场景。**

---

# 14. Training、Validation、Testing

这是本章最重要的知识点之一。

可以理解为：

```text id="7s5kbl"
完整数据集
    │
    ├── Training Data
    │      ↓
    │   训练模型
    │
    ├── Validation Data
    │      ↓
    │   调整和选择模型
    │
    └── Test Data
           ↓
        最终评估
```

---

## 14.1 Training

作用：

> **训练模型。**

模型使用 Training Data 学习数据中的模式。

---

## 14.2 Validation

作用：

> **开发过程中检查和调整模型。**

用于：

* 比较模型
* 调整参数
* 选择模型

---

## 14.3 Testing

作用：

> **对最终模型进行独立测试。**

用于估计模型在新数据上的实际表现。

---

## 14.4 三者对比

| 数据集        | 主要用途    |
| ---------- | ------- |
| Training   | 训练模型    |
| Validation | 调整和选择模型 |
| Testing    | 最终评估    |

记忆：

```text
Training
→ 学习

Validation
→ 调整

Testing
→ 最终检查
```

---

# 15. Supervised Learning 总结

```text
Supervised Learning
│
├── Features
│
├── Labels
│
└── Training
       ↓
    Model
       ↓
    Prediction
```

主要任务：

```text
Regression
→ 预测数值

Classification
→ 预测类别
```

---

# 16. Unsupervised Learning 总结

```text
Unsupervised Learning
│
└── 没有明确 Labels
       ↓
    发现数据结构
       ↓
    Clustering
       ↓
    自动形成群组
```

---

# 17. AI-901 考试重点

## 重点 1：Supervised vs Unsupervised

```text
Supervised Learning
→ 有 Labels
→ 学习预测

Unsupervised Learning
→ 没有 Labels
→ 寻找数据结构
```

---

## 重点 2：Regression vs Classification

```text
Regression
→ 预测数值

Classification
→ 预测类别
```

例如：

```text
预测房价
→ Regression

判断垃圾邮件
→ Classification
```

---

## 重点 3：Clustering

```text
Clustering
→ Unsupervised Learning
→ 根据相似性自动分组
```

---

## 重点 4：Features vs Labels

```text
Features
→ 输入信息

Labels
→ 目标答案
```

---

## 重点 5：Training / Validation / Testing

```text
Training
→ 训练

Validation
→ 调整 / 选择

Testing
→ 最终评估
```

---

## 重点 6：Model Evaluation

需要知道：

```text
Regression
→ 关注预测误差

Classification
→ 关注分类表现
```

分类常见指标：

```text
Accuracy
Precision
Recall
F1 Score
```

---

# 18. 易混淆概念

## Regression vs Classification

错误理解：

> Regression 是分类数字，Classification 是分类文字。

正确理解：

```text
Regression
→ 输出连续数值

Classification
→ 输出类别
```

例如：

```text
预测温度
→ Regression

预测房价
→ Regression

预测猫 / 狗
→ Classification

预测垃圾 / 正常
→ Classification
```

---

## Classification vs Clustering

```text
Classification
→ Supervised
→ 有 Labels
→ 预测已知类别

Clustering
→ Unsupervised
→ 没有 Labels
→ 自动发现群组
```

---

## Features vs Labels

```text
Features
→ 输入

Labels
→ 目标
```

例如：

```text
房屋面积
房龄
卧室数量
    ↓
Features

房价
    ↓
Label
```

---

## Training vs Validation

```text
Training
→ 学习模型

Validation
→ 开发过程中调整模型
```

---

## Validation vs Testing

```text
Validation
→ 用于模型选择和调整

Testing
→ 最终独立评估
```

---

## Accuracy vs Precision vs Recall

```text
Accuracy
→ 总体预测正确多少

Precision
→ 预测为正的有多少是真的

Recall
→ 真正的正类找到了多少
```

---

# 19. 练习题

## 练习题 1

以下哪个最准确地描述 Machine Learning？

A. 只能通过人工编写规则处理数据
B. 让计算机从数据中学习模式
C. 只用于数据库存储
D. 只能用于图像识别

<details>
<summary>查看答案</summary>

**答案：B**

Machine Learning 的核心思想是让计算机通过数据学习模式，并使用学习到的模型处理新的输入。

</details>

---

## 练习题 2

以下哪种 Machine Learning 使用带有 Labels 的训练数据？

A. Supervised Learning
B. Unsupervised Learning
C. Clustering
D. Random Search

<details>
<summary>查看答案</summary>

**答案：A**

Supervised Learning 使用带有已知目标值或 Labels 的数据进行训练。

</details>

---

## 练习题 3

一个房地产公司希望根据房屋面积、房龄和卧室数量预测房屋价格。应该使用：

A. Classification
B. Regression
C. Clustering
D. Speech Recognition

<details>
<summary>查看答案</summary>

**答案：B**

房屋价格是连续数值，因此属于 Regression。

</details>

---

## 练习题 4

一个系统需要判断邮件是 Spam 还是 Not Spam。应该使用：

A. Regression
B. Classification
C. Clustering
D. Regression Analysis

<details>
<summary>查看答案</summary>

**答案：B**

Spam 和 Not Spam 是类别，因此属于 Classification。

</details>

---

## 练习题 5

一家零售企业没有客户类别标签，希望根据客户购买行为自动将客户分成几个群组。应该使用：

A. Regression
B. Classification
C. Clustering
D. Speech-to-Text

<details>
<summary>查看答案</summary>

**答案：C**

没有预先定义 Labels，根据相似性自动分组属于 Clustering。

</details>

---

## 练习题 6

在房价预测模型中，房屋面积、房龄和卧室数量属于：

A. Labels
B. Features
C. Predictions
D. Test Results

<details>
<summary>查看答案</summary>

**答案：B**

这些是用于预测房价的输入变量，因此属于 Features。

</details>

---

## 练习题 7

在房价预测模型中，房价属于：

A. Feature
B. Label
C. Cluster
D. Training Data

<details>
<summary>查看答案</summary>

**答案：B**

在监督学习中，模型需要预测的目标值通常称为 Label。

</details>

---

## 练习题 8

以下哪个数据集主要用于训练模型？

A. Training Data
B. Validation Data
C. Test Data
D. Production Data

<details>
<summary>查看答案</summary>

**答案：A**

Training Data 用于训练模型。

</details>

---

## 练习题 9

以下哪个数据集主要用于模型开发过程中的调整和选择？

A. Training Data
B. Validation Data
C. Test Data
D. Backup Data

<details>
<summary>查看答案</summary>

**答案：B**

Validation Data 用于模型开发过程中的比较、调整和选择。

</details>

---

## 练习题 10

最终评估模型在新数据上的表现，通常使用：

A. Training Data
B. Validation Data
C. Test Data
D. Labels Only

<details>
<summary>查看答案</summary>

**答案：C**

Test Data 用于最终独立评估模型。

</details>

---

## 练习题 11

以下哪一组对应关系正确？

A. Regression → 预测类别
B. Classification → 预测连续数值
C. Clustering → 无监督学习
D. Classification → 不需要 Labels

<details>
<summary>查看答案</summary>

**答案：C**

Clustering 通常属于 Unsupervised Learning。

</details>

---

## 练习题 12

以下哪个指标用于评估分类模型？

A. Precision
B. Recall
C. F1 Score
D. 以上全部

<details>
<summary>查看答案</summary>

**答案：D**

Precision、Recall 和 F1 Score 都是常见的 Classification 评估指标。

</details>

---

## 练习题 13

如果业务场景最担心漏掉真正的正类，应该重点关注：

A. Recall
B. Precision
C. Training Loss
D. Feature Count

<details>
<summary>查看答案</summary>

**答案：A**

Recall 关注真正的正类中有多少被模型成功识别。

</details>

---

## 练习题 14

如果模型预测为正类的结果中，企业非常关注其中有多少是真正的正类，应该关注：

A. Recall
B. Precision
C. Clustering
D. Regression

<details>
<summary>查看答案</summary>

**答案：B**

Precision 关注预测为正类的样本中，有多少是真正的正类。

</details>

---

## 练习题 15

以下哪种顺序最合理？

A. Testing → Training → Validation
B. Training → Validation → Testing
C. Validation → Testing → Training
D. Testing → Validation → Training

<details>
<summary>查看答案</summary>

**答案：B**

典型流程是：

```text
Training
→ Validation
→ Testing
```

即先训练模型，再进行开发过程中的验证和调整，最后使用独立测试数据进行最终评估。

</details>

---

# 20. 本章一句话记忆

> **Supervised Learning 使用 Features 和 Labels 学习预测，其中 Regression 预测数值，Classification 预测类别；Unsupervised Learning 通常没有 Labels，Clustering 根据相似性自动分组；Training 用于训练，Validation 用于调整和选择，Testing 用于最终评估。**

---

# 21. 本章知识结构

```text
Machine Learning
│
├── Supervised Learning
│   │
│   ├── Features
│   │
│   ├── Labels
│   │
│   ├── Regression
│   │   └── 预测数值
│   │
│   └── Classification
│       └── 预测类别
│
└── Unsupervised Learning
    │
    └── Clustering
        └── 自动分组
```

模型开发流程：

```text
Data
│
├── Training Data
│      ↓
│   Training
│      ↓
│   Model
│
├── Validation Data
│      ↓
│   Model Selection
│   Parameter Tuning
│
└── Test Data
       ↓
   Final Evaluation
```

模型评估：

```text
Regression
    ↓
预测数值
    ↓
评估预测误差

Classification
    ↓
预测类别
    ↓
Accuracy
Precision
Recall
F1 Score
```

---

# 🎯 本章最终记忆框架

```text
Machine Learning
        │
        ├── Supervised Learning
        │       │
        │       ├── Features
        │       ├── Labels
        │       │
        │       ├── Regression
        │       │   └── 数值
        │       │
        │       └── Classification
        │           └── 类别
        │
        └── Unsupervised Learning
                │
                └── Clustering
                    └── 自动分组
```

模型生命周期：

```text
Training Data
      ↓
Training
      ↓
Model
      ↓
Validation
      ↓
Model Selection / Tuning
      ↓
Final Model
      ↓
Test Data
      ↓
Model Evaluation
```

---

# 🧠 一分钟复习

```text
Supervised
→ 有 Label

Unsupervised
→ 没有 Label

Regression
→ 预测数值

Classification
→ 预测类别

Clustering
→ 自动分组

Feature
→ 输入

Label
→ 目标

Training
→ 学习

Validation
→ 调整 / 选择

Testing
→ 最终测试

Model Evaluation
→ 判断模型表现
```

> **本章核心：理解 Machine Learning 的基本类型和完整流程。看到“预测数值”想到 Regression，看到“预测类别”想到 Classification，看到“没有标签、自动分组”想到 Clustering；看到 Training、Validation、Testing，要能够区分三者在模型开发生命周期中的不同作用。**
