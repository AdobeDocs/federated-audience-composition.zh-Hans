---
audience: end-user
title: 架构入门
description: 了解如何开始使用架构
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 18%

---

# 架构入门 {#schemas}

>[!AVAILABILITY]
>
>要访问架构，您需要以下权限之一：
>
>-**管理联合架构**
>-**查看联合架构**
>
>有关所需权限的更多信息，请参阅[访问联合受众组合指南](/help/start/feature-access.md)。

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="选择表"
>abstract="选择要为数据模型添加的表。"

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="键"
>abstract="选择一个数据协调的键。"

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="架构的名称。"
>abstract="输入架构的名称。"


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="架构描述"
>abstract="架构描述列出了列、类型和标签。您还可以检查架构的协调密钥。要更新架构定义，请单击铅笔图标。"

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="选择要过滤的源数据库"
>abstract="您可以根据架构的来源对其进行过滤。选择一个或多个联合数据库来显示其架构。"

## 什么是架构 {#schema-start}

架构是数据库表的表示形式。 它是应用程序中的一个对象，用于定义数据如何与数据库表绑定。

通过创建架构，您可以在Experience Platform联合受众构成中定义表的表示形式：

* 为其提供友好名称和描述，以简化用户的理解
* 根据每个字段的实际使用情况确定其可见性
* 选择其主键，以便根据[数据模型](../data-management/gs-models.md#data-model-start)中的需要链接它们之间的架构

>[!CAUTION]
>
>使用同一数据库连接多个沙盒时，必须使用不同的工作架构。
>

## 创建架构 {#schema-create}

要在联合受众构成中创建架构，请执行以下步骤：

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;部分中，访问&#x200B;**[!UICONTROL 模型]**&#x200B;菜单。 浏览到&#x200B;**[!UICONTROL 架构]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 创建架构]**。

   ![](assets/schema_create.png){zoomable="yes"}

   通过此步骤，您可以使用下拉列表访问新屏幕，其中可查找连接到环境的数据库。 在[本节](../connections/connections.md#connections-fdb)中了解有关数据库连接的更多信息。

1. 在列表中选择源数据库，然后单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/schema_tables.png){zoomable="yes"}

   然后，可以查看数据库中所有表的列表。

1. 选择要为其创建方案的表。

1. 每个选定的表都生成一个包含选定列的模式。 根据需要配置架构及其列。

   ![](assets/schema_fields.png){zoomable="yes"}

   对于每个表，您可以：

   * 更改架构的标签
   * 添加描述
   * 重命名所有字段标签，并设置其可见性
   * 选择架构主键

   可以按如下方式定义架构：

   ![](assets/schema_example.png)

1. 完成配置后，单击&#x200B;**[!UICONTROL 完成]**。

## 编辑架构 {#schema-edit}

要编辑架构，请执行以下步骤：

1. 访问您之前创建的架构。

1. 单击&#x200B;**[!UICONTROL 编辑]**&#x200B;按钮。

   ![](assets/schema_edit.png){zoomable="yes"}

1. 从&#x200B;**[!UICONTROL 编辑架构]**&#x200B;窗口，您可以访问和配置与[创建架构](#schema-create)时相同的选项。

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## 在架构中预览数据 {#schema-preview}

要预览架构所代表的表中的数据，请浏览到&#x200B;**[!UICONTROL 数据]**&#x200B;选项卡，如下所示。

单击&#x200B;**[!UICONTROL 计算]**&#x200B;链接预览录制总数。

![](assets/schema_data.png){zoomable="yes"}

单击&#x200B;**[!UICONTROL 配置列]**&#x200B;按钮更改数据显示。

![](assets/schema_columns.png){zoomable="yes"}

## 刷新架构 {#schema-refresh}

可以更新、添加或删除联合数据库中的表。 在这种情况下，您必须刷新Adobe Experience Platform中的架构以符合最新更改。 要执行此操作，请单击要更新的架构名称旁边的三个圆点，然后选择&#x200B;**刷新架构**。

您也可以在编辑架构定义时更新该定义。

![](assets/schema_refresh.png){zoomable="yes"}


## 删除架构 {#schema-delete}

要删除架构，请单击“**[!UICONTROL 更多]**”按钮，然后选择“**[!UICONTROL 删除]**”。

![](assets/schema_delete.png){zoomable="yes"}
