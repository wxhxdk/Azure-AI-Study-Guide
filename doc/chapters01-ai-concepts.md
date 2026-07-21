# 第1章 AI 基础概念

> 本章对应 AI-901 学习路线中的第 1 章，主要建立人工智能、AI 模型、机器学习、深度学习和生成式 AI 的基础认知，并理解 AI 与传统软件的区别以及常见 AI Workloads。

---

# 0. AI-901 考试介绍

## 0.1 AI-901 是什么？

**AI-901: Microsoft Azure AI Fundamentals** 是 Microsoft 面向 AI 基础知识和 Azure AI 解决方案的基础级认证考试。

考试重点不是要求考生自己从零开发复杂的 AI 模型，而是要求理解：

* AI 基本概念
* Machine Learning 基础
* Responsible AI
* AI Workloads
* Generative AI
* Microsoft Foundry
* Azure AI 解决方案的基本应用场景

因此，本章学习的内容是后续章节的基础。

---

## 0.2 本章与 AI-901 的关系

本章主要帮助建立以下知识体系：

```text
Artificial Intelligence
        ↓
Machine Learning
        ↓
Deep Learning
```

同时理解：

```text
Generative AI
        ↓
生成文本、图像、代码等内容
```

以及：

```text
Training
        ↓
训练模型

Inference
        ↓
使用模型
```

最后理解不同 AI Workloads：

```text
Computer Vision
NLP
Speech
Generative AI
Information Extraction
```

后续章节会分别深入学习这些内容。

---

# 1. 本章学习目标

学习完本章后，你应该能够：

* 理解 Artificial Intelligence 的基本概念
* 理解 AI Model 的作用
* 理解 Machine Learning 的基本思想
* 理解 Deep Learning 与 Machine Learning 的关系
* 理解 Generative AI 的基本概念
* 区分 Training 和 Inference
* 了解 AI 的常见应用场景
* 理解 AI 与传统软件的基本区别
* 识别常见 AI Workloads
* 根据实际问题判断适合的 AI 类型

---

# 2. Artificial Intelligence

## 2.1 什么是 Artificial Intelligence？

**Artificial Intelligence（AI，人工智能）** 是一种让计算机系统执行通常需要人类智能才能完成任务的技术。

这些任务包括：

* 理解语言
* 识别图像
* 识别人类语音
* 分析数据
* 预测结果
* 进行分类
* 生成内容
* 根据输入做出决策

简单来说：

> **AI 的目标是让计算机系统能够完成需要智能处理的任务。**

例如：

```text
人类
│
├── 看图片 → 识别物体
├── 听声音 → 理解语音
├── 阅读文字 → 理解语言
├── 分析数据 → 发现规律
└── 根据经验 → 做出判断
```

AI 系统尝试使用计算机完成类似的任务。

---

## 2.2 AI 的基本工作方式

一个简单的 AI 系统可以理解为：

```text
Input
输入
  ↓
AI Model
AI 模型
  ↓
Processing
处理
  ↓
Output
输出
```

例如图像识别：

```text
图片
 ↓
AI Vision Model
 ↓
分析图像
 ↓
识别：
“这是一只猫”
```

例如语音识别：

```text
用户语音
 ↓
Speech Model
 ↓
分析声音
 ↓
转换成文字
```

例如生成式 AI：

```text
用户 Prompt
 ↓
Generative AI Model
 ↓
生成内容
```

因此可以简单理解：

> **输入 → 模型处理 → 输出**

---

# 3. AI Model

## 3.1 什么是 AI Model？

**AI Model（AI 模型）** 是 AI 系统的核心组成部分。

模型通过数据学习某种模式或规律，然后利用这些规律处理新的输入。

基本过程：

```text
Training Data
训练数据
    ↓
Model Training
模型训练
    ↓
AI Model
AI 模型
    ↓
New Input
新的输入
    ↓
Prediction / Generation
预测 / 生成
```

例如训练一个图像分类模型：

