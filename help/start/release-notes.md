---
title: Experience Platform 联合受众构成中的新增功能
description: 最新更新和发行说明。
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 51a6c6154452ae56e495312f1d4e909f4eb2d06e
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 88%

---

# 发行说明 {#rn-new}

[!DNL Federated Audience Composition] 不断地提供新功能、对现有功能进行增强和修复错误。所有变更均已纳入本发行说明中。[!DNL Federated Audience Composition] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}中，进一步了解这些更改。


## 2025年2月更新 {#fac-25-01}

从2月版开始，[!DNL Federated Audience Composition]将开始强制对已获得&#x200B;**管理联合数据**&#x200B;权限的用户访问&#x200B;**联合数据管理**&#x200B;和&#x200B;**联合合成**&#x200B;接口。

我们建议用户联系管理员以将此权限添加到其角色，以便继续访问[!DNL Federated Audience Composition]用户界面。

要了解如何分配此权限，请参阅[详细文档](feature-access.md)。

## 2024 年 11 月版本 {#fac-24-11}

### 改进 {#fac-24-11-improvements}

此版本包含以下改进。

* **IP 地址允许列表**

  在 Adobe Experience Platform 用户界面中添加联合数据库时，您现在可以直接查看与联合受众构成实例关联的 IP 地址。这使您能够轻松复制并授权这些 IPS 连接到您的数据库，以提高安全性和灵活性。[了解详情](../connections/connections.md)

## 2024 年 10 月版本 {#fac-24-10}

>[!AVAILABILITY]
>
>Adobe 体验平台联合受众构成（Adobe Experience Platform Federated Audience Composition）以前面向一组组织（LA），现在面向所有用户（GA）。此附加组件根据您的产品激活，并且只有具有相关权限时才可见。[了解详情](access-prerequisites.md)
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

联合受众构成是一项附加功能，为企业访问企业数据仓库提供了灵活、扩大的权限，以使用关键企业数据集构成受众，并为由品牌发起的即时体验提供支持。通过这种新方法，作为 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/home){target="_blank"} 和/或 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home){target="_blank"} 用户，您可以直接从现有数据仓库联合受众数据，以在一个系统中扩充 Adobe Experience Platform 受众。

联合受众构成满足了企业日益增长的市场需求，企业则需要灵活地利用仓库数据集来构成受众。这有助于企业减少数据移动，同时向营销团队提供关键受众数据，以满足用例要求并提供个性化体验。 

若要了解有关联合受众构成功能方面的更多信息，请参阅[此页面](get-started.md)，以及[常见问题解答](faq.md)。

有关访问联合受众构成的先决条件和当前护栏的详细信息，请参阅[该页面](access-prerequisites.md)。

