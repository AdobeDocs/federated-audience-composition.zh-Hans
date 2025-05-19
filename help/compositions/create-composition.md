---
audience: end-user
title: 创建合成
description: 了解如何创建合成
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 21%

---

# 创建并配置构成 {#create}

创建构图的第一步是定义其标签并根据需要配置其他设置。

## 创建合成 {#create-the-composition}

1. 访问&#x200B;**[!UICONTROL 受众]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 联合合成]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 创建合成]**&#x200B;按钮。

   ![](assets/composition-create.png)

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;部分中，为合成指定标签并选择数据模型。 只有与此数据模型关联的架构才会在合成的活动中可用。

   ![](assets/composition-select-schema.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。组合画布随即显示。 您现在可以通过在执行构成之前根据需要添加任意数量的活动来配置构成：

   * [了解如何编排活动](orchestrate-activities.md)
   * [了解如何启动和监视合成](start-monitor-composition.md)

## 配置构成设置。 {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="构成属性"
>abstract="此部分提供了通用构成属性，在创建构成时也可以访问这些属性。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="构成分段"
>abstract="通过默认，仅保留最后一次构成执行的工作表。您可以启用此选项来保留工作表以供测试目的。它必须 **仅** 在开发或暂存环境中使用。绝不能在生产环境中检查它。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="错误管理设置"
>abstract="在本部分中，您可以定义在执行期间应如何管理错误。您可以选择暂停流程、忽略一定数量的错误或停止构成执行。"

在访问构成时，您可以访问高级设置，例如，这些设置允许您定义构成在出现错误时的行为。 要访问这些其他选项，请单击位于合成创建屏幕上部的&#x200B;**[!UICONTROL 设置]**&#x200B;按钮。

![](assets/composition-create-settings.png)

可用设置如下：

* **[!UICONTROL 标签]**：更改合成标签。

* **[!UICONTROL 保留两次执行之间的临时人口结果]**：默认情况下，仅保留最后执行合成的工作表。 以前执行的工作表由每天运行的技术构成清除。

  如果启用此选项，则即使在执行合成之后，也会保留工作表。 您可以将其用于测试目的，因此必须&#x200B;**仅**&#x200B;用于开发或暂存环境。 绝不能在生产组合中检查它。

* **[!UICONTROL 错误管理]**：此选项允许您定义在合成活动有错误时要执行的操作。 有三种可能的选项：

   * **[!UICONTROL 挂起进程]**：构成自动暂停，其状态更改为&#x200B;**[!UICONTROL 失败]**。 问题解决后，使用&#x200B;**[!UICONTROL 恢复]**&#x200B;按钮恢复合成。
   * **[!UICONTROL 忽略]**：触发错误的任务状态更改为&#x200B;**[!UICONTROL 失败]**，但构成将保留&#x200B;**[!UICONTROL 已启动]**&#x200B;状态。
   * **[!UICONTROL 中止进程]**：组合自动停止，其状态更改为&#x200B;**[!UICONTROL 失败]**。 问题解决后，请使用&#x200B;**[!UICONTROL 开始]**&#x200B;按钮重新启动合成。

* **[!UICONTROL 连续错误]**：指定进程停止之前可以忽略的错误数。 达到此数字后，撰写状态将更改为&#x200B;**[!UICONTROL 失败]**。 如果此字段的值为0，则无论错误数量如何，合成都不会停止。
