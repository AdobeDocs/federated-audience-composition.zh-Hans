---
audience: end-user
title: 使用构建受众活动
description: 了解如何使用构建受众活动
badge: label="限量发布版" type="Informative"
exl-id: 6fad3e49-e654-4f68-a125-50056c4ae980
source-git-commit: 6aec8f5d9e8550ece2b50234d86ed59938f1b028
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 30%

---

# 构建受众 {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="“构建受众”活动"
>abstract="通过&#x200B;**构建受众**&#x200B;活动，可定义将进入构成的受众。"

**构建受众**&#x200B;活动允许您定义将进入构成的受众。 要定义受众群体，您可以：

* 选择现有Adobe Experience Platform受众。
* 通过定义和组合筛选条件使用查询建模器创建新受众。

## 配置“构建受众”活动 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="受众"
>abstract="选择受众。"

请按照以下步骤配置&#x200B;**生成受众**&#x200B;活动：

1. 添加一个&#x200B;**生成受众**&#x200B;活动。
1. 定义一个标签。
1. 指定是要创建受众还是选择现有受众。
1. 按照以下选项卡中详述的步骤配置受众。

>[!BEGINTABS]

>[!TAB 创建受众]

要创建您自己的受众，请执行以下步骤：

1. 选择&#x200B;**创建受众**。
1. 选择&#x200B;**架构**，也称为定向维度。 利用模式，您可以定义操作所针对的群体：收件人、合同受益人、操作员、订阅者等。 默认情况下，从收件人中选择架构。

   ![](../assets/build-audience-create.png)

1. 单击&#x200B;**继续**。
1. 使用查询建模器定义您的查询，然后进行确认。 [了解如何使用查询建模器](../../query/query-modeler-overview.md)

>[!TAB 读取受众]

要选择现有受众，请执行以下步骤：

1. 选择&#x200B;**读取受众**。
1. 单击&#x200B;**继续**。

   ![](../assets/build-audience-read.png)

1. 选择受众。

>[!ENDTABS]

>[!NOTE]
>
>通过&#x200B;**生成叫客过渡**&#x200B;选项，可添加将在活动执行结束时激活的叫客过渡（如果受众群体为空）。

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
