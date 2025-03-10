---
title: 联合受众构成的先决条件和护栏
description: 了解联合受众构成的先决条件、权限和护栏
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 0b8781b5b33d96db7d7f23b3c399942b9cfe901f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 88%

---

# 先决条件和护栏 {#fac-access}

联合受众构成需要 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer **Prime** 或 **Ultimate** 包。要访问此功能，您必须要购买联合受众构成插件。

>[!AVAILABILITY]
>
>在您收到 Adobe 发来的欢迎邮件通知后，界面可能需要几个小时才能更新，功能才会对您可用。

## 支持的系统 {#supported-systems}

联合受众构成支持以下云仓库：

* Amazon Redshift
* Azure Synapse
* 数据块
* Google Big Query
* Snowflake
* Vertica Analytics

在[此页面中了解如何与这些系统建立连接](../connections/connections.md)。

## 沙盒

购买联合受众构成时，您有权使用两个沙盒。 对于任何其他沙盒设置请求，请联系您的 Adobe 代表。

## 权限 {#permissions}

要访问联合受众构成，必须将用户添加到购买时创建的特定沙盒的产品轮廓中，并为其分配&#x200B;**[!UICONTROL 管理联合数据]**&#x200B;的权限。[了解详情](feature-access.md)

## IP 允许列表 {#ip}

要安全地启用联合受众构成来访问您的数据库，您必须授权将会访问这些数据库的联合受众构成服务器的 IP 地址。在 Adobe Experience Platform 用户界面中添加联合数据库时会显示这些 IP 地址。[了解详情](../connections/connections.md)

将这些 IP 地址添加到您的允许列表中，以授予联合受众构成访问权限。

## 护栏和限制 {#fac-guardrails}

* 联合受众构成目前不适用于[引入健康数据的客户](https://experienceleague.adobe.com/zh-hans/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* [Adobe Real-Time Customer Data Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/guardrails){target="_blank"}中列出的授权、产品限制和性能护栏适用于联合受众合成。
