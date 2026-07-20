# 第4章 AI Workloads（AI 工作负载）

## 学习目标

完成本章学习后，你将能够：

* 理解 AI Workload（AI 工作负载）的概念。
* 了解常见 AI 工作负载及其特点。
* 掌握 Azure AI 服务与 AI Workloads 的对应关系。
* 能够根据业务场景选择合适的 Azure AI 服务。
* 为后续学习 Azure AI Services 打下基础。

---

# 4.1 什么是 AI Workloads？

在人工智能领域，**Workload（工作负载）** 是指 AI 系统需要完成的一类任务。

不同的业务需求对应不同的 AI 工作负载。例如：

* 识别图片中的物体
* 将语音转换为文字
* 翻译不同语言
* 分析文档内容
* 回答用户问题
* 自动生成文章

虽然这些都属于 AI 应用，但它们解决的问题不同，因此使用的 AI 服务也不同。

> 💡 **一句话理解：**
>
> **AI Workload 就是 AI 擅长完成的任务类型。**

AI-901 考试经常会给出一个业务场景，要求选择最适合的 AI 服务，因此理解各种 Workload 的特点十分重要。

---

# 4.2 常见 AI Workloads

Azure AI 中常见的工作负载包括以下几类：

| AI Workload                 | 主要功能           | 常见 Azure 服务                           |
| --------------------------- | -------------- | ------------------------------------- |
| Computer Vision             | 图像识别、目标检测、OCR  | Azure AI Vision                       |
| Natural Language Processing | 文本理解、情感分析、实体识别 | Azure AI Language                     |
| Speech AI                   | 语音识别、语音合成、实时翻译 | Azure AI Speech                       |
| Document Intelligence       | 发票、合同、表单解析     | Azure AI Document Intelligence        |
| Knowledge Mining            | 企业知识搜索、智能问答    | Azure AI Search                       |
| Generative AI               | 文本生成、代码生成、图片生成 | Azure OpenAI Service、Azure AI Foundry |

掌握这些工作负载与 Azure 服务之间的对应关系，是 AI-901 考试的重要内容。

---

# 4.3 Computer Vision（计算机视觉）

## 什么是 Computer Vision？

Computer Vision 是指让计算机"看懂"图片或视频内容的技术。

常见能力包括：

* 图像分类
* 目标检测
* 人脸检测
* OCR（文字识别）
* 图像分析

例如：

* 自动识别照片中的汽车。
* 识别身份证上的文字。
* 检测工厂产品是否存在缺陷。

Azure 中主要使用：

**Azure AI Vision**

---

# 4.4 Natural Language Processing（自然语言处理）

Natural Language Processing（NLP）是让计算机理解和处理自然语言的技术。

常见能力包括：

* 情感分析
* 关键词提取
* 实体识别
* 文本分类
* 自动摘要

例如：

客户留言：

> "物流速度很快，但是包装有一点破损。"

AI 可以分析：

* 情感：积极
* 关键词：物流、包装
* 实体：无

Azure 中主要使用：

**Azure AI Language**

---

# 4.5 Speech AI（语音智能）

Speech AI 用于处理语音数据。

主要能力包括：

* Speech to Text（语音转文字）
* Text to Speech（文字转语音）
* Speech Translation（语音翻译）
* Speaker Recognition（说话人识别）

例如：

用户说：

> "明天下午两点开会。"

AI 可以实时转换成文字，并自动生成会议记录。

Azure 中主要使用：

**Azure AI Speech**

---

# 4.6 Document Intelligence（文档智能）

Document Intelligence 用于理解各种文档。

例如：

* 发票
* 收据
* 合同
* 银行流水
* 表格

AI 可以自动提取：

* 公司名称
* 日期
* 金额
* 地址
* 发票编号

无需人工录入。

Azure 中主要使用：

**Azure AI Document Intelligence**

---

# 4.7 Knowledge Mining（知识挖掘）

Knowledge Mining 用于从大量文档中快速找到所需信息。

例如：

企业拥有：

* PDF
* Word
* Excel
* 邮件
* 图片

AI 可以建立索引，实现：

> "请找出去年所有关于 Azure AI 的项目。"

Azure 中主要使用：

**Azure AI Search**

Knowledge Mining 并不是简单的关键字搜索，而是结合 AI 对内容进行理解，提高搜索效率和准确性。

---

# 4.8 Generative AI（生成式 AI）

Generative AI 是近年来发展最快的 AI 工作负载。

它不仅能够分析数据，还能够**生成新的内容**。

