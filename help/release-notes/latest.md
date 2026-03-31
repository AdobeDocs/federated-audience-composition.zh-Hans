---
title: Federated受众组合发行说明
description: 联合受众组合的最新更新和发行说明。
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: d3a97b5887778f910ca8f09f7cb8fa99360a612c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 8%

---


# 发行说明

[!DNL Federated Audience Composition] 不断地提供新功能、对现有功能进行增强和修复错误。 所有变更已整合至本发行说明中。[!DNL Federated Audience Composition] 原生构建于[!DNL Adobe Experience Platform]上并继承了其最新的创新和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年3月版 {#fac-26-03}

3月版的联合受众构成支持以下功能：

### 新功能 {#fac-26-03-feature}

| AI支持的分段 |
| --- |
| 您现在可以在AI Assistant中自主创建联合受众合成。 使用AI Assistant创建受众时，AI Assistant会生成一个计划，在您批准之后，该计划将在您的浏览器中执行。 有关使用AI助手创建受众的更多信息，请阅读[AI助手概述](/help/start/ai-assistant.md)。 |

| 用于操作分析的AI助手 |
| --- |
| 现在，您可以向AI助手询问有关联合受众构成中操作见解的问题。 支持的区域包括连接、架构和数据模型。 此版本不支持&#x200B;**联合合成**。 有关联合受众组合中的AI助手的详细信息，请阅读[AI助手概述](/help/start/ai-assistant.md)。 |

## 2026年2月版 {#fac-26-02}

2月版的联合受众构成支持以下功能：

### 新功能 {#fac-26-02-feature}

| 字段扩充支持 |
| --- |
| 您现在可以在合成中使用保存字段活动。 利用保存字段活动，可通过联合来自外部仓库的数据来扩充Experience Platform架构，从而通过其他属性增强Experience Platform架构。 保存字段活动同时支持B2B和B2C架构。 有关使用此活动的更多信息，请阅读[活动概述](../compositions/activities.md#save-fields)。 |

| 数据库高级身份验证支持 |
| --- |
| 您现在可以使用服务主体身份验证或使用OAuth 2.0通过数据库连接到联合受众合成。 有关创建连接的详细信息，请阅读[连接概述](../connections/home.md#create)。 |

## 2026年1月版 {#fac-26-01}

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
