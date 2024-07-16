---
audience: end-user
title: 使用重复数据删除活动
description: 了解如何使用重复数据删除活动
source-git-commit: 56d9cc6489557c12761cd3fe8f3b7a61a71ece21
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 57%

---


# 删除重复项 {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="用于识别重复项的字段"
>abstract="在&#x200B;**用于识别重复项的字段**&#x200B;部分中，单击&#x200B;**添加属性**&#x200B;按钮以指定允许将相同值视为重复的字段，如电子邮件地址、名字、姓氏等。通过字段的顺序，可指定要先处理的字段。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="“内部重复数据删除”活动"
>abstract="通过&#x200B;**内部重复数据删除**&#x200B;活动，可删除集客活动结果中的重复项。主要在目标选择活动之后且允许使用目标数据的活动之前使用它。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="生成补集"
>abstract="可使用（已作为重复项被排除的）剩余群体生成额外的叫客过渡。为此，请打开&#x200B;**生成补集**&#x200B;选项"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="内部重复数据删除设置"
>abstract="要删除集客数据中的重复项，请在以下字段中定义内部重复数据删除方法。默认情况下，只保留一条记录。您还应该根据表达式或属性选择内部重复数据删除模式。默认情况下，随机选择要避免重复的记录。"

利用&#x200B;**重复数据删除**&#x200B;活动，可删除集客活动结果中的重复项，例如收件人列表中重复的用户档案。 **重复数据删除**&#x200B;活动通常用在定向活动之后，以及允许使用定向数据的活动之前。

## 配置重复数据删除活动{#deduplication-configuration}

按照以下步骤配置&#x200B;**重复数据删除**&#x200B;活动：

1. 将&#x200B;**重复数据删除**&#x200B;活动添加到合成。

1. 如果活动具有多个集客过渡，请从&#x200B;**[!UICONTROL 主集]**&#x200B;下拉列表中选择用于执行重复数据删除的过渡

1. 在&#x200B;**用于识别重复项的字段**&#x200B;部分中，单击&#x200B;**添加属性**&#x200B;按钮以指定允许将相同值视为重复的字段，如电子邮件地址、名字、姓氏等。通过字段的顺序，可指定要先处理的字段。

   ![](../assets/deduplication.png)

1. 在&#x200B;**重复数据删除设置**&#x200B;部分中，选择要保留的唯一&#x200B;**重复项数**。 此字段的默认值为 1。使用 0 值，可保留所有重复项。

   例如，如果记录 A 和 B 被视为记录 Y 的重复项，而记录 C 被视为记录 Z 的重复项：

   * 如果字段的值为 1：只保留 Y 和 Z 记录。
   * 如果字段的值为 0：保留所有记录。
   * 如果字段的值为 2：保留 C 和 Z 记录，并保留 A、B 和 Y 中的两个记录，具体情况取决于此后选择的重复数据删除方法。

1. 选择要使用的&#x200B;**重复数据删除方法**：

   * **随机选择**：随机选择要保留的重复项记录。
   * **使用表达式**：保留输入表达式的值最小或最大的记录。
   * **非空值**：保留表达式不为空的记录。
   * **遵循值列表**：为一个或多个字段定义值优先级。 若要定义值，请单击&#x200B;**属性**&#x200B;以选择一个字段或创建表达式，然后将值添加到相应的表中。 要定义新字段，请单击位于值列表上方的&#x200B;**添加按钮**。

1. 如果要利用剩余群体，请选中&#x200B;**生成补码**&#x200B;选项。 补充包含所有重复项。 然后，将向该活动添加其他过渡。

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
