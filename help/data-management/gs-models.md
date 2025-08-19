---
audience: end-user
title: 开始使用数据模型
description: 了解如何开始使用数据模型
exl-id: 7e1f74c4-b89a-480c-8e12-0257a71e629d
source-git-commit: d8fd926a445e65b6c7310d2ceac5a83ba9fece3f
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 34%

---


# 开始使用数据模型 {#data-model-beta}

>[!AVAILABILITY]
>
>要访问数据模型，您需要以下权限之一：
>
>-**管理联合数据模型**
>&#x200B;>-**查看联合数据模型**
>
>有关所需权限的更多信息，请阅读[访问控制指南](/help/governance-privacy-security/access-control.md)。

## 什么是数据模型 {#data-model-start}

数据模型是一组架构、受众以及它们之间的链接。 它用于将受众与数据库数据联合起来。

在联合受众构成中，您可以直接在画布视图中创建和管理数据模型。 这包括添加架构和受众，以及根据用例定义它们之间的链接。

了解有关[架构](../customer/schemas.md#schema-start)和[受众](../start/audiences.md)的更多信息。

例如，您可以在下文中看到数据模型的表示形式：具有其名称的表以及它们之间的链接。

![](assets/datamodel.png){zoomable="yes"}

## 创建数据模型 {#data-model-create}

要创建数据模型，请执行以下步骤：

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;部分中，访问&#x200B;**[!UICONTROL 模型]**&#x200B;菜单，并浏览到&#x200B;**[!UICONTROL 数据模型]**&#x200B;选项卡。

   选择&#x200B;**[!UICONTROL 创建数据模型]**&#x200B;按钮。

   ![](assets/datamodel_create.png){zoomable="yes"}

2. 定义数据模型的名称，然后选择&#x200B;**[!UICONTROL 创建]**&#x200B;按钮。

3. 从数据模型仪表板中，选择&#x200B;**[!UICONTROL 添加架构]**&#x200B;以选择与数据模型关联的架构。

   ![](assets/datamodel_schemas.png){zoomable="yes"}

4. 此外，您还可以将受众添加到数据模型。 选择&#x200B;**[!UICONTROL 添加受众]**&#x200B;以定义目标组。

   ![](assets/datamodel-audiences.png){zoomable="yes"}

5. 在数据模型中的表之间建立连接，以确保准确的数据关系。 有关详细信息，请阅读[创建链接部分](#data-model-links)。

6. 完成配置后，选择&#x200B;**[!UICONTROL 保存]**&#x200B;以应用更改。

## 创建链接 {#data-model-links}

>[!NOTE]
>
>如果要创建具有多个联接的链接，则只能使用源和目标架构的相同组合一次。

>[!BEGINTABS]

>[!TAB 表视图]

要从表视图选项卡创建数据模型表之间的链接，请执行以下步骤：

1. 选择某个表旁边的![三个圆点图标](/help/assets/icons/more.png)后跟&#x200B;**[!UICONTROL 创建链接]**，或者在&#x200B;**[!UICONTROL 链接]**&#x200B;部分中选择&#x200B;**[!UICONTROL 创建链接]**：

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

2. 填写给定的表单以定义链接。

   ![](assets/datamodel_link.png){zoomable="yes"}

   **基数**

   * **1-N**：源表的一个项可以对应目标表的多个项，但目标表的一个项最多对应源表的一个项。

   * **N-1**：目标表的一个项可以对应源表的多个项，但源表的一个项最多对应目标表的一个项。

   * **1-1**：源表的一个项最多对应目标表的一个项。

   要创建多连接链接，请选择加号图标。 现在，您可以在架构字段之间创建多个联接。

   ![加号按钮突出显示，允许您为模型创建多个连接链接。](assets/multi-join.png){zoomable="yes"}

为数据模型定义的所有链接如下所示：

![](assets/datamodel_alllinks.png){zoomable="yes"}

>[!TAB 画布视图]

要从“画布视图”选项卡创建数据模型表之间的链接，请执行以下步骤：

1. 访问数据模型的“画布”视图，然后选择要链接的两个表

2. 选择Source联接旁边的![](assets/do-not-localize/Smock_AddCircle_18_N.svg)按钮，然后拖动箭头并引导至Target联接以建立连接。

   ![](assets/datamodel.gif){zoomable="yes"}

3. 填写给定表单以定义链接，并在配置后选择&#x200B;**[!UICONTROL 应用]**。

   ![](assets/datamodel-canvas-1.png){zoomable="yes"}

   **基数**

   * **1-N**：源表的一个项可以对应目标表的多个项，但目标表的一个项最多对应源表的一个项。

   * **N-1**：目标表的一个项可以对应源表的多个项，但源表的一个项最多对应目标表的一个项。

   * **1-1**：源表的一个项最多对应目标表的一个项。

4. 数据模型中定义的所有链接在画布视图中均表示为箭头。选择两个表之间的箭头以查看详细信息、进行编辑或根据需要删除链接。

   ![](assets/datamodel-canvas-2.png){zoomable="yes"}

5. 使用工具栏自定义和调整画布。

   ![](assets/datamodel-canvas-3.png)

   * **[!UICONTROL 放大]**：放大画布，更清楚地查看数据模型的详细信息。
   * **[!UICONTROL 缩小]**：缩小画布大小，以便更全面地查看数据模型。
   * **[!UICONTROL 适合视图]**：调整缩放以适合可见区域中的所有架构和/或受众。
   * **[!UICONTROL 切换交互]**：启用或禁用用户与画布的交互。
   * **[!UICONTROL 筛选]**：选择要在画布中显示的架构。
   * **[!UICONTROL 强制自动布局]**：自动排列架构和/或受众以更好地进行组织。

>[!ENDTABS]

## 操作方法视频 {#data-model-video}

请在此视频中了解如何创建数据模型：

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