```text
大量猫和狗的图片
        ↓
训练模型
        ↓
Image Classification Model
        ↓
输入一张新图片
        ↓
模型预测
        ↓
“Cat”
```

---

## 3.2 AI Model 不是数据库

这是一个容易混淆的概念。

数据库主要用于：

> **保存、管理和查询数据。**

AI 模型主要用于：

> **从数据中学习模式，并使用这些模式处理新的输入。**

简单比较：

|      | Database | AI Model     |
| ---- | -------- | ------------ |
| 主要目的 | 保存数据     | 学习模式         |
| 处理方式 | 查询数据     | 预测或生成        |
| 输入   | 查询条件     | 新数据 / Prompt |
| 输出   | 已保存的数据   | 预测 / 生成结果    |

例如：

```text
数据库：
查询 → 返回已经保存的数据

AI 模型：
输入新数据 → 根据学习到的模式 → 生成预测结果
```

---

# 4. Machine Learning

## 4.1 什么是 Machine Learning？

**Machine Learning（ML，机器学习）** 是 Artificial Intelligence 的重要分支。

机器学习的核心思想是：

> **让计算机从数据中学习规律，而不是为所有情况手动编写规则。**

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

机器学习：

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

训练完成后：

```text
New Data
新数据
 ↓
ML Model
机器学习模型
 ↓
Prediction
预测结果
```

---

## 4.2 一个简单例子

假设我们需要识别垃圾邮件。

传统方式可能需要编写很多规则：

```text
如果包含“中奖”
→ 垃圾邮件

如果包含“免费”
→ 垃圾邮件

如果来自某个地址
→ 垃圾邮件
```

这种方式依赖人工定义规则。

机器学习则可以使用大量历史邮件：

```text
正常邮件
垃圾邮件
正常邮件
垃圾邮件
...
```

模型通过训练学习其中的模式。

之后：

```text
新邮件
 ↓
Machine Learning Model
 ↓
垃圾邮件 / 正常邮件
```

---

## 4.3 Machine Learning 的特点

机器学习通常具有以下特点：

* 使用数据学习
* 可以发现数据中的模式
* 可以对新的数据进行预测
* 可以用于分类
* 可以用于回归
* 可以用于聚类

Machine Learning 的具体类型会在**第 2 章 Machine Learning 基础**中详细学习。

---

# 5. Deep Learning

## 5.1 什么是 Deep Learning？

**Deep Learning（深度学习）** 是 Machine Learning 的一种。

深度学习通常使用多层神经网络（Neural Networks）处理复杂数据。

可以简单理解为：

```text
Artificial Intelligence
        ↓
Machine Learning
        ↓
Deep Learning
```

因此：

> **Deep Learning 是 Machine Learning 的子集。**

---

## 5.2 Deep Learning 的基本结构

可以简单表示为：

```text
Input
输入
 ↓
Neural Network
神经网络
 ↓
Hidden Layers
隐藏层
 ↓
Output
输出
```

深度学习通常特别适合处理：

* 图像
* 语音
* 自然语言
* 视频

例如图像识别：

```text
图片
 ↓
Deep Learning Model
 ↓
分析图像特征
 ↓
分类
 ↓
“猫”
```

---

## 5.3 AI、ML、Deep Learning 的关系

可以记住：

```text
AI
│
└── Machine Learning
    │
    └── Deep Learning
```

含义：

* **AI**：最大的概念
* **Machine Learning**：AI 的重要分支
* **Deep Learning**：Machine Learning 的一种

考试中经常通过概念关系进行考察。

---

# 6. Generative AI

## 6.1 什么是 Generative AI？

**Generative AI（生成式 AI）** 是能够根据输入生成新内容的 AI 技术。

它可以生成：

* 文本
* 图片
* 代码
* 音频
* 视频

基本过程：

```text
Prompt
输入指令
 ↓
Generative AI Model
生成式 AI 模型
 ↓
Generated Content
生成内容
```

例如：

```text
用户：
请写一篇关于人工智能的文章。

        ↓

Generative AI

        ↓

生成一篇新的文章
```

