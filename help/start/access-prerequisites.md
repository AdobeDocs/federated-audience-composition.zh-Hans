---
title: 联合受众构成的先决条件和护栏
description: 了解联合受众构成的先决条件、权限和护栏
badge: label="限量发布版" type="Informative"
source-git-commit: 07170ee709c9e3c4ad0bb2390aa0d44adae3b059
workflow-type: ht
source-wordcount: '274'
ht-degree: 100%

---

# 先决条件和护栏 {#fac-access}

联合受众构成需要 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer **Prime** 或 **Ultimate** 包。要访问此功能，您必须要购买联合受众构成插件。

>[!AVAILABILITY]
>
>在您收到 Adobe 发来的欢迎邮件通知后，界面可能需要几个小时才能更新，功能才会对您可用。

## 权限 {#permissions}

当您购买联合受众构成插件时，系统会为每个活动沙盒创建一个产品配置文件。此产品配置文件是在 Admin Console 中的 **Adobe Experience Platform** 产品卡下创建的，并遵循以下命名惯例：`ACP_FAC - <<SandboxName>> - admin.`要访问特定沙盒的联合受众构成，必须将用户添加到为该沙盒创建的产品配置文件中。

例如，如果激活了一个名为“fac-test”的新沙盒，则会创建相应的产品配置文件“ACP_FAC - fac-test - admin”。为了使用此沙盒访问联合受众构成，需要将用户添加到此产品配置文件中。

## IP 允许列表 {#ip}

要安全地启用联合受众构成来访问您的数据库，请联系您的 Adobe 代表以获取将会访问这些数据库的联合受众构成服务器的 IP 地址。

将这些 IP 地址添加到您的允许列表中，以授予联合受众构成访问权限。

## 护栏和限制 {#fac-guardrails}

* 目前，联合受众构成不适用于[获取健康数据](https://experienceleague.adobe.com/zh-hans/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}的客户以及 Adobe Journey Optimizer 隐私与安全护盾客户。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}。

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* [Adobe Real-Time Customer Data Platform 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/guardrails){target="_blank"}中列出的相关权限、产品限制和性能护栏适用于此插件。
