---
title: 联合受众组合入门
description: 了解什么是Adobe联合受众组合以及如何在Adobe Experience Platform中使用它
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# 联合受众组合入门 {#gs-fac}

Adobe联合受众构成可帮助Adobe Experience Platform应用程序用户访问其存储到企业数据仓库中的客户数据。 客户数据可以存放在多个数据仓库中，并且应该可以立即访问，而无需复制。

Adobe Experience Platform联合受众构成提供了一种简单而强大的解决方案，用于直接在Adobe Real-time Customer Data Platform中连接企业数据仓库，并对数据仓库的表执行查询。

## 关键步骤 {#gs-steps}

通过Adobe联合受众合成，可直接从数据库创建和更新Adobe Experience Platform受众，而无需任何摄取过程。

![关系图](assets/FAC-diagram.png)

关键步骤：

* **配置**

   1. 连接Adobe Experience Platform和您的企业数据仓库。
支持以下数据库：Snowflake、Google Big Query、Azure synapse、Redshift。
在[此页面](../connections/federated-db.md)中了解详情
   1. 创建架构以选择可从用户界面访问的数据。
在[此页面](../customer/schemas.md)中了解详情
   1. 为数据模型创建链接。
在[此页面](../data-management/gs-models.md)中了解详情

* **撰写受众**

   1. 设计和执行合成以创建受众。
在[此页面](../compositions/gs-compositions.md)中了解详情
   1. 通过Adobe Experience Platform受众门户和目标更新或重用现有受众。
在[此页面](../connections/destinations.md)中了解详情

## 了解详情 {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="执行设置"
>abstract="在此部分中，您可以配置与工作流执行相关的设置，例如工作流历史记录的保留天数。"




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="无法编辑活动"
>abstract="在控制台中为某个&#x200B;**查询**&#x200B;或&#x200B;**扩充**&#x200B;活动配置了其他数据后，扩充数据被考虑并传递到出站转换，但无法编辑该活动。"

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="创建链接"
>abstract="定义链接设置"
