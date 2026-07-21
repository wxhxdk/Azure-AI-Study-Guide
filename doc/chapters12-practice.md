# 第 12 章 AI-901 综合练习

> 本章用场景题整合 AI 概念、Responsible AI、AI Workloads、Microsoft Foundry 与生成式 AI 的核心知识。

---

# 1. 复习方法

面对每一道场景题，按以下顺序判断：

```text
输入是什么？ → 目标输出是什么？ → 属于哪种 AI 工作负载？
       ↓
是否涉及模型、部署、提示、工具或数据？
       ↓
是否存在公平、安全、隐私、透明或责任问题？
```

# 2. 综合练习

## 练习题 1：机器学习类型

零售商没有预先定义的客户类别，想根据购买行为将客户自动分组。应使用：

A. Regression  
B. Classification  
C. Clustering  
D. OCR

<details><summary>查看答案</summary>

**答案：C。** 没有标签、依据相似性自动分组，属于无监督学习中的聚类。

</details>

## 练习题 2：评估指标

疾病筛查系统最担心漏掉真实患病者，应更重视：

A. Precision  
B. Recall  
C. 聚类数量  
D. Token 数量

<details><summary>查看答案</summary>

**答案：B。** Recall 关注真实正类被成功识别的比例，适合漏检代价高的场景。

</details>

## 练习题 3：Responsible AI

招聘模型对某类候选人的通过率明显更低，团队应首先调查：

A. Fairness  
B. Text-to-Speech  
C. OCR  
D. Context Window

<details><summary>查看答案</summary>

**答案：A。** 不同群体可能受到不合理差别影响，首先对应公平性。

</details>

## 练习题 4：视觉能力

应用需要在生产线照片中标记每一个缺陷的位置。应使用：

A. Image Classification  
B. Object Detection  
C. 情绪分析  
D. 语音翻译

<details><summary>查看答案</summary>

**答案：B。** 需要识别对象并给出位置。

</details>

## 练习题 5：语音能力

会议应用需将演讲者的语音实时显示为字幕。应使用：

A. OCR  
B. Speech-to-Text  
C. Text-to-Speech  
D. 文档提取

<details><summary>查看答案</summary>

**答案：B。** 将音频转换为文字是语音转文本。

</details>

## 练习题 6：信息提取

财务部门要从扫描发票中提取供应商、日期和总金额，并写入业务系统。应使用：

A. OCR only  
B. Information Extraction  
C. 图像分类  
D. 回归

<details><summary>查看答案</summary>

**答案：B。** 该需求需要识别字段的结构和业务含义。

</details>

## 练习题 7：Microsoft Foundry

团队想在编写应用前比较多个生成模型对同一组提示的表现，最适合：

A. Playground  
B. Deployment  
C. Test Data  
D. OCR

<details><summary>查看答案</summary>

**答案：A。** Playground 适合快速测试模型、提示和参数。

</details>

## 练习题 8：模型部署

模型已经选定，现在 Web 应用需要调用它。下一步是：

A. Clustering  
B. 创建 Deployment  
C. 创建标签  
D. 进行 OCR

<details><summary>查看答案</summary>

**答案：B。** 部署将模型提供为可调用服务。

</details>

## 练习题 9：生成式 AI

根据内部手册和员工问题生成答案，并尽量避免编造，应优先：

A. 增加 Temperature  
B. 使用授权文档作为 Grounding 上下文  
C. 删除系统提示  
D. 改用聚类

<details><summary>查看答案</summary>

**答案：B。** 将回答建立在相关、受控资料上可降低无依据输出。

</details>

## 练习题 10：AI Agent

订单助理要先查询库存系统，再生成回复。最需要的是：

A. 受控 Tool / Connection  
B. 图像分类  
C. 仅提高 Temperature  
D. 无监督学习

<details><summary>查看答案</summary>

**答案：A。** Agent 通过受控工具获取真实业务结果。

</details>

# 3. 高频概念速记

```text
Regression       → 预测数值
Classification   → 预测类别
Clustering       → 无标签自动分组

Fairness         → 避免不合理群体差异
Transparency     → 告知 AI 的作用与限制
Accountability   → 人和组织承担责任

OCR              → 读图片中的字
Information Extraction → 读字并提取业务字段
Speech-to-Text   → 音频转文字
Text-to-Speech   → 文字转音频

Model Catalog    → 选择模型
Playground       → 试验模型与提示
Deployment       → 让应用调用模型
Grounding        → 用受控事实支撑回答
```

# 4. 最后检查清单

考前应能快速回答：

* 何时选回归、分类、聚类？
* 何时重视 Precision，何时重视 Recall？
* 六项 Responsible AI 原则分别解决什么风险？
* 图像、文本、语音、文档和生成内容各对应哪种工作负载？
* 模型目录、Playground 和部署各自做什么？
* 如何通过提示、Grounding、工具权限和人工监督提高生成式 AI 应用的可靠性？

# 5. 一句话记忆

> **AI-901 的核心不是死记服务名称，而是从业务场景识别输入、输出、风险和约束，再选择合适的 AI 工作负载、模型能力与治理措施。**
