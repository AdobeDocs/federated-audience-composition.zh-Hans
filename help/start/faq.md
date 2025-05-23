---
title: 常见问题解答
description: 有关 Adobe Experience Platform 联合受众构成的常见问题解答
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: ht
source-wordcount: '897'
ht-degree: 100%

---

# 常见问题解答 {#faq}

以下是有关 Adobe Experience Platform 联合受众构成的常见问题列表。[此页面](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/faq){target="_blank"}中还提供了有关 Adobe Experience Platform 细分服务的一般常见问题解答。


+++访问联合受众构成需要哪些权限？

联合受众构成需要 Adobe Real-Time Customer Data Platform 和 Adobe Journey Optimizer Prime 或 Ultimate 包。您还需要购买联合受众构成。

为了使用联合受众构成，必须将每个用户添加到为每个沙盒创建的特定轮廓中。若要了解更多信息，请参阅[访问联合受众构成](access-prerequisites.md)页面。

+++

+++支持哪些云仓库？

[此页面](../start/access-prerequisites.md#supported-systems)提供了联合受众构成支持的系统列表。

+++


+++在同一构成中可以查询多个数据仓库吗？

是的，同一构成中可以查询多个仓库，并且可以组合多个来源的数据。通常，每个[构成活动](../compositions/orchestrate-activities.md)（查询、扩充、拆分等）根据活动配置、目标数据库（可以有多种联合数据访问的情况）以及执行结果的一个或多个工作表的输出执行一条或多条 SQL 语句。这些工作表用作连续活动的输入。

+++

+++ 我可以使用联合受众构成访问我的整个数据库吗？

不可以，您需要配置对特定或共享数据库/架构的访问。我们建议您为联合受众构成创建一个专用架构，并仅复制/共享业务案例数据集。
+++

+++我可以访问专用架构中的所有表格吗？

是的，连接后，联合受众构成可用于根据定义的初始权限发现所有表，然后您可以使用可视化架构编辑器来：

* 从表中发现列和主键
* 为这些表创建易用的标签
* 为每列创建易用的标签
* 隐藏不必要的列
* 保存对那些表的描述
+++

+++联合受众构成中是否有任何临时存储？

没有，联合受众构成仅会存储元数据（架构描述）。没有客户数据在传输。<!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++联合受众构成是否存储了该人员名单的物理副本，以发送给下游系统？

联合受众构成不会维护数据的物理副本。频率在构成中进行配置，以定义数据刷新的频率。Adobe Experience Platform 存储所得受众数据的时间不会超过客户用例或操作所需的时间。

例如：

* 对于受众创建，受众是在您的仓库中创建的，您可以使用联合受众构成执行其他构成任务和数据操作，然后通过 Adobe Experience Platform 众门户中发布生成的受众和相关属性。受众定义和相关属性都转移到了 Adobe Experience Platform。
请注意，外部生成的受众的当前数据有效期限为 30 天。数据过期会减少组织内存储的多余数据量。数据过期期限过后，关联的数据集仍然在数据集库存中可见，但您无法激活受众，并且轮廓计数将显示为零。在 [Adobe Experience Platform 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}中了解详情。

* 对于受众扩充而言，起点是现有的 Adobe Experience Platform 受众。这里可以看到两种情况：
   1. 从联合数据仓库中获取额外的受众负载属性：在这种情况下，所添加的额外属性将会作为此受众定义的一部分出现。外部生成的受众的数据有效期限与上面描述的相同，为 30 天。
   1. 根据数据仓库中存在的其他属性来优化现有的 Adobe Experience Platform 受众。<!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++如果受众创建和受众扩充用例模式的数据没有经过持久化，那么如何临时存储这些数据？

生成的受众数据不会无限期地保留在 Adobe Experience Platform 或联合受众构成中。它的保留时间不会超过您的用例所需的时间。作为受众负载的一部分所带来的受众属性将仅作为受众定义的一部分而存在。持久性的持续时间是由任何受众的 TTL 而定的，默认为 30 天。

+++

+++ 我可以删除受众吗？

不可以，在当前版本中您无法删除联合受众构成的受众。

+++

+++如果我合并来自多个来源的数据，我们会如何合并数据？我们使用身份标识服务吗？

不，构成过程中不会利用身份标识服务。构成中使用的各种来源之间的数据通过用户定义的逻辑（如底层模型中所表达的）进行连接，例如 CRM ID、用户帐号等。您必须选择用作受众身份标识符的身份标识，以便在数据仓库中进行选择。在联合受众构成产生的受众中，您需要在生成的数据集中身份标识该身份标识的身份标识命名空间。

+++

+++ 如何使用联合受众构成创建和管理隐私请求？

您可以通过两种方法提交单独的请求以访问和删除 Adobe 联合受众构成中的客户数据：

* 通过 Adobe Experience Platform **Privacy Service UI**。[了解详情](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans){target="_blank"}
* 通过 Adobe Experience Platform **Privacy Service API**。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/api/overview){target="_blank"}

[实时客户轮廓文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/privacy){target="_blank"}中详细说明了创建和管理&#x200B;**访问请求**&#x200B;和&#x200B;**删除请求**&#x200B;的所有步骤。

+++

<!--
+++How are customer consent preferences honored for externally generated audiences that are imported into Federated Audience Composition?

As customer data is captured from multiple channels, identity stitching and merge policies allow this data to be consolidated in a single Real-Time Customer Profile. Information on the customers' consent preferences are stored and evaluated at the profile level.

Downstream Real-Time CDP and Journey Optimizer destinations check each profile for consent preferences prior to activation. Each profile's consent information is compared against consent requirements for a particular destination. If the profile does not satisfy the requirements, that profile is not sent to a destination.

When an external audience is ingested into Federated Audience Composition, it is reconciliated with existing profiles using a primary ID such as email or ECID. As a result, the existing consent policies will remain in force throughout activation.

>[!NOTE]
>
>Since the payload variables are not stored in the profile but in the data lake, you should not include consent information in externally generated audiences. Instead, use other Adobe Experience Platform ingestion channels where profile data is imported.

+++
-->
