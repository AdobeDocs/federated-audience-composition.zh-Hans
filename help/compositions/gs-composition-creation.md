---
audience: end-user
title: 创建合成
description: 了解如何创建合成
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: b73eba776e3e75f3ff7107bcf48f7b2f60048d08
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 58%

---

# 创建构成的主要原则 {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="构成属性"
>abstract="在此屏幕中，选择要用于创建构成的模板并指定标签。展开“其他选项”部分以配置更多设置，例如构成的内部名称、其文件夹、时区和主管组等。强烈建议选择一个主管组，以便如果出错，可提醒操作员。"

## 构成中的内容 {#gs-composition-inside}

Experience Platform联合受众构成提供了一个可视画布，允许您利用各种活动（拆分、扩充等）来创建受众。

组合图是应发生情况的表示形式。 它描述要执行的各种任务及其如何链接在一起。

![](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

每个构成都包含：

* **[!UICONTROL 活动]**：活动是要执行的任务。在图上用图标表示各种活动。每个活动都有特定属性和所有活动共有的其他属性。
* **[!UICONTROL 过渡]**：过渡将源活动链接到目标活动并定义它们的顺序。
* **[!UICONTROL 工作表]**：工作表包含了过渡所携带的所有信息。每个构成都使用多个工作台。 这些表中传送的数据可在整个合成生命周期中使用。

## 创建合成的关键步骤 {#gs-composition-steps}

创建合成的主要步骤如下：

1. [创建和配置合成](../compositions/create-composition.md)
1. [策划活动](../compositions/orchestrate-activities.md)
1. [执行构成并监视其执行](../compositions/start-monitor-composition.md)
