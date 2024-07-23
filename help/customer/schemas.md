---
audience: end-user
title: 模式入门
description: 了解如何开始使用架构
badge: label="限量发布版" type="Informative"
source-git-commit: 75d539eef7b36b721c0df52b2fe9115728cf14d3
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 20%

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


## 什么是架构？ {#schema-start}

架构是数据库表的表示形式。 它是应用程序中的一个对象，用于定义数据如何与数据库表绑定。

通过创建架构，您可以在FAC中处理表：
- 为其提供友好名称和描述，以简化用户的理解
- 根据每个字段的实际使用情况确定其可见性
- 选择其主键，以便根据[数据模型](../data-management/gs-models.md#data-model-start)中的需要链接它们之间的架构

## 创建架构 {#schema-create}

要在FAC中创建架构，请执行以下步骤：
在**[!UICONTROL 联合数据]**&#x200B;部分中，转到&#x200B;**[!UICONTROL 模型]**&#x200B;链接。 您将在其中找到&#x200B;**[!UICONTROL 架构]**选项卡。
单击**[!UICONTROL 创建架构]**&#x200B;按钮。

![](assets/schema_create.png){zoomable="yes"}

您将有权访问一个新界面，该界面包含一个下拉列表，您将在该下拉列表中找到
连接到应用程序的所有数据库。 了解有关[数据库连接](../connections/connections.md#connections-fdb)的更多信息。
在列表中选择源数据库，然后单击**[!UICONTROL 添加表]**&#x200B;选项卡

![](assets/schema_tables.png){zoomable="yes"}

您将可以访问数据库中的所有表的列表。

通过添加要为其创建方案的表，您将有权访问其字段，如下所示。

![](assets/schema_fields.png){zoomable="yes"}

对于每个表，您可以：
- 重命名给定的架构标签
- 添加描述
- 重命名所有字段，并决定其可见性。
- 选择架构主键

例如，在添加之后导入了一个表：

![](assets/schema_lumaorder.png){zoomable="yes"}

可以按如下方式定义架构：

![](assets/schema_lumaorders.png){zoomable="yes"}

## 编辑架构 {#schema-edit}

要编辑架构，请在架构文件夹中单击架构的名称。 您将有权访问以下页面。
单击**[!UICONTROL 编辑]**&#x200B;按钮。

![](assets/schema_edit.png){zoomable="yes"}

在创建架构时，您可以使用与相同的可能性：
- 重命名给定的架构标签
- 添加描述
- 重命名所有字段，并决定其可见性。
- 选择架构主键

![](assets/schema_edit_orders.png){zoomable="yes"}

## 在架构中预览数据 {#schema-preview}

要预览架构所代表的表中的数据，请转到&#x200B;**[!UICONTROL 数据]**选项卡，如下所示。
通过单击**[!UICONTROL 计算]**&#x200B;链接，您可以获得录制的总数。

![](assets/schema_data.png){zoomable="yes"}

您可以通过单击&#x200B;**[!UICONTROL 配置列]**&#x200B;按钮来更改数据概述。

![](assets/schema_columns.png){zoomable="yes"}

## 删除架构 {#schema-delete}

要删除架构，请单击&#x200B;**[!UICONTROL 更多]**&#x200B;按钮，然后单击&#x200B;**[!UICONTROL 删除]**。

![](assets/schema_delete.png){zoomable="yes"}