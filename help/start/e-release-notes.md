---
title: Experience Platform 联合受众构成中的新增功能
description: 最新更新和发行说明。
hide: true
hidefromtoc: true
exl-id: 23ea1a5d-a0e4-4f47-b0f8-56009bbc0a4a
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: ht
source-wordcount: '980'
ht-degree: 100%

---

# 发行说明 {#rn-new}

[!DNL Federated Audience Composition] 不断地提供新功能、对现有功能进行增强和修复错误。所有变更均已纳入本发行说明中。[!DNL Federated Audience Composition] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2025 年 4 月版本 {#fac-25-4}

### 改进 {#fac-25-4-improvements}

此版本包含以下改进。

* **数据模型画布视图**

  数据模型部分的画布视图在画布布局中使用数据模型的可视化图表、数据模型的链接以及现有的表格视图，从而改进了使用体验。[了解详情](../data-management/gs-models.md)

* **AI 助手**

  AI 助手是一项用户界面功能，用于帮助您导航并了解 Adobe 概念，获取针对特定环境的操作见解。在 Adobe Experience Cloud 的多个产品中均可使用该功能，包括联合受众构成。[了解详情](../start/audiences.md)

* **数据模型名称**

  在“受众”菜单中，**联合构成**&#x200B;选项卡现在显示数据模型名称而不是 ID，从而提高了清晰度和整体可用性。

* **受众**

  当用户选择没有关联任何受众的数据模型时，受众菜单现在会显示所选数据模型的名称或标签。

### 兼容性 {#fac-25-4-compat}

* **Snowflake 安全连接**

  通过这个新版本，联合受众构成支持与 Microsoft Azure 上托管的 Amazon Redshift 数据库建立安全的私有链接连接。[了解详情](../connections/federated-db.md#amazon-redshift)

## 2025 年 3 月版本 {#fac-25-3}

### 改进 {#fac-25-3-improvements}

此版本包含以下改进。

* **联合受众构成权限**

  从 3 月份版本开始，[!DNL Federated Audience Composition] 将开始强制要求已获得&#x200B;**管理联合数据**&#x200B;权限的用户访问&#x200B;**联合数据管理**&#x200B;和&#x200B;**联合构成**&#x200B;界面。

  我们建议用户联系管理员将此权限添加到他们的角色中，以便继续访问 [!DNL Federated Audience Composition] 用户界面。

  要了解如何分配此权限，请参阅[详细说明文档](feature-access.md)。

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)

* **AI Assistant**

    AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. [Learn more](ai-assistant.md)
-->


### 兼容性 {#fac-25-3-compat}

* **Databricks 连接**

  通过这个新版本，联合受众构成现在支持 Databricks 数据库连接的私有链接连接。
这包括通过私有链接与 Amazon Web Services (AWS) 上托管的 Databricks 数据库建立安全连接，以及通过 VPN 与 Microsoft Azure 上托管的 Databricks 数据库建立安全连接。[了解详情](../connections/federated-db.md#databricks)

* **为 B2B CDP 客户提供支持**

  联合受众构成现在可供企业对企业 (B2B) 客户数据平台 (CDP) 客户使用，支持基于人员的受众用例。

* **Snowflake 安全连接**

  通过这个新版本，联合受众构成支持与 Microsoft Azure 上托管的 Snowflake 数据库建立安全的私有链接连接。[了解详情](../connections/federated-db.md#snowflake)

## 2025 年 2 月版本 {#fac-25-2}

此版本包含下方列出的更改。

* **Microsoft Fabric 支持**

  您现在可以通过联合受众构成建立与 Microsoft Fabric 数据库的连接。[了解详情](../connections/federated-db.md)

* **Amazon Redshift Spectrum 支持**

  Amazon Redshift Spectrum 现已支持连接 Amazon Redshift 数据库。[了解详情](../connections/federated-db.md#amazon-redshift)

* **架构创建体验增强**

  通过更新的用户界面，创建架构的过程得到了改进，该界面设计得更加直观且易于导航。这些增强功能为数据从业者提供了一种更顺畅、更高效的数据模型开发方法。[了解详情](../customer/schemas.md)

* **Databricks 的受众扩充支持**

  您现在可以在“读取受众”流程中使用 Databricks，从而激活 Databricks 数据库的活动，并允许将其设置为新的目标。[了解详情](../connections/destinations.md)

## 2024 年 11 月版本 {#fac-24-11}

### 改进 {#fac-24-11-improvements}

此版本包含以下改进。

* **IP 地址允许列表**

  在 Adobe Experience Platform 用户界面中添加联合数据库时，您现在可以直接查看与联合受众构成实例关联的 IP 地址。这使您能够轻松复制并授权这些 IPS 连接到您的数据库，以提高安全性和灵活性。[了解详情](../connections/connections.md)

## 2024 年 10 月版本 {#fac-24-10}

>[!AVAILABILITY]
>
>Adobe 体验平台联合受众构成（Adobe Experience Platform Federated Audience Composition）以前面向一组组织（LA），现在面向所有用户（GA）。此功能根据您的产品激活，并且只有具有相关权限时才可见。[了解详情](access-prerequisites.md)
>

### 兼容性 {#fac-24-10-compat}

通过此新版本，联合受众构成现在与下面列出的系统兼容。

* **Databricks 支持**

  您现在可以通过联合受众构成建立与 Databricks 数据库的连接。[了解详情](../connections/federated-db.md#databricks)

* **支持通过 AWS PrivateLink 安全访问 Snowflake**

  现在支持通过私有链接安全访问您的外部 Snowflake Data Warehouse。请注意，您的 Snowflake 帐户必须在 Amazon Web Services (AWS) 上托管，并且与您的联合受众构成环境位于同一区域。请联系您的 Adobe 代表，以获取有关设置 Snowflake 帐户安全访问权限的帮助。[了解详情](../connections/federated-db.md#snowflake)

* **Amazon Redshift Serverless 支持**

  通过此新版本，联合受众构成支持 [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}。

### 改进 {#fac-24-10-improvements}

此版本包含下方列出的改进。

* **刷新现有架构**

  当在联合数据库中创建、修改或删除某个列时，您现在可以通过单击相应架构中的&#x200B;**[!UICONTROL 刷新架构]**&#x200B;按钮来检测并应用更改。[了解详情](../customer/schemas.md#schema-refresh)

* **将数据模型与新的构成相关联**

  创建构成时，您现在可以选择要与其关联的数据模型。有了这个新选项，活动的配置会变得更加简单，因为只有相关数据模型的表可用。[了解详情](../compositions/create-composition.md)

## 2024 年 7 月版本：联合受众构成 (LA) {#fac-la}

联合受众构成为企业访问企业数据仓库提供了灵活、扩大的权限，以使用关键企业数据集构成受众，并为由品牌发起的即时体验提供支持。通过这种新方法，作为 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/home){target="_blank"} 和/或 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home){target="_blank"} 用户，您可以直接从现有数据仓库联合受众数据，以在一个系统中扩充 Adobe Experience Platform 受众。

联合受众构成满足了企业日益增长的市场需求，企业则需要灵活地利用仓库数据集来构成受众。这有助于企业减少数据移动，同时向营销团队提供关键受众数据，以满足用例要求并提供个性化体验。

要了解有关联合受众构成功能方面的更多信息，请参阅[此页面](get-started.md)以及[常见问题解答](faq.md)。

有关访问联合受众构成的先决条件和当前护栏的详细信息，请参阅[此页面](access-prerequisites.md)。
