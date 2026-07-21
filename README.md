# AI-901 学习指南

> 面向 **Microsoft Azure AI Fundamentals（AI-901）** 认证考试的中文学习手册。
> 本项目根据 Microsoft 当前公布的 AI-901 考试技能范围整理，结合 AI 基础知识、Azure AI 和 Microsoft Foundry 的实际应用进行学习。

---

# 📚 关于本项目

本项目是一份面向 **AI-901 认证考试**的中文学习资料。

目标是帮助学习者系统掌握：

* Artificial Intelligence（AI）基础概念
* Machine Learning 基础
* Deep Learning 基础
* Responsible AI
* AI Workloads
* Generative AI
* Foundation Models
* Microsoft Foundry
* Prompt Engineering
* AI Agents
* Computer Vision
* Natural Language Processing
* Speech
* Information Extraction

本项目不仅关注考试知识点，也尽量结合 Azure 和 Microsoft Foundry 的实际应用场景，帮助理解 AI 技术在真实项目中的使用方式。

---

# 🎓 AI-901 考试介绍

## 什么是 AI-901？

**AI-901: Microsoft Azure AI Fundamentals** 是 Microsoft 面向 AI 初学者和技术人员推出的基础级认证考试。

该考试主要用于验证考生是否理解：

* AI 的基本概念
* Machine Learning 的基础知识
* Generative AI 的基本概念
* Responsible AI
* 不同 AI Workloads 的特点
* Microsoft Foundry 中 AI 解决方案的基本实现方式
* Azure AI 服务和工具的基本应用场景

AI-901 更关注：

> **理解 AI 技术、识别 AI 工作负载，并选择适合的 AI 解决方案。**

它并不要求考生成为 AI 算法专家，也不是以复杂数学推导为主要考察内容。

因此，学习重点应该放在：

```text
理解概念
    ↓
识别场景
    ↓
选择 AI Workload
    ↓
选择合适的模型或服务
    ↓
理解基本实现方式
```

---

## AI-901 适合哪些人？

AI-901 适合：

* AI 初学者
* 软件开发人员
* 云计算工程师
* Azure 初学者
* 希望进入 AI 领域的技术人员
* 希望了解 Generative AI 的开发人员
* 准备进一步学习 Azure AI、Machine Learning 或 Microsoft Foundry 的人员

如果具备一定的编程或云计算基础，通常可以更快理解 AI 服务和实际应用场景。

AI-901 属于基础级认证，通常不要求具备高级数学或深度学习算法背景。

---

# 📊 AI-901 最新考试范围

根据 Microsoft 当前公布的 AI-901 Skills Measured，考试主要分为两个部分：

| 考试领域                            |     权重 |
| ------------------------------- | -----: |
| 识别 AI 概念和功能                     | 40–45% |
| 使用 Microsoft Foundry 实现 AI 解决方案 | 55–60% |

这意味着当前 AI-901 的学习重点已经明显偏向：

> **Microsoft Foundry + Generative AI + AI 应用实现**

因此，本项目不会只介绍传统 AI 理论，而是按照：

```text
AI 基础
    ↓
Machine Learning
    ↓
Responsible AI
    ↓
AI Workloads
    ↓
Microsoft Foundry
    ↓
Generative AI
    ↓
Prompt Engineering
    ↓
AI Agents
    ↓
具体 AI 解决方案
```

逐步学习。

---

# 🧭 AI-901 学习重点

整个考试可以理解为三个层次：

```text
第一层
理解 AI 基础概念
        ↓
第二层
识别不同 AI Workloads 和模型
        ↓
第三层
使用 Microsoft Foundry 实现 AI 解决方案
```

核心知识结构：

```text
AI 基础
│
├── Artificial Intelligence
├── Machine Learning
├── Deep Learning
├── Generative AI
└── Responsible AI

AI Workloads
│
├── Computer Vision
├── Natural Language Processing
├── Speech
├── Generative AI
└── Information Extraction

Microsoft Foundry
│
├── Model Catalog
├── Model Deployment
├── Generative AI Models
├── Prompt Engineering
├── AI Agents
├── Foundry Tools
└── Foundry SDK
```

---

# 📖 学习目录

## 第一部分：AI 基础概念

### 第1章 AI 基础概念

主要内容：

* Artificial Intelligence
* AI Model
* Machine Learning
* Deep Learning
* Generative AI
* Training
* Inference
* AI 的常见应用
* AI 与传统软件的区别
* AI Workloads 基础

📄 [第1章 AI 基础概念](chapters/01-ai-concepts.md)

---

### 第2章 Machine Learning 基础

主要内容：

* Machine Learning
* Supervised Learning
* Unsupervised Learning
* Regression
* Classification
* Clustering
* Features
* Labels
* Training
* Validation
* Testing
* Model Evaluation

📄 [第2章 Machine Learning 基础](chapters/02-machine-learning.md)

---

### 第3章 Responsible AI

主要内容：

* Responsible AI
* Fairness
* Reliability and Safety
* Privacy and Security
* Inclusiveness
* Transparency
* Accountability
* AI 风险
* Responsible AI 实践

