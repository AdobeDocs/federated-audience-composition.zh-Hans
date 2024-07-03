---
audience: end-user
title: 创建合成
description: 了解如何创建合成
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# 配置构成设置 {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="组合属性"
>abstract="本节提供了创建合成时也可以访问的一般合成属性。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="组合分段"
>abstract="默认情况下，仅保留最后一次执行合成的工作表。 可启用此选项以保留工作表以进行测试。 必须使用 **仅限** 在开发或暂存环境中。 在生产环境中绝不能对其进行检查。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="错误管理设置"
>abstract="在此部分中，您可以定义如何管理执行过程中的错误。 您可以选择暂停进程、忽略特定数量的错误或停止合成执行。"

在访问合成时，您可以访问高级设置，以便定义合成在发生错误时的行为，或管理应清除合成历史记录的延迟。

要访问合成的其他选项，请单击 **设置** 按钮的位置。

![](assets/composition-create-settings.png)

可用设置如下：

* **[!UICONTROL 标签]**：更改撰写的标签。

* **[!UICONTROL 保留两次执行之间的临时人口结果]**：默认情况下，仅保留构成的最后一次执行的工作表。 以前执行的工作表由每天运行的技术构成清除。

  如果启用此选项，则即使在执行合成之后，也会保留工作表。 您可以将其用于测试目的，因此必须使用 **仅限** 在开发或暂存环境中。 绝不能在生产组合中检查它。

* **[!UICONTROL 错误管理]**：利用此部分，可定义在合成活动出错时应执行的操作。 有三种可能的选项：

   * **[!UICONTROL 暂停进程]**：构成自动暂停，其状态更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 继续]** 按钮。
   * **[!UICONTROL 忽略]**：触发错误的任务的状态更改为 **[!UICONTROL 失败]**，但构图会保留 **[!UICONTROL 已开始]** 状态。
   * **[!UICONTROL 中止进程]**：构成将自动停止，其状态将更改为 **[!UICONTROL 失败]**. 问题解决后，请使用 **[!UICONTROL 开始]** 按钮。

* **[!UICONTROL 连续错误]**：指定在停止进程之前可以忽略的错误数。 达到此数字后，构成状态将更改为 **[!UICONTROL 失败]**. 如果此字段的值为0，则无论错误数量如何，合成都不会停止。
