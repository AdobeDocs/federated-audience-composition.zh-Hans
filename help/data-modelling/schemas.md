---
audience: end-user
title: 架构入门
description: 了解如何开始使用架构
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 9b951f74443ac149e837c3f52ca265acabd407b9
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 16%

---

# 架构概述 {#schemas}

>[!AVAILABILITY]
>
>要访问架构，您需要以下权限之一：
>
>-**管理联合架构**
>-**查看联合架构**
>
>有关所需权限的更多信息，请阅读[访问控制指南](/help/governance-privacy-security/access-control.md)。

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
>abstract="架构描述列出了列、类型和标签。您还可以检查架构的协调密钥。要更新架构定义，请选择铅笔图标。"

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="选择要过滤的源数据库"
>abstract="您可以根据架构的来源对其进行过滤。选择一个或多个联合数据库来显示其架构。"

架构是数据库表的表示形式。 它是应用程序中的一个对象，用于定义数据如何与数据库表绑定。

通过创建架构，您可以在Experience Platform联合受众构成中定义表的表示形式：

* 为其提供友好名称和描述，以简化用户的理解
* 根据每个字段的实际使用情况确定其可见性
* 选择其主键，以便根据[数据模型](../data-modelling/models.md#data-model-start)中的需要链接它们之间的架构

>[!CAUTION]
>
>使用同一数据库连接多个沙盒时，必须使用不同的工作架构。

## 创建架构 {#schema-create}

要在联合受众组合中创建架构，请在&#x200B;**[!UICONTROL 联合数据]**&#x200B;部分中选择&#x200B;**[!UICONTROL 模型]**。 在&#x200B;**[!UICONTROL 架构]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL 创建架构]**。

![“创建架构”按钮在“联合受众组合”架构部分中突出显示。](assets/schemas/schema_create.png){zoomable="yes"}

出现&#x200B;**[!UICONTROL Select federated database]**&#x200B;弹出框。 在此弹出窗口中，您可以选择[源数据库](/help/connections/home.md)，然后选择&#x200B;**[!UICONTROL 下一步]**。


![](assets/schemas/schema_tables.png){zoomable="yes"}

出现&#x200B;**选择表**&#x200B;弹出框。 在此弹出窗口中，可以选择要用于创建方案的表。

![将显示“选择表”弹出框。](assets/schemas/select-table.png){zoomable="yes"}

每个选定的表都生成一个包含选定列的模式。 对于每个表，可以更改方案的标签、添加说明、重命名字段标签、设置字段标签可见性并选择方案主键。

![](assets/schemas/schema-fields.png){zoomable="yes"}

>[!NOTE]
>
>如果启用&#x200B;**[!UICONTROL 使用组合键]**，但只选择一个要使用的键，则该键将被视为标准架构主键。

此外，您可以创建一个由多个架构列组成的键。 打开&#x200B;**[!UICONTROL 使用复合键]**，并标记要用作复合键的键。

![](assets/schemas/composite-key.png){zoomable="yes"}

完成配置后，选择&#x200B;**[!UICONTROL 完成]**&#x200B;以完成架构创建。

## 编辑架构 {#schema-edit}

要编辑架构，请在&#x200B;**架构**&#x200B;页面上选择您之前创建的架构。

此时将显示“方案详细资料”页。 选择![铅笔图标](/help/assets/icons/edit.png)以编辑架构。

![](assets/schemas/schema_edit.png){zoomable="yes"}

在&#x200B;**[!UICONTROL 编辑架构]**&#x200B;窗口中，您可以访问和配置与[创建架构](#schema-create)时相同的选项。

![](assets/schemas/schema_edit_orders.png){zoomable="yes"}

## 在架构中预览数据 {#schema-preview}

要预览架构所代表的表中的数据，请浏览到&#x200B;**[!UICONTROL 数据]**&#x200B;选项卡，如下所示。

选择&#x200B;**[!UICONTROL 计算]**&#x200B;链接以预览录制总数。

![](assets/schemas/schema_data.png){zoomable="yes"}

选择&#x200B;**[!UICONTROL 配置列]**&#x200B;按钮以更改数据显示。

![](assets/schemas/schema_columns.png){zoomable="yes"}

## 刷新架构 {#schema-refresh}

可以更新、添加或删除联合数据库中的表。 在这种情况下，您必须刷新Adobe Experience Platform中的架构以符合最新更改。 要执行此操作，请选择架构名称旁边的![三个圆点图标](/help/assets/icons/more.png)，然后选中&#x200B;**[!UICONTROL 刷新架构]**。

您也可以在编辑架构定义时更新该定义。

![](assets/schemas/schema_refresh.png){zoomable="yes"}

## 删除架构 {#schema-delete}

要删除架构，请选择![三个圆点图标](/help/assets/icons/more.png)，然后选择&#x200B;**[!UICONTROL 删除]**。

![](assets/schemas/schema_delete.png){zoomable="yes"}