例如：

* 撰写文章
* 编写代码
* 总结会议纪要
* 回答问题
* 生成图片

Azure 中主要使用：

* Azure OpenAI Service
* Azure AI Foundry

生成式 AI 已成为现代 AI 应用的重要组成部分，也是 AI-901 的重点内容。

---

# 4.9 Azure AI Workloads 对照表

| 业务需求     | 推荐 Azure AI 服务                                   |
| -------- | ------------------------------------------------ |
| 图片识别     | Azure AI Vision                                  |
| OCR      | Azure AI Vision / Azure AI Document Intelligence |
| 情感分析     | Azure AI Language                                |
| 文本翻译     | Azure AI Translator                              |
| 语音识别     | Azure AI Speech                                  |
| 文档解析     | Azure AI Document Intelligence                   |
| 企业知识搜索   | Azure AI Search                                  |
| 聊天机器人    | Azure OpenAI Service                             |
| 内容生成     | Azure OpenAI Service                             |
| AI Agent | Azure AI Foundry                                 |

---

# 4.10 企业应用场景

不同的行业会根据业务需求选择不同的 AI 工作负载。

| 行业 | 应用场景   | AI Workload              |
| -- | ------ | ------------------------ |
| 零售 | 商品识别   | Computer Vision          |
| 金融 | 合同解析   | Document Intelligence    |
| 医疗 | 医学影像分析 | Computer Vision          |
| 教育 | 智能学习助手 | Generative AI            |
| 客服 | 智能客服   | Language + Generative AI |
| 制造 | 产品缺陷检测 | Computer Vision          |
| 办公 | 会议纪要生成 | Speech + Generative AI   |

AI-901 考试通常会给出类似场景，要求选择最适合的 Azure AI 服务。
---

# 4.11 本章总结

本章介绍了 AI Workload（AI 工作负载）的概念，以及 Azure AI 中最常见的六类工作负载：

* Computer Vision（计算机视觉）
* Natural Language Processing（自然语言处理）
* Speech AI（语音智能）
* Document Intelligence（文档智能）
* Knowledge Mining（知识挖掘）
* Generative AI（生成式 AI）

这些工作负载分别对应 Azure 提供的不同 AI 服务。学习 AI-901 时，应重点理解每种工作负载适合解决什么问题，而不是死记服务名称。

---

# 🎯 本章重点

* **AI Workload** 是指 AI 系统完成的任务类型。
* **Computer Vision** 用于分析图片和视频。
* **Natural Language Processing（NLP）** 用于理解和分析文本。
* **Speech AI** 用于处理语音数据。
* **Document Intelligence** 用于解析发票、合同、表单等文档。
* **Knowledge Mining** 用于企业知识搜索和信息发现。
* **Generative AI** 用于生成文本、代码、图片等新内容。

---

# ⚠️ 易错点

## 1. OCR ≠ Document Intelligence

很多初学者容易混淆。

**OCR（Optical Character Recognition）**

* 目标：识别图片中的文字。
* 输出：文字内容。

例如：

身份证照片

↓

识别姓名、身份证号码。

---

**Document Intelligence**

不仅能够识别文字，还能够理解文档结构。

例如：

发票

↓

自动提取：

* 发票号码
* 金额
* 日期
* 公司名称
* 税号

因此：

> **Document Intelligence = OCR + 文档理解**

---

## 2. Azure AI Language ≠ Translator

Azure AI Language

主要用于：

* 情感分析
* 实体识别
* 文本分类
* 摘要

并不负责翻译。

---

Azure AI Translator

专门负责：

不同语言之间的自动翻译。

例如：

中文

↓

英文

↓

日文

---

## 3. Computer Vision ≠ Speech AI

Computer Vision

处理：

* 图片
* 视频

---

Speech AI

处理：

* 声音
* 语音

考试经常利用这两个服务进行干扰。

---

## 4. Knowledge Mining ≠ Generative AI

Knowledge Mining

重点：

> 找到已有的信息。

例如：

企业文档搜索。

---

Generative AI

重点：

> 创造新的内容。

例如：

生成文章。

---

## 5. AI Workload 与 Azure 服务不要混淆

例如：

Computer Vision

属于：

**AI Workload**

---

Azure AI Vision

属于：

**Azure AI Service**

考试很喜欢考：

> "这是 Workload 还是 Azure 服务？"

一定要区分。

---

# 📌 一分钟速记

