---
title: 常见问题
description: 有关Adobe Experience Platform联合受众组合的常见问题解答
badge: label="限量发布版" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 75f997e4b1c0338a635dff43e2254757fbc5ec69
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 2%

---

# 常见问题解答 {#faq}

以下是有关Adobe Experience Platform联合受众组合的常见问题解答列表。 在[此页面](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}中，Adobe Experience Platform分段服务也提供了全局常见问题解答。


+++访问联合受众组合所需的权限是什么？

联合受众构成需要Adobe Real-time Customer Data Platform和Adobe Journey Optimizer Prime或Ultimate包。 联合受众组合没有特定权限。 访问此功能的唯一先决条件就是已购买联合受众构成加载项。

+++

+++支持哪些云仓库？

对于此版本，联合受众组合与以下兼容：

* Amazon Redshift
* azure synapse
* Google Big Query
* Snowflake
* Vertica Analytics

+++


+++能否在同一构成中查询多个数据仓库？

可以，可以在同一组合中查询多个仓库，并且可以组合来自多个来源的数据。  通常，每个[组合活动](../compositions/orchestrate-activities.md)（查询、扩充、拆分等） 根据活动配置、目标数据库（可能存在多个联合数据访问情况）以及一个或多个工作表输出和执行结果执行一个或多个SQL语句。 这些工作表用作连续活动的输入。

+++

+++ 我是否可以使用联合受众组合访问整个数据库？

否，您可以配置对专用或共享数据库/模式的访问。 我们建议您为联合受众组合创建专用架构，并仅复制/共享业务案例数据集。
+++



+++我是否可以访问专用模式中的所有表？

是，连接后，可使用联合受众组合根据定义的初始权限发现所有表，然后可以使用可视模式编辑器执行以下操作：

* 从表中发现列和主键
* 为这些表创建友好标签
* 为每列创建易记标签
* 隐藏不必要的列
* 保存这些表说明
+++


+++联合受众构成中是否存在临时存储？

否，联合受众组合仅存储元数据（架构描述）。 没有客户数据正在中转。<!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++联合受众构成是否存储要发送到下游系统的人员列表的物理副本？

联合受众构成不维护数据的物理副本。 在构成中配置频率，以定义此数据的刷新频率。 生成的受众数据不会由Adobe Experience Platform存储，客户用例或操作所要求的存储时间不会超过此存储时间。

例如：

* 在创建受众时，会在您的仓库中创建受众，在通过Adobe Experience Platform受众门户发布生成的受众和相关属性之前，您可以使用联合受众构成执行其他合成任务和数据操作。 受众定义和相关属性转到Adobe Experience Platform。
请注意，外部生成的受众的当前数据到期时间为30天。 此数据到期可减少组织中存储的多余数据量。 在数据过期后，关联的数据集仍会在数据集清单中可见，但您无法激活受众，并且配置文件计数将显示为零。 请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}以了解详情。

* 对于受众扩充，起始点是现有的Adobe Experience Platform受众。 我们可以在这里看到两种情况：
   1. 从联合数据仓库引入其他受众有效负载属性：在这种情况下，添加的其他属性将作为此受众定义的一部分提供。 外部生成的受众的数据过期时间与上述相同，即30天。
   1. 根据数据仓库中存在的其他属性优化现有Adobe Experience Platform受众。<!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++如果用于受众创建和受众扩充用例模式的数据未保留，那么它是如何临时存储的？

生成的受众数据不会在Adobe Experience Platform或联合受众构成中无限期保留。 它不会保留超过用例所需的时间。 作为受众有效负载的一部分引入的受众属性将仅作为受众定义的一部分保留。 持久性的持续时间基于任何受众的TTL，默认为30天。

+++

+++可以删除自定义上传的受众吗？

只需从操作菜单中选择删除，即可直接在Audience Portal中删除未在下游激活中使用的受众。 请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}以了解详情。

+++

+++如果合并来自多个源的数据，我们如何连接这些数据？ 我们是否使用Identity服务？

否，在组合期间未利用Identity Service。 组合中使用的各种源之间的数据通过用户定义的逻辑（如底层模型中表示的）进行连接，例如CRM ID、用户帐户号等。 您必须选择用作受众中标识符的标识，以供在数据仓库中选择。 对于联合受众组合产生的受众，您需要在产生的数据集中标识身份的身份命名空间。

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