📄 [第3章 Responsible AI](chapters/03-responsible-ai.md)

---

### 第4章 AI Workloads

主要内容：

* AI Workloads
* Computer Vision
* Natural Language Processing
* Speech
* Generative AI
* Information Extraction
* 不同 AI Workload 的选择

📄 [第4章 AI Workloads](chapters/04-ai-workloads.md)

---

# 第二部分：Microsoft Foundry 与 AI 应用

### 第5章 Microsoft Foundry

主要内容：

* Microsoft Foundry 是什么
* Foundry Projects
* Model Catalog
* 模型选择
* 模型部署
* Playground
* Foundry Tools
* Foundry SDK
* AI 应用开发生命周期

📄 [第5章 Microsoft Foundry](chapters/05-microsoft-foundry.md)

---

### 第6章 Generative AI Models

主要内容：

* Foundation Models
* Large Language Models
* Multimodal Models
* Generative AI Models
* 模型能力
* 模型选择
* 模型部署
* Model Parameters
* Token
* Context
* 模型推理

📄 [第6章 Generative AI Models](chapters/06-generative-ai-models.md)

---

### 第7章 Prompt Engineering

主要内容：

* Prompt
* System Prompt
* User Prompt
* Prompt Engineering
* Prompt 结构
* Prompt 优化
* Grounding
* Context
* 模型参数

📄 [第7章 Prompt Engineering](chapters/07-prompt-engineering.md)

---

### 第8章 AI Agents

主要内容：

* AI Agent
* Agent Instructions
* Agent Tools
* Agent 工作流程
* Single Agent
* Agent 测试
* Agent 与普通 Chatbot 的区别

📄 [第8章 AI Agents](chapters/08-ai-agents.md)

---

### 第9章 Text and Speech AI

主要内容：

* Natural Language Processing
* Text Analysis
* Speech Recognition
* Speech-to-Text
* Text-to-Speech
* Azure Speech
* Language AI
* Text 与 Speech AI 应用

📄 [第9章 Text and Speech AI](chapters/09-text-and-speech.md)

---

### 第10章 Computer Vision

主要内容：

* Computer Vision
* Image Analysis
* OCR
* Object Detection
* Image Classification
* Face Detection
* Multimodal Vision
* Image Generation

📄 [第10章 Computer Vision](chapters/10-computer-vision.md)

---

### 第11章 Information Extraction

主要内容：

* Information Extraction
* Document Intelligence
* Content Understanding
* 文档分析
* 数据提取
* 结构化数据
* 非结构化数据
* AI 驱动的信息提取

📄 [第11章 Information Extraction](chapters/11-information-extraction.md)

---

# 第三部分：AI-901 综合复习

### 第12章 AI-901 综合练习

主要内容：

* AI 基础概念练习
* Machine Learning 练习
* Responsible AI 练习
* AI Workloads 练习
* Microsoft Foundry 练习
* Generative AI 练习
* Prompt Engineering 练习
* AI Agents 练习
* Computer Vision 练习
* Speech 练习
* Information Extraction 练习

📄 [第12章 AI-901 综合练习](chapters/12-practice.md)

---

# 🧭 推荐学习路线

建议按照以下顺序学习：

```text
第1章
AI 基础概念
   ↓
第2章
Machine Learning
   ↓
第3章
Responsible AI
   ↓
第4章
AI Workloads
   ↓
第5章
Microsoft Foundry
   ↓
第6章
Generative AI Models
   ↓
第7章
Prompt Engineering
   ↓
第8章
AI Agents
   ↓
第9章
Text & Speech
   ↓
第10章
Computer Vision
   ↓
第11章
Information Extraction
   ↓
第12章
综合练习
```

---

# 🧠 学习方法

推荐采用：

```text
理解概念
    ↓
学习 Azure / Microsoft Foundry 服务
    ↓
理解实际应用场景
    ↓
完成章节练习题
    ↓
整理易错知识点
    ↓
综合练习
```

学习每个 AI 服务时，建议重点理解：

1. **它是什么？**
2. **解决什么问题？**
3. **输入是什么？**
4. **输出是什么？**
5. **什么时候应该使用？**
6. **与其他服务有什么区别？**

不要只记忆服务名称。

真正需要掌握的是：

> **在什么场景下，为什么选择这个 AI 服务或模型。**

---

# 📝 每章内容结构

每个章节统一按照以下结构整理：

```text
0. AI-901 考试介绍（简版）
1. 本章学习目标
2. 核心概念
3. Azure / Microsoft Foundry 相关服务
4. 实际应用场景
5. 核心知识总结
6. AI-901 考试重点
7. 易混淆概念
8. 练习题
9. 本章一句话记忆
10. 本章知识结构
```

每章的内容都尽量做到：

> **理解 → 对比 → 场景 → 考点 → 练习**

---

# 🗺️ AI-901 核心知识地图

