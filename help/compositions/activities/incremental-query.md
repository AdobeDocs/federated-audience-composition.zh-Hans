---
audience: end-user
title: 使用增量查询活动
description: 了解如何使用增量查询活动
hide: true
hidefromtoc: true
source-git-commit: 34d6fc8f97c491fcb91eebf8e1377018e5020a4a
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 13%

---

# 增量查询 {#incremental-query}

<!-- Warning : contextual help IDs are declared in /start/get-started.md-->

**增量查询**&#x200B;活动允许您按计划查询数据库。 每次执行此活动时，都会排除先前执行得出的结果。这样可让您仅定向新元素。

**[!UICONTROL 增量查询]**&#x200B;活动可用于各种类型的使用：

* 对个体进行分段以定义消息的目标、受众等。
* 导出数据。 例如，您可以使用活动以文件格式定期导出新日志。 如果要在外部报表或BI工具中使用日志数据，则此功能非常有用。

之前执行已定向的群体将存储在构成中。 这意味着从同一模板启动的两个合成不共享同一日志。 但是，两个基于相同增量查询的任务在同一组合中使用相同的日志。

如果增量查询在其执行之一期间的结果等于0，则合成将暂停，直到查询下一次程序化执行。 因此，在后续执行之前，不会处理增量查询之后的过渡和活动。

## 配置增量查询活动 {#incremental-query-configuration}

按照以下步骤配置&#x200B;**增量查询**&#x200B;活动：

1. 将&#x200B;**增量查询**&#x200B;活动添加到合成中。

1. 在&#x200B;**[!UICONTROL 受众]**&#x200B;部分中，选择&#x200B;**定向维度**，然后单击&#x200B;**[!UICONTROL 继续]**。

   通过目标选择维度，可定义操作面向的群体：收件人、合同受益人、操作人员、订阅者等。默认情况下，将从收件人中选择目标。<!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. 使用查询建模器定义查询，与设计新电子邮件时创建受众的方式相同。 [了解如何使用查询建模器](../../query/query-modeler-overview.md)

1. 在&#x200B;**[!UICONTROL 已处理数据]**&#x200B;部分中，选择要使用的增量模式：

   * **[!UICONTROL 排除先前执行的结果]**：每次执行活动时，都会排除先前执行的结果。

     以前执行中已定向的记录最多可记录从被定向之日起的天数。 为此，请使用&#x200B;**[!UICONTROL History in days]**&#x200B;字段。 如果此值为零，则不会从日志中清除收件人。

   * **[!UICONTROL 使用日期字段]**：此选项允许您根据特定日期字段从先前执行中排除结果。 要实现此目的，请从可用于所选定向维度的属性列表中选择所需的日期字段。 在下次执行合成时，将仅检索在上次执行日期之后修改或创建的数据。

     在第一次执行合成后，**[!UICONTROL 上次执行日期]**&#x200B;字段变为可用。 它指定将用于下一次执行的日期，并在每次执行合成时自动更新。 您仍然可以手动输入新值来覆盖此值，以使其符合您的需求。

   >[!NOTE]
   >
   >根据所选的日期字段，**[!UICONTROL 使用日期字段]**&#x200B;模式允许更大的灵活性。 例如，如果指定字段对应于修改日期，则可利用日期字段模式，检索最近更新的数据，而其他模式将仅排除在先前执行中已定向的记录，即使上次执行合成后已修改这些记录也是如此。

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
