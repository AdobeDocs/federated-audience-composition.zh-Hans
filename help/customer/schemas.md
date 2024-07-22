---
audience: end-user
title: 模式入门
description: 了解如何开始使用架构
badge: label="限量发布版" type="Informative"
source-git-commit: 883ba223f6c78783fae9f6c9617daa1a7e6635de
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 34%

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

方案是应用程序中的一个对象，它定义数据如何与数据库表绑定。
架构引用表。

## 创建架构 {#schema-create}

在&#x200B;**[!UICONTROL 联合数据]**&#x200B;部分中，转到&#x200B;**[!UICONTROL 模型]**&#x200B;链接。 您将在其中找到&#x200B;**[!UICONTROL 架构]**选项卡。
单击**[!UICONTROL 创建架构]**&#x200B;按钮。

![](assets/schema_create.png){zoomable="yes"}

在下拉列表中选择源数据库，然后单击&#x200B;**[!UICONTROL 添加表]**&#x200B;选项卡

![](assets/schema_tables.png){zoomable="yes"}

您将有权访问数据库中的所有表，并且可为这些表创建方案。

通过添加这些表，您将可以访问它们的字段，并且可以管理以保留您真正需要的。

![](assets/schema_fields.png){zoomable="yes"}

## 编辑架构 {#schema-edit}

要编辑架构，请在架构文件夹中单击架构的名称。 您将有权访问以下页面。
单击**[!UICONTROL 编辑]**&#x200B;按钮。

![](assets/schema_edit.png){zoomable="yes"}

## 在架构中预览数据 {#schema-preview}

要预览架构所代表的表中的数据，请转到&#x200B;**[!UICONTROL 数据]**&#x200B;选项卡，如下所示。

![](assets/schema_data.png){zoomable="yes"}

您可以通过单击&#x200B;**[!UICONTROL 配置列]**&#x200B;按钮来更改数据概述。

![](assets/schema_columns.png){zoomable="yes"}

## 删除架构 {#schema-delete}

要删除架构，请单击&#x200B;**[!UICONTROL 更多]**&#x200B;按钮，然后单击&#x200B;**[!UICONTROL 删除]**。

![](assets/schema_delete.png){zoomable="yes"}