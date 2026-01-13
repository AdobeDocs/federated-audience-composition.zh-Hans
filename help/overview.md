---
title: 联合受众构成概述
description: 了解Adobe Federated Audience Composition以及如何将其用于下游服务，如Adobe Experience Platform和Adobe Journey Optimizer
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 51%

---

# 联合受众构成概述

联合受众构成允许您从第三方数据仓库构建和丰富受众，并将受众导入Adobe Experience Platform。 这带来了一个简单而强大的解决方案，用于直接在Adobe Real-Time Customer Data Platform或Adobe Journey Optimizer等下游服务中连接企业数据仓库，并对数据仓库的表执行查询。 因此，您可以访问存储在数据仓库和云存储平台(如Amazon Redshift和Azure Synapse Analytics)中的客户数据。

## 功能 {#rn-capabilities}

联合受众构成通过全面的受众管理和激活方法扩展了 Real-Time CDP 和 Journey Optimizer 的价值：

* **扩展对基于仓库的关键数据集的访问权限以创建高价值受众**：您可以使用现有数据仓库作为主要记录系统，同时利用同类最佳应用程序来改善优秀的客户体验。

* **全面支持高级参与用例**：联合受众合成，与Real-Time CDP或Journey Optimizer配对，支持由品牌发起的具有联合受众的个性化体验，并提供由实时事件触发的即刻体验，以及人员属性，以满足跨团队的用例要求。

* **最大程度地减少数据移动和重复**：您可以从企业数据仓库中的数据集创建受众，而无需复制基础数据来管理可操作的营销用户档案和受众。

* **为体验驱动的工作流利用单个系统**：您可以在Adobe Experience Platform中策划已摄取和联合的受众，并协调所有渠道的出站体验。

* **多版本支持**： B2C和B2B CDP客户可以通过集成来自受支持的企业数据仓库的数据，利用联合受众组合构建基于人员的受众。 此外，他们可以通过整合企业数据仓库中提供的相关属性来丰富现有的Experience Platform基于人员的受众，提升其受众配置文件以实现更加个性化和有针对性的参与。

## 用例 {#use-cases}

联合受众构成支持&#x200B;**三类**&#x200B;使用场景：受众创建、受众扩充和客户轮廓扩充。

* **受众创建**：您可以通过营销人员友好的拖放用户界面，从数据仓库创建受众并将这些受众联合到Experience Platform中，以便在Real-Time CDP或Journey Optimizer中使用。 因此，您无需复制敏感的底层数据或重复现有数据，即可查询数据仓库。
   * **示例：**&#x200B;利用数据仓库中的历史交易数据创建高价值历史购买者受众，而无需将这些交易数据复制到 Experience Platform 中。

* **受众扩充**：通过使用数据仓库中的其他数据集并使用此信息叠加受众，您可以向Experience Platform中的现有受众添加更多详细信息 — 所有这些操作都不需要将基础数据复制到Experience Platform中。 通过受众扩展，您可以借助扩充后的受众实现更出色的个性化体验。
   * **示例：**&#x200B;将 Experience Platform 中的购物车放弃者受众与联合受众构成中的高价值历史购买者受众进行整合，以实现精准的产品建议投放。

* **配置文件扩充**：您可以从数据仓库中选择单个客户属性以增强Experience Platform配置文件。 通过将联合数据添加到这些轮廓中，您可以更有效地响应客户的实时信号，从而驱动即时体验。
   * **示例：**&#x200B;使用联合受众中的信息丰富 Experience Platform 中的轮廓。现在，您可以根据站点访客的在站行为，向其投放定向产品优惠——前提是该访客属于高价值历史购买者联合受众。

