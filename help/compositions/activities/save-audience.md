---
audience: end-user
title: 使用保存受众活动
description: 了解如何使用分支活动
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 12%

---

# 保存受众 {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="保存受众"
>abstract="使用此活动可更新现有受众，或从构成中上游计算的群体创建新受众。 创建的受众被添加到受众的列表，并可通过&#x200B;**受众**&#x200B;菜单找到这些受众。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="生成出站过渡"
>abstract="如果您想在&#x200B;**保存受众**&#x200B;活动之后添加过渡，请使用此选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="主要标识字段"
>abstract="选择用于配置文件的主要身份。"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="请参阅Experience Platform文档以了解详情"


>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="标识命名空间"
>abstract="选择用于配置文件的命名空间。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces" text="请参阅Experience Platform文档以了解详情"



此 **保存受众** 利用活动，可使用合成上游计算的群体更新现有受众或创建新受众。 创建的受众将添加到应用程序受众的列表，并可通过以下方式使用： **受众** 菜单。

此活动主要用于通过将同一构成中计算得出的群体组转换为可重复使用的受众，将其保留下来。 将其连接到其他定向活动，例如 **构建受众** 或 **合并** 活动。

## 配置保存受众活动 {#save-audience-configuration}

按照以下步骤配置 **保存受众** 活动：

1. 添加 **保存受众** 活动添加到合成。

1. 在 **模式** 在下拉列表中，选择要执行的操作：

   * **创建或更新现有受众**：定义 **受众标签**. 如果受众已存在，则将更新受众，否则将创建新受众。

   * **更新现有受众**：选择 **受众** 您希望在现有受众列表中更新。

1. 选择 **更新模式** ，这些规则将应用于现有受众：

   * **使用新数据替换受众内容**：替换所有受众内容。 旧数据会丢失。仅保留来自保存受众活动之集客过渡的数据。 此选项会清除已更新受众的受众类型和定向维度。

   * **使用新数据完成受众**：保留旧受众内容，并将来自保存受众活动之集客过渡的数据添加到旧内容中。

1. 查看 **生成叫客过渡** 选项，如果您希望在 **保存受众** 活动。

随后，受众的详细视图中会提供所保存受众的内容，可通过访问 **受众** 菜单。 此视图中可用的列，对应于集客过渡的列 **保存受众** 活动。

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