---

## 6.2 Generative AI 与传统 AI 的区别

传统 AI 经常执行：

* 分类
* 预测
* 检测
* 分析

例如：

```text
图片
 ↓
Image Classification
 ↓
“猫”
```

Generative AI 则可以：

```text
Prompt
“写一首关于春天的诗”
 ↓
Generative AI
 ↓
生成新的诗歌
```

简单记忆：

> **传统 AI 更关注分析、分类和预测。**

> **Generative AI 更关注生成新的内容。**

需要注意的是，这并不意味着传统 AI 完全不能生成内容，而是 Generative AI 的核心用途和能力重点就是内容生成。

---

## 6.3 Generative AI 的应用

常见应用包括：

### 文本生成

```text
Prompt
 ↓
生成文章
```

### 代码生成

```text
自然语言需求
 ↓
生成代码
```

### 图像生成

```text
Text Prompt
 ↓
Image Generation Model
 ↓
生成图片
```

### 对话式 AI

```text
用户问题
 ↓
Generative AI
 ↓
生成回答
```

### 内容总结

```text
长文档
 ↓
Generative AI
 ↓
摘要
```

---

# 7. Training

## 7.1 什么是 Training？

**Training（训练）** 是使用数据让 AI 模型学习模式和规律的过程。

基本流程：

```text
Training Data
训练数据
    ↓
Training
模型训练
    ↓
Trained Model
训练好的模型
```

例如训练图像分类模型：

```text
大量图片
 ↓
Training
 ↓
模型学习图像特征
 ↓
得到训练好的模型
```

---

## 7.2 Training 的目的

Training 的目的是：

> **让模型学习数据中的模式，使其能够处理新的输入。**

例如：

```text
训练数据
猫、狗、猫、狗……
        ↓
Training
        ↓
学习特征
        ↓
模型
        ↓
新的图片
        ↓
预测“猫”
```

---

## 7.3 Training 不等于使用模型

需要区分：

```text
Training
→ 训练模型

Inference
→ 使用模型
```

这两个过程是 AI 系统中的不同阶段。

---

# 8. Inference

## 8.1 什么是 Inference？

**Inference（推理）** 是使用已经训练好的模型处理新的输入并生成结果的过程。

例如：

```text
Training
训练
 ↓
得到训练好的模型

Inference
推理
 ↓
输入新数据
 ↓
模型处理
 ↓
得到结果
```

---

## 8.2 一个简单例子

图像分类：

```text
训练阶段

大量图片
 ↓
Training
 ↓
Image Model
```

使用阶段：

```text
新图片
 ↓
Inference
 ↓
“这是一只猫”
```

因此：

> **Training 是让模型学习。**

> **Inference 是使用模型。**

---

## 8.3 Training vs Inference

| 对比        | Training | Inference |
| --------- | -------- | --------- |
| 中文        | 训练       | 推理        |
| 目的        | 学习数据中的模式 | 使用模型处理新输入 |
| 输入        | 训练数据     | 新数据       |
| 结果        | 训练好的模型   | 预测或生成结果   |
| 是否是模型使用阶段 | 否        | 是         |

这是 AI-901 中需要掌握的基础概念。

---

# 9. AI 的常见应用

AI 已经广泛应用于多个领域。

---

## 9.1 医疗

常见应用：

* 医学图像分析
* 疾病预测
* 医疗文档分析
* 医疗信息提取

例如：

```text
医学影像
 ↓
Computer Vision
 ↓
辅助分析
```

---

## 9.2 金融

常见应用：

* 欺诈检测
* 风险分析
* 信用评估
* 客户服务

例如：

```text
交易数据
 ↓
Machine Learning
 ↓
识别异常交易
```

---

## 9.3 零售

常见应用：

* 推荐系统
* 商品识别
* 客户行为分析
* 智能客服

例如：

```text
用户历史行为
 ↓
Machine Learning
 ↓
推荐商品
```

---

## 9.4 制造业

常见应用：

