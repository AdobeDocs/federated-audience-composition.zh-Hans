---
audience: end-user
title: 使用查询建模器
description: 了解如何使用查询建模器。
source-git-commit: f6730819712ffcbe815517a4406dac7e8fb9779c
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 11%

---

# 使用查询建模器 {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="查询建模器"
>abstract="为收件人或数据库中的任何其他定位维度定义过滤条件。"

查询建模器简化了根据各种条件筛选数据库的过程。 此外，查询建模器可以高效地管理非常复杂和长的查询，提供增强的灵活性和精确度。 此外，它支持条件中的预定义过滤器，使您能够轻松优化查询，同时利用高级表达式和运算符实现全面的受众定位和分段策略。

## 访问查询建模器

在每个需要定义规则以过滤数据的环境下都有查询建模器可用。

| 使用情况 | 示例 |
|  ---  |  ---  |
| **定义受众**：指定要在合成中定位的群体，并根据您的需求轻松创建新受众。 | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **自定义工作流活动**：在工作流活动中应用规则，例如 **Split** 和 **调解**，以符合您的特定要求。 [了解有关工作流活动的更多信息](../compositions/activities/about-activities.md) | ![](assets/access-workflow.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **预定义过滤器**：创建预定义过滤器，这些过滤器在各种过滤操作期间用作快捷键，无论您是使用数据列表还是构成投放的受众。 | ![](assets/access-predefined-filter.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **自定义列表**：创建自定义规则以过滤在列表（如收件人、投放列表等）中显示的数据。 | ![](assets/access-lists.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

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

在右侧， **[!UICONTROL 规则属性]** 窗格提供有关查询的信息。 它允许您执行各种操作来检查查询并确保查询符合您的需求。 [了解如何检查和验证您的查询](build-query.md#check-and-validate-your-query)
