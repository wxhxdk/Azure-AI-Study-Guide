# 第 4 章 AI Workloads

> 本章梳理 AI-901 常见的 AI 工作负载（AI Workloads）。考试的关键是从“输入、目标和输出”判断应使用哪一类 AI 能力，而不是只记服务名称。

---

# 0. AI-901 考试介绍（简版）

AI-901 会通过业务场景考查 AI 工作负载选择。例如：从发票照片中读取金额、把会议语音转成文本、判断评论情绪、根据问题生成答案，分别需要不同的 AI 能力。

---

# 1. 本章学习目标

完成本章后，你应该能够：

* 说明 AI Workload 的含义；
* 区分计算机视觉、自然语言处理、语音、生成式 AI 和信息提取；
* 根据输入与期望输出选择合适的工作负载；
* 理解多模态应用如何组合多种能力；
* 区分 OCR、图像分析、文档智能和生成式 AI。

---

# 2. 什么是 AI Workload

**AI Workload** 是按任务类型划分的一类 AI 能力。它回答的问题是：系统要处理什么形式的信息，并要完成什么样的智能任务？

选择工作负载时，可按以下顺序判断：

```text
输入是什么？
文字 / 图像 / 文档 / 音频 / 多种形式
        ↓
希望得到什么？
分类、提取、理解、转写、合成或生成
        ↓
选择最匹配的 AI Workload
```

AI-901 常见工作负载如下：

| 工作负载 | 核心对象 | 典型目标 |
| --- | --- | --- |
| Computer Vision | 图像、视频 | 看懂视觉内容 |
| Natural Language Processing | 文本、语言 | 理解或分析语言 |
| Speech | 语音、音频 | 语音识别、语音合成、翻译 |
| Generative AI | 提示与上下文 | 生成文本、图像、代码等内容 |
| Information Extraction | 表单、发票、合同等文档 | 提取结构化字段和内容 |

---

# 3. Computer Vision

**Computer Vision（计算机视觉）** 让系统从图像或视频中识别对象、文字、场景、位置和其他视觉特征。

## 3.1 常见任务

* **Image classification（图像分类）**：判断整张图像属于什么类别，例如“猫”或“狗”；
* **Object detection（对象检测）**：识别图像中的对象并标出位置，例如找出货架上所有商品；
* **Image analysis（图像分析）**：生成图像描述、标签、颜色或场景信息；
* **OCR（光学字符识别）**：从图像中读取印刷或手写文字；
* **Face detection（人脸检测）**：检测图像中是否存在人脸及其位置。它不等同于确认某人的身份。

## 3.2 典型场景

```text
监控画面中定位安全帽       → Object detection
从菜单照片读出菜品名称     → OCR
自动为商品图片生成描述     → Image analysis
将质检图片分为合格/不合格 → Image classification
```

## 3.3 考点提示

若题干需要“在哪里”，通常是对象检测；若只需判断“是什么类别”，通常是图像分类；若核心是读取图片中的文字，选择 OCR。

---

# 4. Natural Language Processing

**Natural Language Processing（NLP，自然语言处理）** 让系统分析、理解和处理人类书面语言。

## 4.1 常见任务

* **Sentiment analysis（情绪分析）**：判断文本表达正面、负面或中性态度；
* **Key phrase extraction（关键短语提取）**：抽取文本主题和重点短语；
* **Named entity recognition（命名实体识别）**：识别人名、地点、组织、日期等实体；
* **Language detection（语言检测）**：判断文本使用的语言；
* **Text classification（文本分类）**：例如把邮件分类为“订单、投诉、咨询”。

## 4.2 典型场景

```text
分析客户评价满意度         → Sentiment analysis
从新闻中识别人名和地点     → Named entity recognition
将工单路由到不同服务团队   → Text classification
提取会议纪要中的主题       → Key phrase extraction
```

NLP 主要是**分析和理解已有文本**；当需求变为“根据指令撰写新的内容”时，通常更接近生成式 AI。

---

# 5. Speech

**Speech（语音）** 工作负载处理口语音频，使应用能够听懂、说出或翻译语音。

## 5.1 常见任务

* **Speech-to-Text（语音转文本）**：将会议、电话或语音命令转写为文字；
* **Text-to-Speech（文本转语音）**：把文字自然地朗读出来；
* **Speech translation（语音翻译）**：将一种语言的语音转成另一种语言的文本或语音；
* **Speaker recognition（说话人识别）**：在经过适当设计和授权的场景中，区分或验证说话人。

## 5.2 典型场景

```text
会议实时字幕               → Speech-to-Text
无障碍阅读应用朗读文章     → Text-to-Speech
跨语言客服的实时口译       → Speech translation
```

不要把 Speech-to-Text 与 OCR 混淆：前者的输入是**音频**，后者的输入是**图像或扫描文档**。

---

# 6. Generative AI

**Generative AI（生成式 AI）** 使用模型基于提示（Prompt）和上下文创建新内容，例如文字、摘要、图像、代码或对话回复。

## 6.1 基本流程

```text
用户提示 + 系统指令 + 相关上下文
              ↓
        生成式 AI 模型
              ↓
       新生成的内容或回答
```

## 6.2 常见场景

* 根据知识库回答员工问题；
* 起草邮件、报告、营销文案或代码；
* 总结长文档或会议记录；
* 创建图像、设计草图或多模态内容；
* 通过 AI Agent 结合工具完成多步骤任务。