* 预测性维护
* 产品质量检测
* 图像缺陷检测
* 设备异常检测

例如：

```text
生产线图片
 ↓
Computer Vision
 ↓
检测产品缺陷
```

---

## 9.5 客户服务

常见应用：

* Chatbot
* AI Assistant
* 自动问答
* 文档问答
* 内容总结

例如：

```text
用户问题
 ↓
Generative AI
 ↓
AI Assistant
 ↓
生成回答
```

---

## 9.6 企业自动化

AI 可以帮助企业自动处理：

* 发票
* 合同
* 表格
* 邮件
* 文档

例如：

```text
发票
 ↓
AI
 ↓
提取：
供应商
日期
金额
发票号码
```

这属于 Information Extraction 的典型应用。

---

# 10. AI 与传统软件的区别

## 10.1 传统软件

传统软件通常由开发人员明确编写规则。

基本流程：

```text
Input
输入
 ↓
预先编写的 Rules
规则
 ↓
Program
程序
 ↓
Output
输出
```

例如：

```text
如果年龄 >= 18
    ↓
允许注册
否则
    ↓
拒绝注册
```

规则是由程序员明确指定的。

---

## 10.2 Machine Learning 系统

机器学习系统通常通过数据学习模式。

```text
Training Data
训练数据
 ↓
Machine Learning
 ↓
Model
模型
 ↓
New Input
新的输入
 ↓
Prediction
预测
```

例如：

```text
大量历史邮件
 ↓
Training
 ↓
Spam Detection Model
 ↓
新邮件
 ↓
预测：
Spam / Not Spam
```

---

## 10.3 两者的核心区别

| 对比   | 传统软件    | Machine Learning |
| ---- | ------- | ---------------- |
| 核心   | 人工编写规则  | 从数据中学习模式         |
| 规则   | 明确写入程序  | 模型从数据中学习         |
| 处理方式 | 按固定逻辑执行 | 根据模型进行预测         |
| 适合场景 | 规则明确    | 模式复杂、难以手动定义      |
| 输出   | 通常较确定   | 可能存在概率和不确定性      |

需要注意：

> 实际应用中，传统软件和 AI 模型经常结合使用。

例如：

```text
用户输入
 ↓
传统程序规则
 ↓
AI Model
 ↓
业务逻辑
 ↓
最终结果
```

因此：

> **AI 并不是传统软件的完全替代品。**

很多真实应用是：

> **传统程序 + AI 模型**

共同完成任务。

---

# 11. AI Workloads 基础

## 11.1 什么是 AI Workload？

**AI Workload** 可以理解为 AI 解决方案需要完成的任务类型。

不同的问题需要使用不同的 AI Workload。

例如：

```text
需要识别图片
→ Computer Vision

需要理解文本
→ Natural Language Processing

需要处理语音
→ Speech

需要生成内容
→ Generative AI

需要从文档提取字段
→ Information Extraction
```

---

## 11.2 Computer Vision

**Computer Vision（计算机视觉）** 用于处理图像和视频。

常见任务：

* Image Analysis
* Image Classification
* Object Detection
* OCR
* Face Detection

例如：

```text
图片
 ↓
Computer Vision
 ↓
识别：
人
汽车
猫
狗
```

典型场景：

* 人脸检测
* 商品识别
* 自动驾驶
* 医学图像分析
* 工业质量检测

---

## 11.3 Natural Language Processing

**Natural Language Processing（NLP，自然语言处理）** 用于处理和理解人类语言。

常见任务：

* Text Analysis
* Sentiment Analysis
* Entity Recognition
* Keyword Extraction
* Text Classification

例如：

```text
“这个产品非常好，我很喜欢。”

        ↓

NLP

        ↓

Sentiment:
Positive
```

典型场景：

* 情感分析
* 文本分类
* 智能客服
* 文本分析

---

## 11.4 Speech

Speech AI 用于处理人类语音。

常见任务：

* Speech-to-Text
* Text-to-Speech
* Speech Recognition
* Speech Translation

