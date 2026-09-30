---
audience: end-user
title: 架构概述
description: 了解如何在Adobe Experience Platform UI中为联合受众组合创建和使用架构。
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 6%
---
# 架构概述 {#schemas}

>[!AVAILABILITY]
>
>新架构体验仅向部分客户提供。 有关更多信息，请联系Adobe客户关怀部门。
>
>如果您无权访问新的架构体验，请阅读[架构概述](./schemas.md)。
>
>要访问架构，您需要以下权限之一：
>
>-**管理联合架构**
>-**查看联合架构**
>
>有关所需权限的更多信息，请阅读[访问控制指南](/help/governance-privacy-security/access-control.md)。

架构是数据库表的表示形式。 它是应用程序中的一个对象，用于定义数据如何与数据库表绑定。

通过创建架构，您可以在Experience Platform联合受众构成中定义表的表示形式：

* 为其提供友好名称和描述，以简化用户的理解
* 根据每个字段的实际使用情况确定其可见性
* 选择其主键，以便根据[数据模型](../data-modelling/models.md#data-model-start)中的需要链接它们之间的架构

>[!CAUTION]
>
>使用同一数据库连接多个沙盒时，必须使用不同的工作架构。

## 创建架构 {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="管理配置"
>abstract="临时空白内容。"

要在联合受众组合中创建架构，请在Experience Platform UI的&#x200B;**[!UICONTROL 数据管理]**&#x200B;部分中选择&#x200B;**[!UICONTROL 架构]**。 在架构UI中，选择&#x200B;**[!UICONTROL 创建架构]**。

![架构UI中的“架构”和“创建架构”按钮均突出显示。](/help/data-modelling/assets/integrated/select-create-schema.png)

出现“创建架构”弹出框后，选择&#x200B;**[!UICONTROL 关系]**，然后选择&#x200B;**[!UICONTROL 发现架构]**&#x200B;和&#x200B;**[!UICONTROL 下一步]**&#x200B;以创建联合受众组合架构。

![在“创建关系架构”弹出框中突出显示了“发现架构”按钮。](/help/data-modelling/assets/integrated/select-discover-schemas.png)

出现&#x200B;**[!UICONTROL Select federated database]**&#x200B;弹出框。 在此弹出窗口中，您可以选择[源数据库](/help/connections/home.md)，然后选择&#x200B;**[!UICONTROL 下一步]**。

![将显示“选择联合数据库”弹出框。](/help/data-modelling/assets/integrated/select-federated-database.png)

## 定义架构 {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="复合密钥"
>abstract="由多个架构列组成的架构键。 标记要用作复合键的列。"

选择联合数据库后，您现在可以定义架构。 出现&#x200B;**[!UICONTROL 添加数据]**&#x200B;屏幕。 在此页上，可以选择&#x200B;**[!UICONTROL 添加表]**&#x200B;以选择要添加到架构中的表。

![“添加表”按钮在“添加数据”屏幕中高亮显示。](/help/data-modelling/assets/integrated/select-add-table.png)

出现&#x200B;**[!UICONTROL 选择表]**&#x200B;弹出框。 在此弹出窗口中，可以选择要用于创建方案的表。

![将显示“选择表”弹出框。](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

每个选定的表都生成一个包含选定列的模式。 对于每个表，可以更改方案的标签、添加说明、重命名字段标签、设置字段标签可见性并选择方案主键。

![选定的表将显示在“添加数据”页中。](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>如果选择&#x200B;**[!UICONTROL 复合键]**，但只选择一个要使用的键，则该键将被视为标准架构主键。

此外，您可以创建一个由多个架构列组成的键。 选择&#x200B;**[!UICONTROL 复合键]**，并标记要用作复合键的键。

![组合键切换和架构均已选中。](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

完成配置后，选择&#x200B;**[!UICONTROL 完成]**&#x200B;以完成架构创建。

## 编辑架构 {#schema-edit}

要编辑架构，请在&#x200B;**架构**&#x200B;页面上选择您之前创建的架构旁边的![省略号图标](/help/assets/icons/more.png)，然后选择&#x200B;**[!UICONTROL 编辑]**。

![已突出显示“编辑架构”按钮。](/help/data-modelling/assets/integrated/edit-schema.png)

在&#x200B;**[!UICONTROL 编辑架构]**&#x200B;窗口中，您可以看到架构编辑器。 有关使用架构编辑器的更多信息，请阅读[架构UI指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/ui/resources/schemas#customize-schema)。

![将显示架构编辑器。](/help/data-modelling/assets/integrated/schema-editor.png)

### 编辑关系 {#relationship-edit}

要编辑架构的关系，请在架构编辑器中选择&#x200B;**[!UICONTROL 查看实体图]**。

![视图实体图按钮突出显示。](/help/data-modelling/assets/integrated/view-entity-diagram.png)

此时将显示实体图页面。 在此页上，可以创建链接以建立方案之间的关系。

![显示实体图。](/help/data-modelling/assets/integrated/entity-diagram.png)

有关创建链接的更多信息，请阅读[数据模型概述](/help/data-modelling/models.md#data-model-links)的“画布视图”选项卡。

## 在架构中预览数据 {#schema-preview}

要预览架构所代表的表中的数据，请转到&#x200B;**[!UICONTROL 数据集]**&#x200B;部分，然后选择&#x200B;**[!UICONTROL 浏览]**。

![数据集和“浏览”按钮突出显示。](/help/data-modelling/assets/integrated/datasets-browse.png)

选择![三个点](/help/assets/icons/more.png)，然后选择&#x200B;**[!UICONTROL 预览数据集]**&#x200B;以查看架构中数据的预览。

![预览数据集按钮突出显示。](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## 刷新架构 {#schema-refresh}

可以更新、添加或删除联合数据库中的表。 在这种情况下，您必须刷新Adobe Experience Platform中的架构以符合最新更改。 要刷新架构，请选择&#x200B;**[!UICONTROL 更多]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 管理配置]**。

![“管理配置”按钮突出显示。](/help/data-modelling/assets/integrated/manage-configuration.png)

出现&#x200B;**[!UICONTROL 编辑配置]**&#x200B;弹出框。 选择&#x200B;**[!UICONTROL 刷新]**&#x200B;以刷新架构。

![刷新架构按钮突出显示。](/help/data-modelling/assets/integrated/refresh-schema.png)

## 删除架构 {#schema-delete}

要删除架构编辑器中的架构，请选择&#x200B;**[!UICONTROL 更多]**，然后选择&#x200B;**[!UICONTROL 删除]**。

![已突出显示“删除架构”按钮。](/help/data-modelling/assets/integrated/delete-schema.png)
