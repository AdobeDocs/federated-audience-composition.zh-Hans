---
title: 联合受众构成中的隐私和安全
description: 了解联合受众构成如何处理用户数据的隐私与安全问题，其中包括数据治理、同意管理、访问控制、数据加密及隐私合规等功能。
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 7429577d99d2f163e7084db056005fe641d1bcf3
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 77%

---

# 数据治理、隐私和安全性

>[!IMPORTANT]
>
>Federated Audience Composition完全符合HIPAA，可用于Healthcare Shield以及Privacy and Security Shield客户。

Federated Audience Composition提供了多种服务和工具，使您能够遵守业务实践、法律义务和开发流程。

这些服务可以分为三类：

- [数据治理](#data-governance)
- [隐私](#privacy)
- [安全性](#security)

## 数据治理 {#data-governance}

您可以使用数据治理来管理和识别客户数据，确保正确地标记这些数据，以遵守您的组织或法规所定义的限制。

### 数据使用情况标签 {#data-usage-labels}

您可以使用数据使用标签，根据应用于该数据的治理策略对数据集和字段进行分类。 在使用构成功能创建受众后，您可以在生成的架构上应用相应的数据标签，以确保其遵循所需的使用限制。

有关在联合受众组合中使用数据标签的更多信息，请阅读[应用访问标签部分](../compositions/gs-compositions.md#access-labels){target="_blank"}。

## 隐私

联合受众组合可为Adobe Experience Platform和Adobe Journey Optimizer提供联合数据以供使用，并确保尊重用户数据的隐私。

### Privacy Service {#privacy-service}

由于联合受众合成&#x200B;**不**&#x200B;存储任何数据仓库中的任何客户数据，因此您可以使用Adobe Experience Platform Privacy Service来遵守数据主体和数据删除请求。

例如，当您在组合画布中使用“保存”操作块创建受众时，生成的受众会作为外部受众存储在 Experience Platform 的数据湖中。该外部受众将标记其身份标识字段和身份标识命名空间。因此，您可以使用 Privacy Service 访问并移除包含在外部受众中的这些轮廓。

或者，当您在组合画布中使用“保存轮廓”操作创建轮廓扩充信息后，生成的扩充数据将作为启用轮廓的架构和启用轮廓的数据集存储在 Experience Platform 中。该扩充数据会标记其身份标识字段和身份标识命名空间。因此，您可以使用 Privacy Service 访问并清除这些轮廓。

有关 Privacy Service 的更多信息，请阅读 [Privacy Service 服务概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/home){target="_blank"}。

### 隐私请求 {#privacy-requests}

在 Privacy Service 中，您可以创建和管理单独的隐私请求以访问和删除联合受众构成中的客户数据。Privacy Service 同时提供[用户界面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans){target="_blank"}和[RESTful API](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/api/overview){target="_blank"}，以帮助您管理客户数据请求。

如需了解有关创建和管理隐私请求的更多信息，请参阅 [Privacy Service UI 指南中的隐私作业](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/ui/user-guide){target="_blank"}。

### 同意政策执行 {#consent}

联合受众构成通过 Experience Platform 提供相关工具，帮助您自动执行同意策略，确保仅基于客户所提供的同意来激活受众。

例如，当您在组合画布中使用“保存”操作块创建受众时，生成的受众会作为外部受众存储在 Experience Platform 的数据湖中。Experience Platform 在激活过程中会自动支持同意验证。有关更多信息，请参阅 [Segmentation Service 常见问题解答](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/faq#consent){target="_blank"}。

或者，当您在组合画布中使用“保存轮廓”操作创建轮廓扩充信息后，生成的扩充数据将作为启用轮廓的架构和启用轮廓的数据集存储在 Experience Platform 中。对于现有轮廓，系统将在激活过程中自动遵循其可用的同意属性。对于新建的轮廓，在轮廓摄取过程中提供的同意属性也将在激活时自动被遵循。如需了解有关如何将同意信息应用于轮廓的更多内容，请参阅[同意与偏好字段组指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}。

如需了解更多有关应用同意策略的信息，请参阅[管理策略用户界面指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}。

### 数据生命周期 {#data-lifecycle}

由于联合受众构成&#x200B;**不会**&#x200B;存储来自任何数据仓库的客户数据，因此您可以通过 Experience Platform 管理数据生命周期。借助高级数据生命周期管理功能，您可以在数据集级别和记录级别上对数据生命周期进行管理。

例如，当您在组合画布中使用“保存”操作块创建受众时，生成的受众会作为外部受众存储在 Experience Platform 的数据湖中。由于这些数据&#x200B;**不会**&#x200B;存储在联合受众构成中，当您在受众门户中删除受众时，相关的受众数据及其对应数据集将被自动删除。

或者，当您在组合画布中使用“保存轮廓”操作创建轮廓扩充信息后，生成的扩充数据将作为启用轮廓的架构和启用轮廓的数据集存储在 Experience Platform 中。因此，您可以使用数据生命周期管理功能来访问并清除这些轮廓。

如需了解更多关于使用数据生命周期管理功能的信息，请参阅[数据生命周期概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/data-lifecycle/home){target="_blank"}。

## 安全性 {#security}

数据安全可确保您的数据在联合受众构成中受到保护。

### 加密 {#encryption}

联合受众组合通过静态数据加密、传输中加密和客户管理的密钥提供加密。

静态数据是指在联合受众构成中使用的客户数据。该数据由云服务提供商进行加密，并在联合受众构成中以加密形式使用。

传输中数据是指在联合受众构成中，客户数据在各组件之间传输时的状态。在联合受众构成的各个组件中，数据始终通过基于 HTTPS 的 TLS 1.3 协议保持加密状态。

如需了解 Adobe 如何处理数据加密的更多信息，请参阅 [Experience Platform 中的数据加密](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}。

### 客户管理密钥 {#customer-managed-keys}

客户管理密钥使您能够使用自有加密密钥对数据进行加密，从而实现对数据的自主控制。由于联合受众构成&#x200B;**不会**&#x200B;存储任何客户数据，您可以将客户管理密钥直接应用于生成的受众和扩充数据，因为这些数据将存储在 Experience Platform 的数据湖中。

如需了解更多关于客户管理密钥的信息，请参阅[客户管理密钥指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}。

### 审核日志 {#audit-log}

在联合受众构成中执行的所有创建、读取、更新和删除操作都会记录在审计日志中。您可以利用审计日志追踪这些操作，强化责任归属，并支持合规性审计。

如需了解更多信息，请参阅[审计日志概述](/help/admin/audit-trail.md){target="_blank"}。

### 访问控制 {#access-control}

您可以在字段级别和角色级别控制对联合受众构成的访问权限。您可以利用这些访问控制机制来执行数据治理策略、限制敏感信息的暴露，并确保访问权限与用户职责保持一致。

有关联合受众组合中访问控制的详细信息，请参阅[访问控制指南](/help/governance-privacy-security/access-control.md){target="_blank"}。

### 数据本地化 {#data-localization}

联合受众构成&#x200B;**不会**&#x200B;存储任何客户数据。 因此，您需要确保&#x200B;**仅**&#x200B;将外部数据库连接到相应的沙盒区域，以便将数据保留在同一地区。如果您将其他区域的数据库连接到某个沙盒，Adobe 将&#x200B;**不**&#x200B;对数据本地化负责。

## 后续步骤 {#next-steps}

阅读本指南后，您可以更好地了解用于联合受众组合的数据治理、隐私和安全功能，包括数据使用标签、隐私合规、同意实施、数据生命周期管理和访问控制。
