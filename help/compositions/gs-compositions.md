---
audience: end-user
title: 合成快速入门
description: 了解如何开始使用合成
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 8%

---

# 合成快速入门 {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="组合属性"
>abstract="本节提供了创建合成时也可以访问的一般合成属性。"

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="组合分段"
>abstract="默认情况下，仅保留最后一次执行合成的工作表。 可启用此选项以保留工作表以进行测试。 必须使用 **仅限** 在开发或暂存环境中。 在生产环境中绝不能对其进行检查。"




## 什么是组合？ {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="构成"
>abstract="在此屏幕中，您可以访问组合的完整列表，检查其当前状态、上次/下次执行日期，以及创建新组合。"


## 错误管理设置  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="错误管理设置"
>abstract="在此部分中，您可以定义如何管理执行过程中的错误。 您可以选择暂停进程、忽略特定数量的错误或停止合成执行。"

* **[!UICONTROL 错误管理]**：利用此字段，可定义在构成活动出错时应执行的操作。
有三种可能的选项：

   * **[!UICONTROL 暂停进程]**：构成自动暂停，其状态更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 继续]** 按钮。
   * **[!UICONTROL 忽略]**：触发错误的任务的状态更改为 **[!UICONTROL 失败]**，但构图会保留 **[!UICONTROL 已开始]** 状态。
   * **[!UICONTROL 中止进程]**：构成将自动停止，其状态将更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 开始]** 按钮。

* **[!UICONTROL 连续错误]**：当满足以下条件时，此字段将变为可用 **[!UICONTROL 忽略]** 值在 **[!UICONTROL 发生错误时]** 字段。 您可以指定在流程停止前可忽略的错误的数量。达到此数字后，构成状态将更改为 **[!UICONTROL 失败]**. 如果此字段的值为0，则无论错误数量如何，合成都不会停止。
