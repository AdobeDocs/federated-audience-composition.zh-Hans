---
audience: end-user
title: 使用构建受众活动
description: 了解如何使用构建受众活动
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 50%

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

此 **构建受众** 活动可以放置在合成的开头或任何其他活动之后。 任何活动都可以放在 **构建受众**.

## 配置“构建受众”活动 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="受众"
>abstract="选择受众。"

请按照以下步骤配置&#x200B;**生成受众**&#x200B;活动：

1. 添加一个&#x200B;**生成受众**&#x200B;活动。
1. 定义一个标签。
1. 定义受众类型：**创建您自己的**&#x200B;或&#x200B;**读取受众**。
1. 按照以下选项卡中详述的步骤配置受众。

>[!BEGINTABS]

>[!TAB 创建您自己的（查询）]

要创建自己的查询，请执行以下步骤：

1. 选择&#x200B;**创建您自己的（查询）**。
1. 选择&#x200B;**定位维度**。通过定位维度，可定义操作面向的群体：收件人、合同受益人、操作人员、订阅者等。默认情况下，将从收件人中选择目标。<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. 单击&#x200B;**继续**。
1. 使用查询建模器定义查询，与设计新电子邮件时创建受众的方式相同。 <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB 读取受众]

要选择现有受众，请执行以下步骤：

1. 选择&#x200B;**读取受众**。
1. 单击&#x200B;**继续**。
1. 选择受众，与设计新投放时使用受众的方式相同。 <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
