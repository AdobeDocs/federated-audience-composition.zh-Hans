---
audience: end-user
title: 模式入门
description: 了解如何开始使用架构
badge: label="限量发布版" type="Informative"
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: c2d4ec21f497a1c4ad9c1701b4283edd16ca0611
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 22%

---

# 模式入门 {#schemas}

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
>abstract="您可以根据架构的来源对其进行过滤。选择一个或多个联合数据库来显示其模式。"

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

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;部分中，转到&#x200B;**[!UICONTROL 模型]**&#x200B;链接。 浏览到&#x200B;**[!UICONTROL 架构]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 创建架构]**&#x200B;按钮。

   ![](assets/schema_create.png){zoomable="yes"}

   通过此步骤，您可以使用下拉列表访问新屏幕，其中可查找连接到环境的数据库。 在[本节](../connections/connections.md#connections-fdb)中了解有关数据库连接的更多信息。

1. 在列表中选择源数据库，然后单击&#x200B;**[!UICONTROL 添加表]**&#x200B;选项卡。

   ![](assets/schema_tables.png){zoomable="yes"}

   然后，可以查看数据库中所有表的列表。

1. 通过添加要为其创建方案的表，您可以访问其字段，如下所示：

   ![](assets/schema_fields.png){zoomable="yes"}

   对于每个表，您可以：

   * 更改架构的标签
   * 添加描述
   * 重命名所有字段，并设置其可见性
   * 选择架构主键

   例如，对于导入的下表：

   ![](assets/schema_lumaorder.png){zoomable="yes"}

   可按如下方式定义架构：

   ![](assets/schema_lumaorders.png){zoomable="yes"}

## 编辑架构 {#schema-edit}

要编辑方案，请执行以下操作：

1. 单击“架构”文件夹中架构的名称。

1. 单击&#x200B;**[!UICONTROL 编辑]**&#x200B;按钮。

   ![](assets/schema_edit.png){zoomable="yes"}

   您可以访问与[创建架构](#schema-create)时相同的选项。

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## 在架构中预览数据 {#schema-preview}

要预览架构所代表的表中的数据，请浏览到&#x200B;**[!UICONTROL 数据]**&#x200B;选项卡，如下所示。

单击&#x200B;**[!UICONTROL 计算]**&#x200B;链接预览录制总数。

![](assets/schema_data.png){zoomable="yes"}

单击&#x200B;**[!UICONTROL 配置列]**&#x200B;按钮更改数据显示。

![](assets/schema_columns.png){zoomable="yes"}

## 删除架构 {#schema-delete}

要删除架构，请单击“**[!UICONTROL 更多]**”按钮，然后选择“**[!UICONTROL 删除]**”。

![](assets/schema_delete.png){zoomable="yes"}
