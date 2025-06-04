---
title: 联合受众组合中的隐私和安全性
description: 了解联合受众构成如何处理用户数据的隐私和安全性，包括数据管理、同意实施、访问控制、数据加密和隐私合规性等功能。
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# 联合受众组合中的隐私和安全性

联合受众构成符合大量安全实践，可在处理期间保护您的数据。

## Privacy Service {#privacy}

联合受众组合可为Adobe Experience Platform和Adobe Journey Optimizer提供联合数据以供使用。 但是，联合受众合成&#x200B;**不**&#x200B;存储任何数据仓库中的任何客户数据。 因此，您可以使用Adobe Experience Platform Privacy Service来遵守数据主体和数据删除请求。

例如，在构成画布中使用保存活动块创建受众时，生成的受众将作为外部受众存储在Experience Platform的数据湖中。 此外部受众标记有其身份字段和身份命名空间。 因此，您可以使用Privacy Service通过外部受众访问和删除这些用户档案。

或者，在通过组合画布中的保存配置文件活动创建配置文件扩充后，生成的扩充作为启用配置文件的架构和启用配置文件的数据集存储在Experience Platform中。 此扩充数据使用身份字段和身份命名空间进行标记。 因此，您可以使用Privacy Service来访问和清理这些配置文件。

有关Privacy Service的更多信息，请阅读[Privacy Service概述](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/home){target="_blank"}。

### 隐私请求 {#privacy-requests}

在Privacy Service中，您可以创建和管理个人隐私请求，以从联合受众构成中访问和删除客户数据。 Privacy Service提供[用户界面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans){target="_blank"}和[RESTful API](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/api/overview){target="_blank"}，帮助您管理客户数据请求。

有关创建和管理隐私请求的更多信息，请参阅Privacy Service UI指南](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/ui/user-guide){target="_blank"}中的[隐私作业。

## 同意策略实施 {#consent}

联合受众构成通过Experience Platform提供了一些工具，可让您自动执行同意书，确保根据提供给客户的同意激活受众。

例如，在构成画布中使用保存活动块创建受众时，生成的受众将作为外部受众存储在Experience Platform的数据湖中。 Experience Platform在激活期间自动支持同意验证。 有关详细信息，请阅读[分段服务常见问题解答](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#consent){target="_blank"}。

或者，在通过使用构成画布中的保存配置文件活动创建配置文件扩充后，生成的扩充将作为启用配置文件的架构和启用配置文件的数据集存储在Experience Platform中。 对于现有配置文件，激活期间会自动遵循可用的同意属性。 对于新用户档案，在激活期间自动遵循用户档案摄取期间提供的同意属性。 有关将同意应用于用户档案的详细信息，请阅读[同意和偏好设置字段组指南](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}。

有关应用同意的详细信息，请参阅[管理策略UI指南](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}。

## 数据生命周期 {#data-lifecycle}

由于联合受众合成&#x200B;**不**&#x200B;存储任何数据仓库中的任何客户数据，因此您可以使用Experience Platform处理数据生命周期。 利用高级数据生命周期管理，您可以在数据集和记录级别管理数据生命周期。

例如，在构成画布中使用保存活动块创建受众时，生成的受众将作为外部受众存储在Experience Platform的数据湖中。 由于此数据是&#x200B;**而不是**&#x200B;存储在联合受众构成中，因此当在受众门户中删除受众时，将自动删除受众数据和相应的数据集。

或者，在通过使用构成画布中的保存配置文件活动创建配置文件扩充后，生成的扩充将作为启用配置文件的架构和启用配置文件的数据集存储在Experience Platform中。 因此，您可以使用数据生命周期来访问和清理用户档案。

有关使用数据生命周期的更多信息，请阅读[数据生命周期概述](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/home){target="_blank"}。

## 数据使用情况标签 {#data-usage-labels}

您可以使用数据使用标签，根据应用于该数据的治理策略对数据集和字段进行分类。 使用合成创建受众后，您可以对生成的架构应用适当的数据标签，以确保其符合所需的使用限制。

有关使用数据标签的详细信息，请阅读[数据使用标签概述](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}。

## 加密 {#encryption}

灵活的受众组合通过静态数据加密、传输中加密和客户管理的密钥提供加密。

静态数据是指在联合受众组合中使用的客户数据。 数据由云服务提供商加密，并以加密形式用于联合受众合成。

在联合受众构成中，当数据从一个组件移动到另一个组件时，传输中的数据即指客户数据。 在整个联合受众组合组件中，数据会通过HTTPS使用TLS 1.3进行加密。

有关Adobe如何处理数据加密的更多信息，请阅读有关Experience Platform中[数据加密](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}的指南。

### 客户管理的密钥 {#customer-managed-keys}

客户管理的密钥允许您使用自己的加密密钥加密数据，从而控制数据。 由于联合受众合成&#x200B;**不会**&#x200B;存储任何客户数据，因此您可以直接对生成的受众和增强功能使用客户管理的密钥，因为它们将存储在Experience Platform上的数据湖中。

有关客户管理的密钥的详细信息，请阅读[客户管理的密钥指南](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}。

## 审核日志 {#audit-log}

在联合受众构成中执行的所有创建、读取、更新和删除操作都记录在审核跟踪中。 您可以使用此审核日志来跟踪这些操作、强制实施责任和支持合规性审核。

有关详细信息，请阅读[审核记录概述](/help/admin/audit-trail.md){target="_blank"}。

## 访问控制 {#access-control}

您可以在基于字段和基于角色的级别控制对联合受众组合的访问。 您可以使用这些访问控制来强制实施数据治理策略、限制敏感信息的泄露，以及根据用户责任调整访问权限。

有关联合受众组合中访问控制的详细信息，请参阅[访问联合受众组合指南](/help/start/feature-access.md){target="_blank"}。

## 数据本地化 {#data-localization}

联合受众组合&#x200B;**不**&#x200B;存储任何客户数据。 因此，您需要确保&#x200B;**仅**&#x200B;将外部数据库与匹配的沙盒区域连接，以将数据保留在同一区域。 如果将其他区域的数据库连接到沙盒，则Adobe将&#x200B;**不负责**&#x200B;数据本地化。

## 后续步骤 {#next-steps}

阅读本指南后，您可以更好地了解用于联合受众构成的隐私和安全功能，包括数据治理、隐私合规、同意实施、数据生命周期管理和访问控制。
