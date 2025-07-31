---
audience: end-user
title: 使用“保存受众”活动
description: 了解如何使用保存受众活动
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: c133ddb2b1d2a75e7f9614d7623fad63aa24eb55
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 25%

---

# 保存受众 {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="保存受众"
>abstract="使用此活动从构成中的上游计算得出的群体创建新受众。创建的受众被添加到受众的列表，并可通过&#x200B;**受众**&#x200B;菜单找到这些受众。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="生成出站过渡"
>abstract="如果您想在&#x200B;**保存受众**&#x200B;活动之后添加过渡，请使用此选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="主要身份标识字段"
>abstract="选择要用于轮廓的主要身份标识。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="在 Experience Platform 文档中了解详情。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="身份标识命名空间"
>abstract="选择要用于轮廓的命名空间。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces" text="在 Experience Platform 文档中了解详情。"

>[!IMPORTANT]
>
>如果您的沙盒使用&#x200B;**数据集优先级**&#x200B;合并策略，请联系Adobe客户关怀团队以将`Halos UPS`数据集添加到您的合并策略。
>
>如需了解有关合并策略的更多信息，请参阅[合并策略概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/merge-policies/overview)。

利用&#x200B;**[!UICONTROL 保存受众]**&#x200B;活动，可使用组合上游计算的群体创建新受众。 创建的受众将添加到Adobe Experience Platform受众列表，并可通过&#x200B;**受众**&#x200B;菜单使用。 [了解如何使用受众](../../start/audiences.md)

此活动主要用于通过将同一构成中计算得出的群体组转换为可重复使用的受众，将其保留下来。 将其连接到其他定向活动，如&#x200B;**构建受众**&#x200B;或&#x200B;**合并**&#x200B;活动。

**[!UICONTROL 保存受众]**&#x200B;活动会生成一个新的受众架构和相关的数据集，其中可能包含个人身份信息(PII)或受保护的健康信息(PHI)。 创建受众后，请与管理员合作，确保根据组织的数据策略应用适当的数据治理标签。 有关如何应用数据使用标签的详细信息，请参阅[数据使用标签用户指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/data-governance/labels/user-guide)。

## 配置“保存受众”活动 {#save-audience-configuration}

请按照以下步骤配置&#x200B;**保存受众**&#x200B;活动：

1. 将&#x200B;**保存受众**&#x200B;活动添加到合成。

   ![](../assets/save-audience.png)

1. 指定要创建的受众的标签。

   >[!IMPORTANT]
   >
   >受众标签在当前沙盒中必须是唯一的。 标签不能与任何现有受众相同。

1. 使用“受众映射”部分选择要与新创建的受众一起导入的字段。 为此，请单击&#x200B;**添加受众映射**，然后选择源受众和目标受众字段。

   重复该操作，根据需要添加任意数量的受众映射。

1. 选择用于标识数据库中的目标用户档案的主要身份和命名空间：

   * **主标识字段**：选择用于标识用户档案的字段。 例如，其电子邮件地址或电话号码。
   * **标识命名空间**：选择要用于标识配置文件的命名空间，即要用作标识键的数据类型。 例如，如果已选择电子邮件地址作为主身份字段，则应选择身份命名空间&#x200B;**Email**。 如果唯一标识符是电话号码，则应选择身份命名空间&#x200B;**电话**。

## 访问 Adobe Experience Platform 中的受众 {#access-audience}

执行组合后，生成的受众将作为外部受众保存在Adobe Experience Platform中，并在Audience Portal的Adobe Real-Time CDP和/或Adobe Journey Optimizer中可用。 有关受众门户的更多信息，请阅读[受众门户概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}。

创建的受众包含“受众映射”部分中选择的所有字段。 您可以在Journey Optimizer中定位此受众，或将其激活到Adobe Experience Platform支持的任何目标。

[在 Adobe Experience Platform 文档中了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}。

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
