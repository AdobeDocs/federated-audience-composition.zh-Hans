---
audience: end-user
title: 创建合成
description: 了解如何创建合成
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 9%

---


# 创建和执行合成 {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="工作流属性"
>abstract="在此屏幕中，选择要用于创建工作流的模板并指定标签。展开“其他选项”部分以配置更多设置，例如工作流内部名称、其文件夹、时区和主管组等。强烈建议选择一个主管组，以便如果出错，可提醒操作员。"

## 创建合成 {#create}

要创建合成，请执行以下步骤：

1. 访问 **[!UICONTROL 受众]** 菜单并选择 **[!UICONTROL 联合组合]** 选项卡。

1. 单击 **[!UICONTROL 创建合成]** 按钮。

1. 在 **[!UICONTROL 属性]** 部分，为组合指定标签，然后单击 **[!UICONTROL 创建]**.

1. 组合画布随即显示。 您现在可以通过在执行之前，根据需要添加任意数量的活动来配置合成。 您还可以配置其他设置，如合成标签或合成执行时与错误管理相关的选项。

请参阅以下部分以了解详情：

* [配置构成设置](#starting-audience)
* [添加活动](#action-activities)
* [执行构成并监视其执行](#save)

## 配置构成设置 {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="组合属性"
>abstract="本节提供了创建合成时也可以访问的一般合成属性。"

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="组合分段"
>abstract="默认情况下，仅保留最后一次执行合成的工作表。 可启用此选项以保留工作表以进行测试。 必须使用 **仅限** 在开发或暂存环境中。 在生产环境中绝不能对其进行检查。"

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="错误管理设置"
>abstract="在此部分中，您可以定义如何管理执行过程中的错误。 您可以选择暂停进程、忽略特定数量的错误或停止合成执行。"

单击 **设置** 按钮访问构成的其他选项：

* **[!UICONTROL 标签]**：更改撰写的标签。

* **[!UICONTROL 保留两次执行之间的临时人口结果]**：默认情况下，仅保留构成的最后一次执行的工作表。 以前执行的工作表由每天运行的技术工作流清除。

  如果启用此选项，则即使在执行合成之后，也会保留工作表。 您可以将其用于测试目的，因此必须使用 **仅限** 在开发或暂存环境中。 绝不能在生产工作流中勾选该活动。

* **[!UICONTROL 错误管理]**：利用此部分，可定义在合成活动出错时应执行的操作。 有三种可能的选项：

   * **[!UICONTROL 暂停进程]**：构成自动暂停，其状态更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 继续]** 按钮。
   * **[!UICONTROL 忽略]**：触发错误的任务的状态更改为 **[!UICONTROL 失败]**，但构图会保留 **[!UICONTROL 已开始]** 状态。
   * **[!UICONTROL 中止进程]**：构成将自动停止，其状态将更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 开始]** 按钮。

* **[!UICONTROL 连续错误]**：指定在停止进程之前可以忽略的错误数。 达到此数字后，构成状态将更改为 **[!UICONTROL 失败]**. 如果此字段的值为0，则无论错误数量如何，合成都不会停止。

## 添加活动 {#activities}

合成画布允许您配置以在合成中添加所需数量的活动，以满足您的需求。

为此，请单击构成路径上的+按钮，然后添加所需的活动。 右侧窗格将打开，允许您配置新添加的活动。 [了解有关组合中活动以及如何配置它们的更多信息](../compositions/activities/about-activities.md)

要从画布中删除活动，请选择该活动并单击右窗格中的删除按钮。 如果要删除的活动是构成中其他活动的父项，则会显示一条消息，允许您指定是只删除选定活动，还是删除其所有子活动。

## 执行合成 {#execute}

合成准备就绪后，单击 **[!UICONTROL 开始]** 按钮执行，并将生成的受众保存到Adobe Experience Platform中。 »您可以使用监控工作流的执行 **日志** 按钮。 有三个选项卡可帮助您监视执行：

* **[!UICONTROL 日志]**：
* **[!UICONTROL 任务]**：
* **[!UICONTROL 变量]**：