## 6.3 使用注意

生成式 AI 可能给出看似合理但不准确的内容。实际应用应使用清晰的指令、可靠的上下文来源、内容安全控制和人工审核。对于要求事实准确的场景，可通过 Grounding（将回答建立在受控数据源上）降低幻觉风险。

---

# 7. Information Extraction

**Information Extraction（信息提取）** 从半结构化或非结构化文档中识别并提取有业务意义的数据，将其转成可使用的结构化结果。

## 7.1 典型输入与输出

```text
输入：发票、收据、表单、合同、身份证明、扫描 PDF
        ↓
识别文字、布局、表格、键值对和字段关系
        ↓
输出：供应商、日期、金额、地址、条款等结构化字段
```

## 7.2 与 OCR 的关系

OCR 专注于“读出字符”。信息提取通常进一步理解文档结构和字段含义。

```text
从图片读出“总计：¥1,280”      → OCR
把 ¥1,280 识别为发票总金额字段 → Information Extraction
```

## 7.3 典型场景

* 自动处理报销单与采购发票；
* 从合同中提取到期日、当事方和关键条款；
* 从申请表中读取姓名、地址和证件号码；
* 将扫描档案转为可搜索、可分析的数据。

---

# 8. 组合与多模态应用

真实解决方案常组合多个工作负载。例如，客户服务应用可先用 Speech-to-Text 转写电话，再用 NLP 分析情绪，最后由生成式 AI 起草回复；文档处理应用可用 OCR 读取文字，再用信息提取生成业务字段。

```text
音频 → Speech-to-Text → NLP / Generative AI → 文本回复或业务动作

扫描发票 → OCR → Information Extraction → 财务系统字段
```

组合能力时，要分别评估每一步的准确性、延迟、隐私和错误传播风险。

---

# 9. AI-901 考试重点

| 业务需求 | 应优先想到的工作负载 |
| --- | --- |
| 从照片或视频理解场景、对象 | Computer Vision |
| 从图片中读取文字 | OCR / Computer Vision |
| 判断评论好坏、抽取实体 | NLP |
| 把录音转写为文字 | Speech-to-Text |
| 让应用朗读文本 | Text-to-Speech |
| 按提示写出新内容或回答 | Generative AI |
| 从发票、表单、合同抽取字段 | Information Extraction |

---

# 10. 易混淆概念

## OCR vs Information Extraction

* **OCR**：识别文字本身；
* **Information Extraction**：识别文字并理解其在文档中的字段、布局和业务含义。

## Image Classification vs Object Detection

* **Image Classification**：给整张图一个或多个类别；
* **Object Detection**：找出多个对象，并给出它们的位置。

## NLP vs Generative AI

* **NLP**：侧重分析已有语言，例如情绪、实体和分类；
* **Generative AI**：侧重依据提示创建新的内容。

## Speech-to-Text vs Text-to-Speech

* **Speech-to-Text**：听音频并输出文本；
* **Text-to-Speech**：读取文本并输出语音。

---

# 11. 练习题

## 练习题 1

一家零售商希望从商品照片中定位每一件商品，并标出其位置。应使用：

A. Image classification  
B. Object detection  
C. OCR  
D. Sentiment analysis

<details><summary>查看答案</summary>

**答案：B。** 题干要求定位多个对象的位置，属于对象检测。

</details>

## 练习题 2

应用需要将呼叫中心录音自动转为客服可搜索的文字记录。应使用：

A. OCR  
B. Text-to-Speech  
C. Speech-to-Text  
D. Object detection

<details><summary>查看答案</summary>

**答案：C。** 输入是音频，目标是输出文本。

</details>

## 练习题 3

系统需要从发票 PDF 中提取供应商名称、发票日期和应付金额。最匹配的是：

A. Sentiment analysis  
B. Information Extraction  
C. Image classification  
D. Speech translation

<details><summary>查看答案</summary>

**答案：B。** 该需求不仅要读出文字，还要将字段转为结构化数据。

</details>

## 练习题 4

根据员工手册和用户提问生成一段回答，最匹配的工作负载是：

A. NLP 情绪分析  
B. Generative AI  
C. OCR  
D. 对象检测

<details><summary>查看答案</summary>

**答案：B。** 题目要求基于上下文生成新的自然语言回答。

</details>

## 练习题 5

判断客户评论是正面、负面还是中性，最匹配的是：

A. Sentiment analysis  
B. Speech synthesis  
C. Image analysis  
D. Document extraction

<details><summary>查看答案</summary>

**答案：A。** 情绪分析是 NLP 的典型任务。

</details>

---

# 12. 本章一句话记忆

> **看图像与视频用 Computer Vision，理解已有文本用 NLP，处理声音用 Speech，按提示创建新内容用 Generative AI，从业务文档抽取字段用 Information Extraction。**

# 13. 本章知识结构

```text
AI Workloads
├─ Computer Vision
│  ├─ Classification
│  ├─ Object Detection
│  └─ OCR
├─ Natural Language Processing
│  ├─ Sentiment
│  └─ Entity / Key Phrase Extraction
├─ Speech
│  ├─ Speech-to-Text
│  └─ Text-to-Speech
├─ Generative AI
│  └─ Prompt → New Content
└─ Information Extraction
   └─ Document → Structured Fields
```
