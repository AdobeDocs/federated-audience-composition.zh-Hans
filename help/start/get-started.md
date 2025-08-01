---
title: 开始使用 Experience Platform 联合受众构成
description: 了解什么是 Adobe 联合受众构成以及如何在 Adobe Experience Platform 中使用它
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 16d307172ec6ad2d64f50b686d2d251267ce29ae
workflow-type: ht
source-wordcount: '1236'
ht-degree: 100%

---

# 开始使用联合受众构成 {#gs-fac}

联合受众构成适用于 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/home){target="_blank"} 和 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home){target="_blank"} 环境。它允许您从第三方数据仓库构建和扩充受众，并将受众导入到 Adobe Experience Platform 中。联合受众构成提供了一种简单而强大的解决方案，可直接在 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer 内连接您的企业数据仓库，并对数据仓库的表格执行查询。

Adobe 联合受众构成可帮助 Adobe Experience Platform 应用程序用户访问存储在其数据仓库和云存储平台（例如 Amazon Redshift、Azure Synapse Analytics 等）中的客户数据。客户数据可存储在多个数据仓库中，并且现在可以立即访问，而无需复制。支持的平台列于[此页面](../connections/home.md#supported-db)中。

>[!INFO]
>
>按照此[分步指南](https://experienceleague.adobe.com/zh-hans/docs/platform-learn/tutorial-comprehensive-technical/datacollection/module13/fac)了解如何使用联合受众构成创建受众。

## 功能 {#rn-capabilities}

联合受众构成通过全面的受众管理和激活方法扩展了 Real-Time CDP 和 Journey Optimizer 的价值：

* 通过扩大对关键仓库数据集的访问权限来创建高价值受众：利用现有数据仓库作为主要的记录系统，同时利用一流的应用程序来提供出色的客户体验。

* 全面支持参与用例：联合受众构成与 Real-Time CDP 或 Journey Optimizer 相结合，支持由品牌发起的联合受众个性化体验，并提供由实时事件触发的即时体验，同时结合人员属性来满足跨团队的用例要求。

* 最小化数据移动和重复：从企业数据仓库中的数据集创建受众，而无需复制基础数据来管理可操作的营销轮廓和受众。

* 利用一个系统来实现由体验驱动的工作流程：在 Adobe Experience Platform 中策划摄取和联合的受众，并协调所有渠道的出站体验。

* B2C 和 B2B CDP 客户现在可以使用联合受众构成功能，通过集成来自受支持的企业数据仓库的数据来构建基于人群的受众。此外，他们可以通过整合企业数据仓库中的相关属性，丰富现有的 AEP 基于人群的受众，从而增强受众轮廓，实现更加个性化和有针对性的参与度。

## 用例 {#use-cases}

联合受众构成支持&#x200B;**三类**&#x200B;使用场景：受众创建、受众扩充和客户轮廓扩充。

* 受众创建：您可以从数据仓库中创建受众，并将这些受众联合到 Experience Platform 中，通过便于营销人员使用的拖放式用户界面，将其用于 Real-Time CDP 或 Journey Optimizer。因此，您无需复制敏感的底层数据或重复现有数据，即可查询数据仓库。
   * **示例：**&#x200B;利用数据仓库中的历史交易数据创建高价值历史购买者受众，而无需将这些交易数据复制到 Experience Platform 中。

* 受众扩充：您可以通过使用数据仓库中的其他数据集，在 Experience Platform 中为现有受众添加更多详细信息，并将这些信息叠加到受众上——整个过程无需将底层数据复制到 Experience Platform 中。通过受众扩展，您可以借助扩充后的受众实现更出色的个性化体验。
   * **示例：**&#x200B;将 Experience Platform 中的购物车放弃者受众与联合受众构成中的高价值历史购买者受众进行整合，以实现精准的产品建议投放。

* 轮廓扩充：您可以从数据仓库中选择特定的客户属性，以增强 Experience Platform 中的轮廓。通过将联合数据添加到这些轮廓中，您可以更有效地响应客户的实时信号，从而驱动即时体验。
   * **示例：**&#x200B;使用联合受众中的信息丰富 Experience Platform 中的轮廓。现在，您可以根据站点访客的在站行为，向其投放定向产品优惠——前提是该访客属于高价值历史购买者联合受众。

![图表](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

如需了解更多联合受众构成的使用案例，请参阅[《联合受众构成白皮书》](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html)。

## 关键步骤 {#gs-steps}

使用 Adobe 联合受众构成可以直接从数据库创建和更新 Adobe Experience Platform 受众，而无需任何引入过程。

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

关键步骤：

1. **数据集成**：汇集来自不同来源的数据，并将其合并为统一的数据集。若要了解如何连接 Adobe Experience Platform 应用程序以及您的企业数据仓库、所支持的数据库以及如何配置它们，请参阅[本节](../connections/home.md)中的详细说明。

1. **数据建模**：设计和创建定义数据结构、关系和约束的数据模型和架构。要了解有关架构的更多信息，请参阅[此页面](../customer/schemas.md)。在[此页面](../data-management/gs-models.md)中了解如何为您的数据模型创建链接。

1. **数据转换**：应用数据操作技术来修改数据元素的格式、结构或值，使其兼容或适合特定的分析或应用程序。

1. **数据使用**：创建、组织和建立受众。在[此页面](../compositions/gs-compositions.md)中了解如何构成受众。您还可以通过 Adobe Experience Platform 受众门户和目标更新或重复使用现有受众。请参阅[此页面](../connections/destinations.md)了解详情。

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

新的审核记录功能按时间顺序详细记录了实时发生在您的环境中的事件。[了解详情](../admin/audit-trail.md)

## 了解详情 {#learn}

<!-- Workflow + Workflow activities-->


在[此页面](access-prerequisites.md)中了解如何访问联合受众构成、护栏和限制。

也可以在[此页面](faq.md)中查看常见问题解答。


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