```text
Artificial Intelligence
│
├── Machine Learning
│     ├── Supervised Learning
│     ├── Unsupervised Learning
│     ├── Regression
│     ├── Classification
│     └── Clustering
│
├── Deep Learning
│
├── Responsible AI
│     ├── Fairness
│     ├── Reliability
│     ├── Privacy
│     ├── Inclusiveness
│     ├── Transparency
│     └── Accountability
│
├── AI Workloads
│     ├── Computer Vision
│     ├── NLP
│     ├── Speech
│     ├── Generative AI
│     └── Information Extraction
│
└── Microsoft Foundry
      │
      ├── Models
      │     ├── Foundation Models
      │     ├── LLM
      │     └── Multimodal Models
      │
      ├── Prompt
      │     ├── System Prompt
      │     ├── User Prompt
      │     └── Prompt Engineering
      │
      ├── AI Agents
      │     ├── Instructions
      │     ├── Tools
      │     └── Single Agent
      │
      ├── Vision
      │
      ├── Speech
      │
      └── Information Extraction
```

---

# 🔑 AI-901 高频关键词

```text
Artificial Intelligence
Machine Learning
Deep Learning
Generative AI
Foundation Model
Large Language Model
Multimodal Model
Token
Context
Prompt
System Prompt
User Prompt
Prompt Engineering
AI Agent
Tool
Computer Vision
Natural Language Processing
Speech
OCR
Information Extraction
Responsible AI
Fairness
Reliability
Privacy
Inclusiveness
Transparency
Accountability
Microsoft Foundry
Model Catalog
Model Deployment
Foundry Tools
Foundry SDK
```

---

# 🛠️ Azure AI 学习资源

建议优先使用 Microsoft 官方学习资源：

* Microsoft Learn
* AI-901 官方考试页面
* AI-901 Skills Measured
* Microsoft Foundry 文档
* Azure AI 服务文档

本项目主要用于：

* 中文理解
* 知识整理
* 考试复习
* 概念对比
* 练习题训练

---

# 📌 学习注意事项

AI-901 考试内容和技能范围可能随着 Microsoft 的更新而变化。

因此，本项目中的内容主要用于学习和复习。

在参加正式考试之前，应再次确认 Microsoft 官方最新的：

* AI-901 Exam Details
* AI-901 Skills Measured
* Microsoft Learn 学习内容

并以官方信息作为最终参考。

---

# 🚀 学习目标

完成本学习手册后，希望能够达到：

```text
理解 AI 基础
      ↓
理解 Machine Learning
      ↓
理解 Responsible AI
      ↓
识别不同 AI Workloads
      ↓
理解 Generative AI
      ↓
掌握 Microsoft Foundry 基础
      ↓
理解 Prompt Engineering
      ↓
理解 AI Agents
      ↓
了解 Vision / Speech / Information Extraction
      ↓
完成 AI-901 考试准备
```

---

# 📊 当前学习进度

| 章节   | 内容                     | 状态 |
| ---- | ---------------------- | -- |
| 第1章  | AI 基础概念                | ⬜  |
| 第2章  | Machine Learning 基础    | ⬜  |
| 第3章  | Responsible AI         | ⬜  |
| 第4章  | AI Workloads           | ⬜  |
| 第5章  | Microsoft Foundry      | ⬜  |
| 第6章  | Generative AI Models   | ⬜  |
| 第7章  | Prompt Engineering     | ⬜  |
| 第8章  | AI Agents              | ⬜  |
| 第9章  | Text and Speech AI     | ⬜  |
| 第10章 | Computer Vision        | ⬜  |
| 第11章 | Information Extraction | ⬜  |
| 第12章 | AI-901 综合练习            | ⬜  |

---

# 📖 推荐学习顺序

> **先理解 AI 基础 → 再理解 Machine Learning → 掌握 Responsible AI → 理解不同 AI Workloads → 学习 Microsoft Foundry → 深入 Generative AI → 学习 Prompt 和 AI Agents → 学习具体 AI 解决方案 → 最后通过综合练习进行查漏补缺。**

---

# 🎯 最终目标

本项目希望建立一套完整的 AI-901 学习路径：

```text
AI 基础知识
      ↓
Machine Learning
      ↓
Responsible AI
      ↓
AI Workloads
      ↓
Microsoft Foundry
      ↓
Generative AI
      ↓
Prompt Engineering
      ↓
AI Agents
      ↓
Azure AI Solutions
      ↓
AI-901 综合练习
      ↓
AI-901 Certification
```

> **目标不是单纯背题通过考试，而是通过 AI-901 建立 Azure AI 和 Generative AI 的基础知识体系，为后续学习 Azure AI、Machine Learning、Microsoft Foundry 和 AI 应用开发打下基础。**

---

## ⚠️ 免责声明

本项目是个人学习资料整理，不是 Microsoft 官方考试题库，也不代表 Microsoft 官方认证内容。

考试内容和技能测评范围可能会随着 Microsoft 的更新而发生变化。

准备考试时，请始终以 Microsoft 官方最新公布的考试信息和学习资料为最终参考依据。
