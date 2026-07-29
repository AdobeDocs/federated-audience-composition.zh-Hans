---
title: Federated受众组合发行说明
description: 联合受众组合的最新更新和发行说明。
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
TQID: https://experienceleague.adobe.com/AqtqibUr1TNXwQ9lrtVoQ3CBNwyjSMS64e4s8y4iTSc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
source-git-commit: f31a9799fecd72b0fccf84f5656b0ee8a6e7df92
workflow-type: tm+mt
source-wordcount: 825
ht-degree: 11%

---

# 发行说明

[!DNL Federated Audience Composition] 不断地提供新功能、对现有功能进行增强和修复错误。 所有变更均已纳入本发行说明中。 [!DNL Federated Audience Composition] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年7月版 {#fac-26-07}

联合受众构成的7月版本支持以下功能：

| CHE2（瑞士）区域全面提供 |
| --- |
| 您现在可以在CHE2（瑞士）区域中配置联合受众组合实例。 |

### 改进 {#fac-26-07-improvements}

此版本附带以下改进。

- **在历程模拟中支持联合受众组合受众**

  通过历程模拟，您现在可以在使用模拟用户发布之前，测试使用联合受众构成受众创建的历程。 有关详细信息，请阅读[历程模拟入门指南](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs)。

## 2026 年 6 月版本 {#fac-26-06}

联合受众组合的6月版本支持以下功能：

| Google [!DNL BigQuery]的REST API连接器具有[!DNL Apigee]网关支持 |
| --- |
| 您现在可以使用REST API连接器连接到Google [!DNL BigQuery]，并可以选择在使用服务帐户身份验证时通过[!DNL Apigee]网关路由您的连接。 有关使用[!DNL Apigee]连接的更多详细信息，请阅读[连接概述](/help/connections/home.md#apigee)。 |

## 2026年5月版 {#fac-26-05}

针对联合受众组合的5月版本支持以下功能：

| Google [!DNL BigQuery]的工作负载身份联合(WIF)身份验证 |
| --- |
| 您现在可以使用WIF身份验证连接到Google [!DNL BigQuery]。 有关使用WIF身份验证进行连接的更多详细信息，请阅读[连接概述](/help/connections/home.md#wif-configuration)。 |

### 改进 {#fac-26-05-improvements}

此版本附带以下改进。

- **Adobe Journey Optimizer读取受众历程中具有联合受众组合受众的多实体定位**

  您现在可以在Journey Optimizer读取受众历程中将FAC受众属性用作补充标识符。 这使您可以在多个实体（如帐户或订阅级别）激活受众。

  有关详细信息，请参阅历程指南[&#128279;](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier)中的使用补充标识符。

## 2026 年 4 月版本 {#fac-26-04}

4月版的联合受众构成支持以下功能和改进：

### 新功能 {#fac=26-04-feature}

| 新连接器 — Teradata |
| --- |
| Teradata连接器现在可用于联合受众合成。 您可以使用Teradata连接器创建受众和扩充受众用例。 有关Teradata连接器的更多信息，请阅读[连接概述](/help/connections/home.md)。 |

### 改进 {#fac-26-04-improvements}

此版本附带以下改进。

- 对Snowflake的&#x200B;**未加密密钥支持**

  现在，在使用密钥对身份验证与Snowflake数据仓库连接时，您可以使用未加密的密钥。

  若要了解有关将未加密密钥与Snowflake结合使用的更多信息，请阅读[连接概述](/help/connections/home.md)。

## 2026 年 3 月版本 {#fac-26-03}

3月版的联合受众构成支持以下功能：

### 新功能 {#fac-26-03-feature}

| AI支持的分段 |
| --- |
| 您现在可以在AI Assistant中自主创建联合受众合成。 使用AI Assistant创建受众时，AI Assistant会生成一个计划，在您批准之后，该计划将在您的浏览器中执行。 有关使用AI助手创建受众的更多信息，请阅读[AI助手概述](/help/start/ai-assistant.md)。 |

| 用于操作分析的AI助手 |
| --- |
| 现在，您可以向AI助手询问有关联合受众构成中操作见解的问题。 支持的区域包括连接、架构和数据模型。 此版本不支持&#x200B;**联合合成**。 有关联合受众组合中的AI助手的详细信息，请阅读[AI助手概述](/help/start/ai-assistant.md)。 |

## 2026 年 2 月版本 {#fac-26-02}

2月版的联合受众构成支持以下功能：

### 新功能 {#fac-26-02-feature}

| 字段扩充支持 |
| --- |
| 您现在可以在合成中使用保存字段活动。 利用保存字段活动，可通过联合来自外部仓库的数据来扩充Experience Platform架构，从而通过其他属性增强Experience Platform架构。 保存字段活动同时支持B2B和B2C架构。 有关使用此活动的更多信息，请阅读[活动概述](../compositions/activities.md#save-fields)。 |

| 数据库高级身份验证支持 |
| --- |
| 您现在可以使用服务主体身份验证或使用OAuth 2.0通过数据库连接到联合受众合成。 有关创建连接的详细信息，请阅读[连接概述](../connections/home.md#create)。 |

## 2026 年 1 月版本 {#fac-26-01}

1月版的联合受众构成支持以下新功能和改进：

### 新功能 {#fac-26-01-feature}

| Azure Synapse服务主体身份验证支持 |
| --- |
| 您现在可以使用服务主体通过Azure Synapse连接到联合受众合成。 有关创建连接的详细信息，请阅读[连接概述](../connections/home.md#create)。 |

| Adobe Experience Platform客户在Amazon Web Services (AWS)上的可用性 |
| --- |
| 如果您的Experience Platform实例位于AWS上，则现在可以使用联合受众合成。 有关AWS上Experience Platform的更多信息，请阅读[多云概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/multi-cloud)。 |

### 改进 {#fac-26-01-improvements}

此版本附带以下改进。

- **受众的数据过期配置**

  在组合中使用&#x200B;**保存受众**&#x200B;活动时，您现在可以设置数据过期时间。

  要了解有关联合受众组合中的数据过期的更多信息，请阅读[活动指南](../compositions/activities.md#save-audience)。
