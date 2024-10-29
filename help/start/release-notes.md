---
title: Experience Platform 联合受众构成中的新增功能
description: 最新更新和发行说明。
badge: label="限量发布版" type="Informative"
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 61a70f9de0a6cf171a2ff1128b57ae6206be842c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 53%

---

# 发行说明 {#rn-new}

[!DNL Federated Audience Composition] 不断地提供新功能、对现有功能进行增强和修复错误。所有变更已整合至本发行说明中。 [!DNL Federated Audience Composition] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

## 2024年10月版 {#fac-24-10}

### 兼容性 {#fac-24-10-compat}

在此新版本中，联合受众构成现在与下面列出的系统兼容。

* **数据库支持**

  现在，您可以通过联合受众组合建立与数据库数据库的连接。 [了解详情](../connections/federated-db.md#databricks)

* **支持通过AWS PrivateLink安全访问Snowflake**

  现在支持通过专用链接安全访问外部Snowflake数据仓库。 请注意，您的Snowflake帐户必须托管在Amazon Web Services (AWS)上，并且与您的联合受众构成环境位于同一区域。 请联系您的Adobe代表，以获得设置对您的Snowflake帐户的安全访问权限方面的帮助。 [了解详情](../connections/federated-db.md#snowflake)

* **Amazon Redshift无服务器支持**

  在此新版本中，联合受众组合支持[Amazon Redshift无服务器](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}。

### 改进 {#fac-24-10-improvements}

此版本包含下方列出的改进。

* **刷新现有架构**

  在联合数据库中创建、修改或删除列时，您现在可以通过单击相应架构中的&#x200B;**[!UICONTROL 刷新架构]**&#x200B;按钮来检测并应用更改。 [了解详情](../customer/schemas.md#schema-refresh)

* **将数据模型与新组合关联**

  创建合成时，现在可以选择要与其关联的数据模型。 通过这个新选项，可更轻松地配置活动，因为只有关联数据模型的表可用。 [了解详情](../compositions/create-composition.md)

## 2024年7月版 — 同盟受众构成(LA) {#fac-la}

>[!AVAILABILITY]
>
>Adobe Experience Platform 联合受众构成目前仅对一部分组织提供（限量发布）。
>

联合受众构成是一项附加功能，为企业访问企业数据仓库提供了灵活、扩大的权限，以使用关键企业数据集构成受众，并为由品牌发起的即时体验提供支持。通过这种新方法，作为 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/home){target="_blank"} 和/或 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home){target="_blank"} 用户，您可以直接从现有数据仓库联合受众数据，以在一个系统中扩充 Adobe Experience Platform 受众。

联合受众构成满足了企业日益增长的市场需求，企业则需要灵活地利用仓库数据集来构成受众。这有助于企业减少数据移动，同时向营销团队提供关键受众数据，以满足用例要求并提供个性化体验。 

若要了解有关联合受众构成功能方面的更多信息，请参阅[此页面](get-started.md)，以及[常见问题解答](faq.md)。

有关访问联合受众构成的先决条件和当前护栏的详细信息，请参阅[该页面](access-prerequisites.md)。

