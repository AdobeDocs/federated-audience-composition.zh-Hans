---
audience: end-user
title: Create compositions
description: Learn how to create compositions
badge: label="限量发布版" type="Informative"
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: bd3223a77f490a43487e21662d8f766d4f9b06fc
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 21%

---

# 创建并配置构成 {#create}

创建合成的第一步是定义其标签并根据需要配置其他设置。

## Create the composition {#create-the-composition}

1. ********

1. ****

   ![](assets/composition-create.png)

1. **** Only the schemas associated to this data model will be available in your composition&#39;s activities.

   ![](assets/composition-select-schema.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。The composition canvas displays. You can now configure your composition by adding as many activities as needed to suit your needs before executing it:

   * [Learn how to orchestrate activities](orchestrate-activities.md)
   * [](start-monitor-composition.md)

## 配置构成设置。 {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="构成属性"
>abstract="此部分提供了通用构成属性，在创建构成时也可以访问这些属性。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="构成分段"
>abstract="通过默认，仅保留最后一次构成执行的工作表。您可以启用此选项来保留工作表以供测试目的。它必须 **仅** 在开发或登台环境中使用。绝不能在生产环境中检查它。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="错误管理设置"
>abstract="在本部分中，您可以定义在执行期间应如何管理错误。您可以选择暂停流程、忽略一定数量的错误或停止构成执行。"

When accessing a composition, you can access advanced settings that allow you, for example, to define how the composition should behave in case of error. ****

![](assets/composition-create-settings.png)

Available settings are as follows:

* **[!UICONTROL 标签]**：更改合成的标签。

* **[!UICONTROL 在两个执行之间保留临时填充的结果]**：默认情况下，仅保留合成的最后一个执行的工作表。 Working tables from previous executions are purged by a technical composition, which runs on a daily basis.

  If this option is enabled, working tables will be kept even after the composition has been executed. **** It must never be checked in a production composition.

* **** There are three possible options:

   * ************
   * ************
   * ************

* **[!UICONTROL 连续错误]**：指定在停止进程之前可以忽略的错误数。 达到此数字后，合成状态将更改为&#x200B;**[!UICONTROL 失败]**。 如果此字段的值为0，则无论错误数量如何，合成都不会停止。
