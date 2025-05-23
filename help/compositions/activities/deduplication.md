---
audience: end-user
title: 使用重复数据删除活动
description: 了解如何使用重复数据删除活动
exl-id: 55db2461-fcfb-4284-9ab7-7cb01071ed1c
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 42%

---

# 重复数据删除 {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="用于识别重复项的字段"
>abstract="在&#x200B;**[!UICONTROL 用于识别重复项的字段]**&#x200B;部分中，单击&#x200B;**[!UICONTROL &#x200B;添加属性&#x200B;]**&#x200B;按钮以指定允许将相同值视为重复的字段，如电子邮件地址、名字、姓氏等。栏位的顺序可让您指定首要处理的条件。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="删除重复项活动"
>abstract="删除&#x200B;**重复项活动可让您删除**&#x200B;入站活动结果中的重复项。主要在定位活动之后且在允许使用目标数据的活动之前使用。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="删除重复项设置"
>abstract="要删除传入数据中的重复项，请在以下字段中定义删除重复项方法。默认情况下，只会保留一条记录。您还应该根据表达式或属性选择删除重复项模式。默认情况下，要避免重复的记录是随机选择的。"

利用&#x200B;**重复数据删除**&#x200B;活动，可删除集客活动结果中的重复项，例如收件人列表中重复的用户档案。 **重复数据删除**&#x200B;活动通常用在定向活动之后，以及允许使用定向数据的活动之前。

## 配置重复数据删除活动{#deduplication-configuration}

按照以下步骤配置&#x200B;**重复数据删除**&#x200B;活动：

1. 将&#x200B;**重复数据删除**&#x200B;活动添加到合成。

1. 如果活动具有多个集客过渡，请从&#x200B;**[!UICONTROL 主集]**&#x200B;下拉列表中选择用于执行重复数据删除的过渡

1. 在&#x200B;**[!UICONTROL 用于识别重复项的字段]**&#x200B;部分中，单击&#x200B;**[!UICONTROL &#x200B;添加属性&#x200B;]**&#x200B;按钮以指定允许将相同值视为重复的字段，如电子邮件地址、名字、姓氏等。栏位的顺序可让您指定首要处理的条件。

   ![](../assets/deduplication.png)

1. 在&#x200B;**[!UICONTROL 重复数据删除设置]**&#x200B;部分中，选择要保留的唯一&#x200B;**[!UICONTROL 重复项数]**。 此字段的默认值为&#x200B;**1**。 值&#x200B;**0**&#x200B;允许您保留所有重复项。

   例如，如果记录 A 和 B 被视为记录 Y 的重复项，而记录 C 被视为记录 Z 的重复项：

   * 如果该字段的值为&#x200B;**1**：只保留Y和Z记录。
   * 如果该字段的值为&#x200B;**0**：保留所有记录。
   * 如果该字段的值为&#x200B;**2**：保留C和Z记录，并保留A、B和Y中的两个记录，具体情况取决于此后选择的重复数据删除方法。

1. 选择要使用的&#x200B;**[!UICONTROL 重复数据删除方法]**：

   * **[!UICONTROL 随机选择]**：随机选择要保留的重复项记录。
   * **[!UICONTROL 使用表达式]**：保留输入表达式的值最小或最大的记录。
   * **[!UICONTROL 非空值]**：保留表达式不为空的记录。
   * **[!UICONTROL 遵循值列表]**：为一个或多个字段定义值优先级。 若要定义值，请单击&#x200B;**[!UICONTROL 属性]**&#x200B;以选择一个字段或创建表达式，然后将值添加到相应的表中。 要定义新字段，请单击位于值列表上方的&#x200B;**[!UICONTROL 添加按钮]**。

1. 如果要利用剩余群体，请选中&#x200B;**[!UICONTROL 生成补码]**&#x200B;选项。 补充包含所有重复项。 然后，将向该活动添加其他过渡。

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
