# 第 10 章 Computer Vision

> Computer Vision（计算机视觉）让系统理解图像和视频中的内容。本章重点区分图像分类、对象检测、OCR 与图像分析。

---

# 1. 学习目标

学习后，你应能根据视觉任务的输出需求，选择恰当的计算机视觉能力，并说明其实际限制与 Responsible AI 风险。

# 2. 常见视觉任务

| 任务 | 目标 | 示例 |
| --- | --- | --- |
| Image Classification | 判断整张图像的类别 | 合格/不合格，猫/狗 |
| Object Detection | 找出对象及其位置 | 找出货架上的所有瓶子 |
| OCR | 从图像读取文字 | 读取路牌、收据、菜单 |
| Image Analysis | 识别场景、标签或描述 | “海滩上有两个人” |
| Face Detection | 检测人脸及位置 | 将人脸区域模糊化 |

# 3. Image Classification 与 Object Detection

```text
“这张照片是否有安全帽？”      → Image Classification
“每个安全帽在哪里？”            → Object Detection
```

分类回答“是什么”；对象检测还回答“在哪里”。

# 4. OCR

OCR（光学字符识别）从图片、照片或扫描件中读取文字。若进一步需要理解“哪一个数字是发票总金额”，则应使用信息提取或文档智能能力。

# 5. 典型应用

* 质检：发现产品外观缺陷；
* 零售：识别货架商品或盘点；
* 交通：从路面图像识别对象；
* 文档数字化：从扫描资料读取文字；
* 内容管理：生成图片描述与标签。

# 6. 使用限制与责任

视觉模型受光照、角度、遮挡、图像质量和训练数据代表性的影响。面向人群的系统尤其应测试不同肤色、年龄、辅助设备和环境；涉及人脸或敏感图像时还要谨慎处理隐私、用途边界和访问权限。

# 7. 练习题

## 练习题 1

在仓库照片中定位所有包裹并在每个包裹外画框，应使用：

A. Object Detection  
B. Image Classification  
C. 情绪分析  
D. Speech-to-Text

<details><summary>查看答案</summary>

**答案：A。** 需要识别多个对象并给出位置。

</details>

## 练习题 2

从停车票照片中读取票号，应使用：

A. OCR  
B. 聚类  
C. Text-to-Speech  
D. 回归

<details><summary>查看答案</summary>

**答案：A。** OCR 用于从图像中读取文字。

</details>

# 8. 一句话记忆

> **整图分类型用 Image Classification；既识别又定位用 Object Detection；读图中文字用 OCR。**
