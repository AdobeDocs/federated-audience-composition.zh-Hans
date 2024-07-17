---
audience: end-user
title: 使用构建受众活动
description: 了解如何使用构建受众活动
badge: label="限量发布版" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 40%

---


# 构建受众 {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="“构建受众”活动"
>abstract="通过&#x200B;**构建受众**&#x200B;活动，可定义将进入构成的受众。"

通过&#x200B;**构建受众**&#x200B;活动，可定义将进入构成的受众。

要定义受众群体，您可以：

<!--* Select an existing audience, created as a list in the client console.-->
* 选择 Adobe Experience Platform 受众。
* 通过定义和组合筛选条件，使用查询建模器生成器构建新受众。

**生成受众**&#x200B;活动可以放置在合成的开头或任何其他活动之后。 任何活动都可以放在&#x200B;**生成受众**&#x200B;之后。

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
1. 单击&#x200B;**继续**。
1. 使用查询建模器定义您的查询。 [了解如何使用查询建模器](../../query/query-modeler-overview.md)

>[!TAB 读取受众]

要选择现有受众，请执行以下步骤：

1. 选择&#x200B;**读取受众**。
1. 单击&#x200B;**继续**。
1. 选择受众。

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
