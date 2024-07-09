---
audience: end-user
title: 使用查询建模器
description: 了解如何使用查询建模器。
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 8%

---

# 使用查询建模器 {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="查询建模器"
>abstract="从数据库中为收件人或任何其他架构（也称为定向维度）定义筛选标准。"

查询建模器简化了根据各种条件筛选数据库的过程。 此外，查询建模器可以高效地管理非常复杂和长的查询，提供增强的灵活性和精确度。 此外，它支持条件中的预定义过滤器，使您能够轻松优化查询，同时利用高级表达式和运算符实现全面的受众定位和分段策略。

## 访问查询建模器

在每个需要定义规则以过滤数据的环境下都有查询建模器可用。

| 使用情况 | 示例 |
|  ---  |  ---  |
| **定义受众**：指定要在合成中定位的群体，并根据您的需求轻松创建新受众。 | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **自定义工作流活动**：在构成活动中应用规则，例如 **Split** 和 **调解**，以符合您的特定要求。 [了解有关组合活动的更多信息](../compositions/activities/about-activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## 查询建模器接口 {#interface}

查询建模器提供了一个中央画布，您可以在其中构建查询，以及一个右窗格，提供有关查询的信息。

![](assets/query-interface.png){zoomable="yes"}

### 中央画布 {#canvas}

在查询建模器中心画布上，您可以添加和组合构建查询的不同组件。 [了解如何构建查询](build-query.md)

位于画布右上角的工具栏提供了一些选项，用于轻松处理查询组件并在画布中导航：

* **多选模式**：选择多个筛选组件以将其复制并粘贴到您选择的位置。
* **旋转**：垂直切换画布。
* **适应屏幕**：根据屏幕调整画布缩放级别。
* **缩小** / **放大**：缩小或显示在画布中。
* **显示地图**：打开显示您所在位置的画布快照。

### 规则属性窗格 {#rule-properties}

在右侧， **[!UICONTROL 规则属性]** 窗格提供有关查询的信息。 它允许您执行各种操作来检查查询并确保查询符合您的需求。 构建查询以创建受众时，显示此窗格。 [了解如何检查和验证您的查询](build-query.md#check-and-validate-your-query)
