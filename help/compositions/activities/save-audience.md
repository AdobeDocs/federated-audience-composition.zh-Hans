---
audience: end-user
title: 使用保存受众活动
description: 了解如何使用保存受众活动
source-git-commit: 6b7a0ae164bdb09b1f5fc067a13e304eec9c5201
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 26%

---


# 保存受众 {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="保存受众"
>abstract="使用此活动更新现有受众或从构成中的上游计算得出的群体创建新受众。创建的受众被添加到受众的列表，并可通过&#x200B;**受众**&#x200B;菜单找到这些受众。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="生成出站过渡"
>abstract="如果您想在&#x200B;**保存受众**&#x200B;活动之后添加过渡，请使用此选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="主要标识字段"
>abstract="选择要用于轮廓的主要标识。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="在 Experience Platform 文档中了解详情。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="标识命名空间"
>abstract="选择要用于轮廓的命名空间。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces" text="在 Experience Platform 文档中了解详情。"

此 **保存受众** 利用活动，可使用合成上游计算的群体更新现有受众或创建新受众。 创建的受众将添加到应用程序受众的列表，并可通过以下方式使用： **受众** 菜单。

此活动主要用于通过将同一构成中计算得出的群体组转换为可重复使用的受众，将其保留下来。 将其连接到其他定向活动，例如 **构建受众** 或 **合并** 活动。

## 配置保存受众活动 {#save-audience-configuration}

按照以下步骤配置 **保存受众** 活动：

1. 添加 **保存受众** 活动添加到合成。

   ![](../assets/save-audience.png)

1. 指定要创建的受众的标签。

1. 单击 **添加受众映射** 然后选择源受众和目标受众字段：

   * **Source受众字段**：
   * **目标受众字段**：

   重复该操作，根据需要添加任意数量的受众映射。

1. 选择用于标识数据库中的目标用户档案的主要身份和命名空间：

   * **主要标识字段**：选择用于标识用户档案的字段。 例如，其电子邮件地址或电话号码。
   * **身份命名空间**：选择用于标识用户档案的命名空间，即用作标识键的数据类型。 例如，如果已选择电子邮件地址作为主身份字段，则身份命名空间 **电子邮件** 应选中。 如果唯一标识符是电话号码，则身份命名空间 **电话** 应选中。

执行合成后，生成的受众将保存在Adobe Experience Platform中 <!-- to check-->，并可在中访问 **受众** 菜单。

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