例如：

```text
用户说话
 ↓
Speech-to-Text
 ↓
文字
```

或者：

```text
文字
 ↓
Text-to-Speech
 ↓
语音
```

---

## 11.5 Generative AI

Generative AI 用于生成新的内容。

常见内容：

* Text
* Image
* Code
* Audio
* Video

例如：

```text
Prompt
 ↓
Generative AI
 ↓
生成内容
```

典型场景：

* AI Chatbot
* AI Assistant
* 内容生成
* 代码生成
* 文档总结

---

## 11.6 Information Extraction

Information Extraction 用于从非结构化或半结构化内容中提取有用信息。

例如：

```text
发票
 ↓
AI
 ↓
发票号码
日期
金额
供应商
```

典型场景：

* 发票处理
* 合同分析
* 表单处理
* 文档自动化

---

## 11.7 AI Workloads 快速判断

考试中遇到场景题，可以使用以下方法：

```text
看到图片 / 视频
→ Computer Vision

看到文本 / 语言
→ NLP

看到声音 / 语音
→ Speech

看到“生成”
→ Generative AI

看到“从文档中提取字段”
→ Information Extraction
```

例如：

### 场景 1

> 判断一张图片中是否有汽车。

答案：

> Computer Vision

---

### 场景 2

> 判断客户评论是正面还是负面。

答案：

> NLP / Sentiment Analysis

---

### 场景 3

> 把客户电话转换成文字。

答案：

> Speech-to-Text

---

### 场景 4

> 根据 Prompt 写一篇文章。

答案：

> Generative AI

---

### 场景 5

> 从发票中提取金额。

答案：

> Information Extraction

---

# 12. 核心知识总结

## AI

> 让计算机执行通常需要人类智能才能完成的任务。

---

## AI Model

> 通过学习数据中的模式，对新的输入进行预测、分类、分析或生成。

---

## Machine Learning

> AI 的重要分支，让计算机从数据中学习模式。

---

## Deep Learning

> Machine Learning 的一种，通常使用多层神经网络。

---

## Generative AI

> 能够根据输入生成新内容的 AI 技术。

---

## Training

> 使用数据训练模型，使模型学习数据中的模式。

---

## Inference

> 使用已经训练好的模型处理新的输入。

---

## AI Workloads

```text
Computer Vision
→ 图像 / 视频

NLP
→ 文本 / 语言

Speech
→ 语音

Generative AI
→ 内容生成

Information Extraction
→ 信息提取
```

---

# 13. AI-901 考试重点

## 重点 1：AI、Machine Learning、Deep Learning 的关系

```text
AI
└── Machine Learning
    └── Deep Learning
```

记住：

> **Deep Learning 是 Machine Learning 的一种。**

---

## 重点 2：Training 与 Inference

```text
Training
→ 训练模型

Inference
→ 使用模型
```

---

## 重点 3：Generative AI

核心特征：

> **生成新的内容。**

例如：

* 文本
* 图片
* 代码
* 音频

---

## 重点 4：AI Workloads

```text
图片
→ Computer Vision

文本
→ NLP

语音
→ Speech

生成内容
→ Generative AI

提取文档信息
→ Information Extraction
```

---

## 重点 5：AI Model 与 Database

```text
Database
→ 保存数据

AI Model
→ 学习模式
→ 处理新输入
```

---

## 重点 6：AI 不等于自己训练模型

实际 AI 应用中，可以直接使用：

* 预训练模型
* Foundation Models
* Azure AI Services
* Microsoft Foundry 中的模型

因此：

> **开发 AI 应用不一定需要从零开始训练模型。**

---

# 14. 易混淆概念

## AI vs Machine Learning

```text
AI
→ 更大的概念

Machine Learning
→ AI 的重要分支
```

---

## Machine Learning vs Deep Learning

```text
Machine Learning
→ 更大的概念

Deep Learning
→ Machine Learning 的一种
```

---

## Training vs Inference

```text
Training
→ 学习

Inference
→ 使用
```

