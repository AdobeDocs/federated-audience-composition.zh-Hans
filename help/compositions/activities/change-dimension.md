---
audience: end-user
title: 使用更改维度活动
description: 了解如何使用更改维度活动
exl-id: e71017bd-6d2f-4ace-b2d9-cbfbb537d127
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 42%

---

# 更改维度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="更改维度活动"
>abstract="通过此活动，可在生成受众时更改架构，也称为定位维度。它根据数据模板和输入架构移动轴。例如，您可以从“合同”架构切换到“客户端”架构。"

**更改维度**&#x200B;活动允许您在构建受众时更改架构，也称为定向维度。 它根据数据模板和输入架构移动轴。

## 配置更改维度活动 {#configure}

按照以下步骤配置&#x200B;**更改维度**&#x200B;活动：

1. 将&#x200B;**更改维度**&#x200B;活动添加到合成。

   ![](../assets/change-dimension.png)

1. 定义&#x200B;**新架构**。 在模式更改期间，将保留所有记录。

1. 执行合成以查看结果。 比较&#x200B;**更改维度**&#x200B;活动之前和之后的表中的数据，并比较组合表的结构。

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->

