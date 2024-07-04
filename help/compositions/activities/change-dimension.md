---
audience: end-user
title: 使用更改维度活动
description: 了解如何使用更改维度活动
source-git-commit: 44be467650e2329a1fce6c5adb6d266d94efd1e2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 32%

---


# 更改维度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="生成补集"
>abstract="可使用（已作为重复项被排除的）剩余群体生成额外的叫客过渡。为此，请打开&#x200B;**生成补集**&#x200B;选项"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="“更改维度”活动"
>abstract="利用此活动，可在构建受众时更改定向维度，即架构。 它根据数据模板和输入维度移动轴。例如，您可以从“合同”维度切换到“客户”维度。"

此 **更改维度** 活动允许您在构建受众时更改定向维度，即架构。 它根据数据模板和输入维度移动轴。 <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

## 配置更改维度活动 {#configure}

按照以下步骤配置 **更改维度** 活动：

1. 添加 **更改维度** 活动添加到合成。

   ![](../assets/change-dimension.png)

1. 定义 **新架构**. 在模式更改期间，将保留所有记录。

1. 执行合成以查看结果。 比较变更维活动之前和之后的表中的数据，并比较构成表的结构。

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->