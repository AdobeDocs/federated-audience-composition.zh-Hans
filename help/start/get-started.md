---
title: 联合受众组合入门
description: 了解什么是Adobe联合受众组合以及如何在Adobe Experience Platform中使用它
badge: label="限量发布版" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 9397bac0fda54761b2ac3c29140d32a433cb514b
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 11%

---

# 联合受众组合入门 {#gs-fac}

联合受众构成是Adobe Real-time Customer Data Platform和Adobe Journey Optimizer的一个附加组件，允许您从第三方数据仓库构建和扩充受众，并将受众导入Adobe Experience Platform。 联合受众组合提供了一个简单而强大的解决方案，用于直接在Adobe Real-time Customer Data Platform和/或Adobe Journey Optimizer中连接企业数据仓库，并对数据仓库的表执行查询。

Adobe联合受众构成可帮助Adobe Experience Platform应用程序用户访问其客户数据，这些数据会存储到其数据仓库和云存储平台(如Amazon Redshift、Azure synapseAnalytics等)中。 客户数据可以存放在多个数据仓库中，现在无需复制即可即时访问。 [此页面](../connections/federated-db.md#supported-db)中列出了支持的平台。

## 用例 {#rn-uc}

通过营销友好UI，创建区段规则，这些规则可在数据仓库中查询符合营销活动所需特定区段资格的用户列表，访问仓库中的现有受众以供激活，或使用仓库中存在的附加数据点扩充Adobe Experience Platform受众。

在此版本中，提供了两个用例：受众分段和受众扩充。 用户档案扩充功能将在未来版本中提供。

![关系图](assets/fac-use-cases.png){zoomable="yes"}

## 关键步骤 {#gs-steps}

通过Adobe联合受众合成，可直接从数据库创建和更新Adobe Experience Platform受众，而无需任何摄取过程。

![关系图](assets/steps-diagram.png){zoomable="yes"}

关键步骤：

1. **数据集成**：将来自各种源的数据合并到一个统一的数据集中。 [本节](../connections/federated-db.md)详细介绍了如何连接Adobe Experience Platform应用和您的企业数据仓库、支持的数据库以及如何配置它们。

2. **数据建模**：设计和创建定义数据结构、关系和约束的数据模型和架构。 在[此页面](../customer/schemas.md)中了解有关架构的更多信息。 在[此页面](../data-management/gs-models.md)中了解如何为数据模型创建链接。

3. **数据转换**：应用数据操作技术来修改数据元素的格式、结构或值，使其兼容或适用于特定的分析或应用程序。

4. **数据使用情况**：创建、编排和构建受众。 了解如何在[此页面](../compositions/gs-compositions.md)中组合受众。 您还可以通过Adobe Experience Platform受众门户和目标更新或重用现有受众。 在[此页面](../connections/destinations.md)中了解详情


>[!NOTE]
>
>执行组合后，生成的受众将作为外部受众保存在Adobe Experience Platform中，并可用于Adobe实时客户数据平台和/或Adobe Journey Optimizer中。 它可在&#x200B;**受众**&#x200B;菜单中访问。 [了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}
>



## 了解详情 {#learn}

<!-- Workflow + Workflow activities-->

请参阅[此页面](faq.md)中的常见问题解答。

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="执行设置"
>abstract="在此部分中，您可以配置与工作流执行相关的设置，如构成历史记录的保留天数。"




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="无法编辑活动"
>abstract="在控制台中为某个&#x200B;**查询**&#x200B;或&#x200B;**扩充**&#x200B;活动配置了其他数据后，扩充数据被考虑并传递到出站转换，但无法编辑该活动。"

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="创建链接"
>abstract="定义链接设置"