| 工作负载                  | 一句话记忆 | Azure 服务                                |
| --------------------- | ----- | --------------------------------------- |
| Computer Vision       | 看图片   | Azure AI Vision                         |
| NLP                   | 看文字   | Azure AI Language                       |
| Speech                | 听声音   | Azure AI Speech                         |
| Document Intelligence | 看文档   | Azure AI Document Intelligence          |
| Knowledge Mining      | 找知识   | Azure AI Search                         |
| Generative AI         | 创造内容  | Azure OpenAI Service / Azure AI Foundry |

---

# 📝 本章练习

## 一、单项选择题

### 1. AI Workload 指的是：

A. Azure 的计费方式

B. AI 系统需要完成的任务类型

C. Azure 区域

D. 虚拟机规格

**答案：** B

---

### 2. 某企业希望自动识别发票中的金额和日期，应使用哪种 AI Workload？

A. Speech AI

B. Document Intelligence

C. NLP

D. Generative AI

**答案：** B

---

### 3. 用户上传一张图片，希望识别图片中的物体，应选择：

A. Azure AI Language

B. Azure AI Vision

C. Azure AI Speech

D. Azure AI Translator

**答案：** B

---

### 4. 客户希望分析评论是积极还是消极，应使用：

A. Computer Vision

B. Speech AI

C. Azure AI Language

D. Azure AI Search

**答案：** C

---

### 5. 用户希望把语音实时转换成文字，应使用：

A. Azure AI Vision

B. Azure AI Search

C. Azure AI Speech

D. Document Intelligence

**答案：** C

---

### 6. 企业希望员工能够搜索公司内部 PDF、Word 和邮件内容，应优先考虑：

A. Azure AI Search

B. Azure AI Vision

C. Azure AI Speech

D. Translator

**答案：** A

---

### 7. 希望 AI 自动编写会议纪要，应优先考虑：

A. Generative AI

B. OCR

C. Face Detection

D. Object Detection

**答案：** A

---

### 8. 下列哪项属于 Computer Vision 的典型应用？

A. 情感分析

B. 图片分类

C. 文本摘要

D. 语音翻译

**答案：** B

---

## 二、判断题

### 1. AI Workload 与 Azure AI 服务是同一个概念。

**答案：** ✘ 错误

---

### 2. OCR 只能识别文字，而 Document Intelligence 还能理解文档结构。

**答案：** ✔ 正确

---

### 3. Azure AI Language 可以完成情感分析。

**答案：** ✔ 正确

---

### 4. Knowledge Mining 的主要目标是生成新的内容。

**答案：** ✘ 错误

---

### 5. Azure AI Speech 可以完成语音识别。

**答案：** ✔ 正确

---

## 三、场景题（AI-901 真题风格）

### 场景 1

一家物流公司希望：

* 自动读取快递面单；
* 提取收件人、地址和运单号。

应该优先选择哪项 Azure AI 服务？

A. Azure AI Vision

B. Azure AI Speech

C. Azure AI Document Intelligence

D. Azure AI Language

**答案：** C

---

### 场景 2

一家电商平台希望：

根据客户评论自动判断：

* 满意
* 一般
* 不满意

应该选择：

A. Azure AI Language

B. Azure AI Vision

C. Azure AI Speech

D. Azure AI Search

**答案：** A

---

### 场景 3

一家制造企业希望：

利用摄像头自动检测产品是否存在划痕或缺陷。

应选择：

A. Computer Vision

B. NLP

C. Speech AI

D. Translator

**答案：** A

---

# 📚 本章知识检查

学习完本章后，请确认自己能够回答以下问题：

* □ 什么是 AI Workload？
* □ 能否说出六种常见 AI Workload？
* □ 是否能够区分 OCR 与 Document Intelligence？
* □ 是否能够区分 Azure AI Language 与 Translator？
* □ 是否能够根据业务场景选择合适的 Azure AI 服务？
* □ 是否理解 AI Workload 与 Azure AI 服务之间的关系？

如果以上问题都能够回答，说明你已经掌握了 AI-901 关于 AI Workloads 的核心内容，可以继续学习下一章《Azure AI Foundry 概述》。

---

# 🔗 Microsoft Learn 对应学习内容

本章对应 Microsoft Learn 中 **Describe AI workloads and considerations（描述 AI 工作负载及其注意事项）** 的相关内容，也是 AI-901 考试大纲中的重要知识点。

建议在学习完本章后，结合 Azure Portal 或 Microsoft Learn 的在线示例进一步了解各项 Azure AI 服务的实际使用方式，加深对不同 AI Workload 的理解。
