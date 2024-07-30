---
title: 联合受众组合的先决条件和防护
description: 了解联合受众组合的先决条件、权限和防护
badge: label="限量发布版" type="Informative"
source-git-commit: e6858ecd06e97b952e59738f299afc90fddeafb7
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 13%

---

# 先决条件和护栏 {#fac-access}

联合受众组合需要Adobe Real-time Customer Data Platform和/或Adobe Journey Optimizer **Prime**&#x200B;或&#x200B;**Ultimate**&#x200B;包。 要访问此功能，您必须已购买联合受众构成加载项。

>[!AVAILABILITY]
>
>在您收到 Adobe 发来的欢迎电子邮件通知后，界面可能需要几个小时才会更新，并为您提供功能。

## 权限 {#permissions}

当您购买联合受众构成加载项时，将同时为每个活动沙盒创建产品配置文件。 此产品配置文件在Admin Console中的&#x200B;**Adobe Experience Platform**&#x200B;产品卡下创建，并遵循以下命名约定： `ACP_FAC - <<SandboxName>> - admin.`要访问特定沙盒的联合受众合成，必须将用户添加到为该沙盒创建的产品配置文件中。

例如，如果激活名为“fac-test”的新沙盒，则会创建相应的产品配置文件“ACP_FAC - fac-test - admin”。 要使用此沙盒访问联合受众合成，需要将用户添加到此产品配置文件。

## IP允许列表 {#ip}

要安全地启用联合受众合成以访问您的数据库，请联系您的Adobe代表以获取将访问它们的联合受众合成服务器的IP地址。

将这些IP地址添加到允许列表以授予对联合受众组合的访问权限。

## 护栏和限制 {#fac-guardrails}

* Federated Audience Composition与Privacy &amp; Security Shield兼容，可用于除医疗保健行业外的所有垂直行业。 目前，联合受众组合无法许可给希望摄取运行状况数据的客户。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* [Adobe Real-time Customer Data Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/guardrails){target="_blank"}中列出的授权、产品限制和性能护栏适用于此加载项。