---

## Traditional AI vs Generative AI

```text
传统 AI
→ 分类
→ 预测
→ 检测
→ 分析

Generative AI
→ 生成文本
→ 生成图片
→ 生成代码
```

---

## AI Model vs Database

```text
Database
→ 保存和查询数据

AI Model
→ 学习数据模式
→ 预测或生成
```

---

## AI Workload 选择

```text
图片 / 视频
→ Computer Vision

文本
→ NLP

语音
→ Speech

内容生成
→ Generative AI

文档字段提取
→ Information Extraction
```

---

# 15. 练习题

## 练习题 1

以下哪个最准确地描述 Artificial Intelligence？

A. 只用于数据库管理的技术
B. 让计算机执行通常需要人类智能的任务
C. 只用于创建网站的技术
D. 只用于存储文件的技术

<details>
<summary>查看答案</summary>

**答案：B**

AI 的目标是让计算机系统执行通常需要人类智能才能完成的任务。

</details>

---

## 练习题 2

以下哪个描述正确？

A. Machine Learning 是 AI 的重要分支
B. AI 是 Machine Learning 的子集
C. Deep Learning 是 AI 的唯一形式
D. Machine Learning 和 AI 完全相同

<details>
<summary>查看答案</summary>

**答案：A**

Machine Learning 是 Artificial Intelligence 的重要分支。

</details>

---

## 练习题 3

以下哪个描述正确？

A. Deep Learning 是 Machine Learning 的一种
B. Deep Learning 是数据库技术
C. Deep Learning 不需要数据
D. Deep Learning 只能处理数字

<details>
<summary>查看答案</summary>

**答案：A**

Deep Learning 是 Machine Learning 的一种，通常使用多层神经网络。

</details>

---

## 练习题 4

Training 的主要目的是什么？

A. 删除 AI 模型
B. 使用数据让模型学习
C. 创建数据库
D. 部署网站

<details>
<summary>查看答案</summary>

**答案：B**

Training 是使用数据训练模型，使模型学习数据中的模式。

</details>

---

## 练习题 5

Inference 是什么？

A. 训练 AI 模型
B. 删除 AI 模型
C. 使用训练好的模型处理新的输入
D. 收集训练数据

<details>
<summary>查看答案</summary>

**答案：C**

Inference 是使用已经训练好的模型处理新的输入，并产生预测或生成结果。

</details>

---

## 练习题 6

以下哪个场景最适合 Generative AI？

A. 生成一篇文章
B. 判断数据库是否连接
C. 配置虚拟网络
D. 创建虚拟机

<details>
<summary>查看答案</summary>

**答案：A**

生成文章属于 Generative AI 的典型应用。

</details>

---

## 练习题 7

一个应用需要识别图片中的汽车和行人。应该使用哪种 AI Workload？

A. Speech
B. Natural Language Processing
C. Computer Vision
D. Text-to-Speech

<details>
<summary>查看答案</summary>

**答案：C**

识别图片中的物体属于 Computer Vision。

</details>

---

## 练习题 8

一个应用需要将用户说话的内容转换成文字。应该使用什么？

A. Speech-to-Text
B. Text-to-Speech
C. Image Classification
D. Object Detection

<details>
<summary>查看答案</summary>

**答案：A**

Speech-to-Text 用于将语音转换成文本。

</details>

---

## 练习题 9

一个企业需要从发票中提取：

* 发票号码
* 日期
* 金额

应该使用哪种 AI Workload？

A. Information Extraction
B. Speech
C. Image Generation
D. Text-to-Speech

<details>
<summary>查看答案</summary>

**答案：A**

从文档中提取结构化信息属于 Information Extraction。

</details>

---

## 练习题 10

以下哪个描述最准确？

A. AI 应用一定需要从零训练模型
B. AI 应用可以使用现有的预训练模型或 AI 服务
C. AI 只能处理数字
D. AI 不能处理文本

<details>
<summary>查看答案</summary>

**答案：B**

