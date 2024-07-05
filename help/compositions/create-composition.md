---
audience: end-user
title: 创建合成
description: 了解如何创建合成
source-git-commit: be24c32977cdccab0a5fc7e77a033f4d2b746b9f
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 21%

---


# 创建和配置合成 {#create}

创建构图的第一步是定义其标签并根据需要配置其他设置。

## 创建合成 {#create-the-composition}

1. 访问 **[!UICONTROL 受众]** 菜单并选择 **[!UICONTROL 联合组合]** 选项卡。

1. 单击 **[!UICONTROL 创建合成]** 按钮。

   ![](assets/composition-create.png)

1. 在 **[!UICONTROL 属性]** 部分，为组合指定标签，然后单击 **[!UICONTROL 创建]**.

1. 组合画布随即显示。 您现在可以通过在执行构成之前根据需要添加任意数量的活动来配置构成：

   * [了解如何编排活动](#action-activities)
   * [了解如何启动和监控合成](#save)

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

在访问构成时，您可以访问高级设置，例如，这些设置允许您定义构成在出现错误时的行为。

要访问合成的其他选项，请单击 **设置** 按钮位于构成创建屏幕的上部。

![](assets/composition-create-settings.png)

可用设置如下：

* **[!UICONTROL 标签]**：更改撰写的标签。

* **[!UICONTROL 保留两次执行之间的临时人口结果]**：默认情况下，仅保留构成的最后一次执行的工作表。 以前执行的工作表由每天运行的技术构成清除。

  如果启用此选项，则即使在执行合成之后，也会保留工作表。 您可以将其用于测试目的，因此必须使用 **仅限** 在开发或暂存环境中。 绝不能在生产组合中检查它。

* **[!UICONTROL 错误管理]**：利用此选项，可定义在构成活动出错时应执行的操作。 有三种可能的选项：

   * **[!UICONTROL 暂停进程]**：构成自动暂停，其状态更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 继续]** 按钮。
   * **[!UICONTROL 忽略]**：触发错误的任务的状态更改为 **[!UICONTROL 失败]**，但构图会保留 **[!UICONTROL 已开始]** 状态。
   * **[!UICONTROL 中止进程]**：构成将自动停止，其状态将更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 开始]** 按钮。

* **[!UICONTROL 连续错误]**：指定在停止进程之前可以忽略的错误数。 达到此数字后，构成状态将更改为 **[!UICONTROL 失败]**. 如果此字段的值为0，则无论错误数量如何，合成都不会停止。