![图表](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

如需了解更多联合受众构成的使用案例，请参阅[《联合受众构成白皮书》](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html)。

## 关键步骤 {#gs-steps}

使用 Adobe 联合受众构成可以直接从数据库创建和更新 Adobe Experience Platform 受众，而无需任何引入过程。

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **创建连接**：将来自各种源的数据合并到一个统一的数据集中。 有关将Adobe Experience Platform应用连接到您的企业数据仓库、支持的数据库，以及配置连接的详细信息，请阅读[连接概述](./connections/home.md)。

2. **为您的数据建模**：设计和创建定义数据的结构、关系和约束的架构和数据模型。 有关架构的详细信息，请阅读[架构概述](./data-modelling/schemas.md)。 有关数据模型的详细信息，请阅读[数据模型概述](./data-modelling/models.md)。

3. **转换数据**：应用数据操作技术来修改数据元素的格式、结构或值，使其兼容或适用于特定的分析或应用程序。

4. **撰写受众**：创建、编排和构建受众。 有关合成受众的详细信息，请阅读[合成概述](./compositions/home.md)。 您还可以通过 Adobe Experience Platform 受众门户和目标更新或重复使用现有受众。请参阅[此页面](./connections/destinations.md)了解详情。

>[!NOTE]
>
>执行构成后，生成的受众将会作为外部受众保存在 Adobe Experience Platform 中，并可进入 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer。它可在&#x200B;**受众**&#x200B;菜单中访问。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## 管理、隐私和安全 {#governance-privacy-security}

### 隐私请求 {#gov-privacy-requests}

您创建一个构成后，生成的受众就会保存在 Adobe Experience Platform 中。

然后，您可以通过 Adobe Experience Platform **Privacy Service** 提出隐私请求，以访问和/或删除与这些受众相对应的轮廓数据，该服务提供[用户界面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans){target="_blank"}和 [RESTful API](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/api/overview){target="_blank"} 来帮助您管理客户数据请求。

>[!NOTE]
>
>关于 Privacy Service 的更多信息，请参阅 [Adobe Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans){target="_blank"}。

您可以创建和管理单独的请求以访问和删除 Adobe 联合受众构成中的客户数据。[实时客户轮廓文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/privacy){target="_blank"}中详细说明了提交&#x200B;**访问请求**&#x200B;和&#x200B;**删除请求**&#x200B;的步骤。

### 审核记录 {#gov-audit-trail}

审核记录功能会按时间顺序详细记录对环境实时执行的所有操作和事件。 若要了解有关审核记录的详细信息，请阅读[审核记录概述](./admin/audit-trail.md)。

## 了解详情 {#learn}

<!-- Workflow + Workflow activities-->

在[此页面](./start/access-prerequisites.md)中了解如何访问联合受众构成、护栏和限制。

有关常见问题的解答，请阅读[联合受众组合常见问题解答](./faq.md)。

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="执行设置"
>abstract="在此部分中，您可以配置与工作流执行相关的设置，如合成历史记录的保留天数。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="无法编辑活动"
>abstract="在控制台中为某个&#x200B;**查询**&#x200B;或&#x200B;**扩充**&#x200B;活动配置了其他数据后，扩充数据被考虑并传递到出站转换，但无法编辑该活动。"

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="创建链接"
>abstract="定义链接设置"


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="增量查询"
>abstract="**增量查询** 活动允许您使用查询建模器查询数据库。每次执行此活动时，都会排除先前执行得出的结果。这样可让您仅定向新元素。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="增量查询历史记录"
>abstract="增量查询历史记录"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="增量查询处理后的数据"
>abstract="增量查询处理后的数据"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="增量查询模式"
>abstract="增量查询允许您通过每次新执行排除以前执行的结果来多次执行相同的查询。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="增量查询模式"
>abstract="增量查询允许您仅考虑日期字段晚于或等于增量查询活动的上次执行日期的结果，从而多次执行相同的查询。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="选择定位维度"
>abstract="通过定位维度，可定义操作面向的群体：收件人、合同受益人、操作人员、订阅者等。默认情况下，对于电子邮件和 SMS，目标是在收件人内置表中进行选择的。对于推送通知，默认目标维度是订阅者应用程序。"