实际 AI 应用开发中，可以使用预训练模型、Foundation Models 或现有 AI 服务。

</details>

---

## 练习题 11

以下哪种技术最适合分析客户评论的情感？

A. Computer Vision
B. Natural Language Processing
C. Speech
D. Object Detection

<details>
<summary>查看答案</summary>

**答案：B**

情感分析属于 Natural Language Processing。

</details>

---

## 练习题 12

以下哪个场景属于 Generative AI？

A. 判断图片中是否存在汽车
B. 预测房屋价格
C. 根据 Prompt 生成一篇文章
D. 将语音转换成文字

<details>
<summary>查看答案</summary>

**答案：C**

根据 Prompt 生成新的文本属于 Generative AI。

</details>

---

## 练习题 13

以下哪个描述最准确地说明 AI Model 和 Database 的区别？

A. AI Model 主要用于保存数据
B. Database 主要用于学习模式
C. AI Model 可以利用学习到的模式处理新的输入
D. AI Model 和 Database 完全相同

<details>
<summary>查看答案</summary>

**答案：C**

Database 主要保存和查询数据，而 AI Model 可以学习数据中的模式，并处理新的输入。

</details>

---

## 练习题 14

一个工厂需要自动检测产品表面的划痕和缺陷。最适合使用哪种 AI Workload？

A. Speech
B. Computer Vision
C. Text-to-Speech
D. Natural Language Processing

<details>
<summary>查看答案</summary>

**答案：B**

通过图像识别产品缺陷属于 Computer Vision。

</details>

---

## 练习题 15

一个企业需要根据用户输入自动生成产品介绍文案。最适合使用哪种技术？

A. Generative AI
B. Object Detection
C. Speech-to-Text
D. Image Classification

<details>
<summary>查看答案</summary>

**答案：A**

根据输入生成新的文本属于 Generative AI。

</details>

---

# 16. 本章一句话记忆

> **AI 是让计算机执行需要人类智能的任务；Machine Learning 让计算机从数据中学习；Deep Learning 是 Machine Learning 的一种；Generative AI 能够生成新的内容；Training 用于训练模型，Inference 用于使用模型。**

---

# 17. 本章知识结构

```text
Artificial Intelligence
人工智能
│
├── AI Model
│
├── Machine Learning
│   机器学习
│   │
│   └── Deep Learning
│       深度学习
│
├── Generative AI
│   生成式 AI
│
├── Training
│   模型训练
│
└── Inference
    模型推理
```

AI Workloads：

```text
AI Workloads
│
├── Computer Vision
│   └── 图像 / 视频
│
├── Natural Language Processing
│   └── 文本 / 语言
│
├── Speech
│   └── 语音
│
├── Generative AI
│   └── 内容生成
│
└── Information Extraction
    └── 信息提取
```

AI 与传统软件：

```text
传统软件
Input
  ↓
Rules
  ↓
Program
  ↓
Output
```

```text
Machine Learning
Training Data
  ↓
Training
  ↓
AI Model
  ↓
New Input
  ↓
Inference
  ↓
Prediction
```

---

# 🎯 本章最终记忆框架

```text
AI
│
├── Machine Learning
│     └── 从数据中学习
│           └── Deep Learning
│
├── Generative AI
│     └── 生成新的内容
│
└── AI Workloads
      ├── Computer Vision
      ├── NLP
      ├── Speech
      └── Information Extraction
```

模型生命周期：

```text
Training Data
      ↓
Training
      ↓
AI Model
      ↓
Inference
      ↓
Prediction / Generation
```

场景判断：

```text
看到图片 / 视频
→ Computer Vision

看到文本 / 语言
→ NLP

看到语音
→ Speech

看到“生成”
→ Generative AI

看到“从文档提取字段”
→ Information Extraction
```

> **本章核心：先理解 AI 是什么，再理解 AI Model 如何工作，掌握 AI、Machine Learning、Deep Learning 和 Generative AI 的关系，最后能够根据实际问题识别对应的 AI Workload。**
