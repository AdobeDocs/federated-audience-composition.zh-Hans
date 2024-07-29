---
title: Experience Platform联合受众组合入门
description: 了解什么是 Adobe 联合受众构成以及如何在 Adobe Experience Platform 中使用它
badge: label="限量发布版" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 57%

---

# 开始使用联合受众构成 {#gs-fac}

联合受众组合是[Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/home){target="_blank"}和[Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home){target="_blank"}的附加功能，允许您从第三方数据仓库构建和扩充受众，并将受众导入Adobe Experience Platform。 联合受众构成提供了一种简单而强大的解决方案，可直接在 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer 内连接您的企业数据仓库，并对数据仓库的表格执行查询。

Adobe 联合受众构成可帮助 Adobe Experience Platform 应用程序用户访问存储在其数据仓库和云存储平台（例如 Amazon Redshift、Azure Synapse Analytics 等）中的客户数据。客户数据可存储在多个数据仓库中，并且现在可以立即访问，而无需复制。支持的平台列于[此页面](../connections/federated-db.md#supported-db)中。

## 功能 {#rn-capabilities}

联合受众构成通过全面的受众管理和激活方法扩展了Real-Time CDP和Journey Optimizer的价值：

* 扩展对关键基于仓库的数据集的访问，以创建高价值受众：利用现有数据仓库作为主要记录系统，同时利用同类最佳的应用程序来改善出色的客户体验。

* 全面支持强力参与用例：联合受众构成，与Real-Time CDP或Journey Optimizer配对，支持由品牌发起的具有联合受众的个性化体验，并提供由实时事件触发的即时体验以及人员属性，以满足跨团队的用例要求。

* 最大程度地减少数据移动和重复：从企业数据仓库中的数据集创建受众，而无需复制基础数据来管理可操作的营销用户档案和受众。

* 利用单个系统处理体验驱动型工作流：在Adobe Experience Platform中策划已摄取和联合的受众，并协调所有渠道的出站体验。

## 用例 {#rn-uc}

通过易于营销的 UI，创建细分规则，查询数据仓库以获取符合营销活动所需的特定区段的用户列表，访问仓库中的现有受众以进行激活，或使用仓库中存在的其他数据点扩充 Adobe Experience Platform 受众。

在此版本中，提供了两个用例：

1. 受众创建：从企业数据集构建新受众，而无需复制基础数据，并使用预建目标激活这些受众&#x200B;。

1. 受众扩充：通过利用从企业数据仓库联合的组合受众数据，扩充Adobe Experience Platform中的现有受众。 此数据将不会保留在Adobe Experience Platform客户配置文件中。

![图表](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## 关键步骤 {#gs-steps}

使用 Adobe 联合受众构成可以直接从数据库创建和更新 Adobe Experience Platform 受众，而无需任何引入过程。

![图表](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}

关键步骤：

1. **数据集成**：汇集来自不同来源的数据，并将其合并为统一的数据集。若要了解如何连接 Adobe Experience Platform 应用程序以及您的企业数据仓库、所支持的数据库以及如何配置它们，请参阅[本节](../connections/federated-db.md)中的详细说明。

2. **数据建模**：设计和创建定义数据结构、关系和约束的数据模型和模式。要了解有关架构的更多信息，请参阅[本页](../customer/schemas.md)。在[此页面](../data-management/gs-models.md)中了解如何为您的数据模型创建链接。

3. **数据转换**：应用数据操作技术来修改数据元素的格式、结构或值，使其兼容或适合特定的分析或应用程序。

4. **数据使用**：创建、组织和建立受众。在[此页面](../compositions/gs-compositions.md)中了解如何组合观众。您还可以通过 Adobe Experience Platform 受众门户和目标更新或重复使用现有受众。在[此页面](../connections/destinations.md)中了解详情

>[!NOTE]
>
>执行组合后，生成的受众将作为外部受众保存在Adobe Experience Platform中，并可用于Adobe实时客户数据平台和/或Adobe Journey Optimizer中。 它可在&#x200B;**受众**&#x200B;菜单中访问。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## 了解详情 {#learn}

<!-- Workflow + Workflow activities-->


在[此页面](access-prerequisites.md)中了解如何访问联合受众合成、护栏和限制。

另请参阅[此页面](faq.md)中的常见问题解答。


>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="执行设置"
>abstract="在此部分中，您可以配置与工作流执行相关的设置，例如构成历史记录的保留天数。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="无法编辑活动"
>abstract="在控制台中为某个&#x200B;**查询**&#x200B;或&#x200B;**扩充**&#x200B;活动配置了其他数据后，扩充数据被考虑并传递到出站转换，但无法编辑该活动。"

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="创建链接"
>abstract="定义链接设置"
