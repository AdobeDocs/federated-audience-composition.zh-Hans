---
audience: end-user
title: 使用扩充活动
description: 了解如何使用扩充活动
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 40%

---


# 扩充 {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="“扩充”活动"
>abstract="通过&#x200B;**扩充**&#x200B;活动，可利用来自数据库的其他信息增强目标数据。它通常用在分段活动后的构成中。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="“扩充”活动"
>abstract="将扩充数据添加到构成后，即可在之后添加的活动中使用 **扩充** 活动根据用户档案的行为、偏好和选择将其划分为不同的组。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="链接定义"
>abstract="在工作表数据和联合数据库之间创建链接。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="扩充协调"
>abstract="设置协调参数。"

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="扩充数据"
>abstract="选择用于丰富合成的数据。 可选择两种类型的扩充数据：目标维度中的单个扩充属性或收藏集链接（即在各表之间具有 1-N 基数的链接）。"

此 **扩充** 利用活动，可使用联合数据库中的其他信息来增强目标数据。 它通常用在分段活动后的合成中。

扩充数据可来自：

* **从同一工作表** 作为合成中的目标：

  *定位一组客户并将“出生日期”字段添加到当前工作表*.

* **另一个工作表**：

  *定位一组客户，并添加“采购”表中的“金额”和“产品类型”字段*。

将扩充数据添加到构成后，即可在之后添加的活动中使用 **扩充** 活动根据客户的行为、偏好和选择将客户划分为不同的组。

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## 添加扩充活动 {#enrichment-configuration}

请按照以下步骤操作，配置&#x200B;**扩充**&#x200B;活动：

1. 添加活动，例如&#x200B;**生成受众**&#x200B;和&#x200B;**合并**&#x200B;活动。
1. 添加&#x200B;**扩充**&#x200B;活动。
1. 如果在构成中配置了多个过渡，则可以使用 **[!UICONTROL 主集]** 字段来定义哪个过渡应用作主集以扩充数据。

## 添加扩充数据 {#enrichment-add}

1. 单击 **添加扩充数据** 并选择要用于扩充数据的属性。

   您可以选择两种类型的扩充数据：从目标维中选择单个扩充属性，或者选择收集链接。 以下示例详细介绍了每种类型：

   * [单个扩充属性](#single-attribute)
   * [收藏集链接](#collection-link)

<!--
>[!NOTE]
>
>The **Edit expression button** in the attribute selection screen allows you to build advanced expressions to select the attribute. [Learn how to work with the expression editor](../../query/expression-editor.md)-->

## 在表之间创建链接 {#create-links}

此 **[!UICONTROL 链接定义]** 部分允许您在工作表数据和数据库之间创建链接。 例如，如果您从包含收件人的帐号、国家/地区和电子邮件的文件中加载数据，则必须创建一个指向该国家/地区表的链接，以便在其配置文件中更新此信息。

有多种类型的链接可用：

* **[!UICONTROL 1基数简单链接]**：主集中的每个记录都可以与链接数据中的一个记录（且只能与一个记录关联）。
* **[!UICONTROL 0或1基数简单链接]**：主集中的每个记录可以与链接数据中的0或1个记录关联，但不能与多个记录关联。
* **[!UICONTROL N基数收藏集链接]**：主集中的每个记录可以与来自链接数据的0、1个或多个(N)记录关联。

要创建链接，请执行以下步骤：

1. 在 **[!UICONTROL 链接定义]** 部分，单击 **[!UICONTROL 添加链接]** 按钮。

1. 在 **关系类型** 从下拉列表中，选择要创建的链接类型。

1. 确定要将主集链接到的目标：

   * 要链接数据库中的现有表，请选择 **[!UICONTROL 数据库模式]** 并从中选择所需的表 **[!UICONTROL 目标架构]** 字段。
   * 要链接到输入过渡中的数据，请选择 **临时架构** 并选择要使用其数据的过渡。

1. 定义协调条件，以将主集的数据与链接架构进行匹配。 有两种类型的连接可用：

   * **简单联接**：选择特定属性以匹配两个架构中的数据。 单击 **添加联接** 并选择 **Source** 和 **目标** 要用作协调条件的属性。
   * **高级联接**：使用高级条件创建连接。 单击 **添加联接** 然后单击 **创建条件** 按钮以打开查询建模器。

有关使用链接的构成示例，请参阅 [示例](#link-example) 部分。

## 示例 {#example}

### 单个扩充属性 {#single-attribute}

我们在此处只添加单个扩充属性，例如出生日期。执行以下步骤：

1. 在&#x200B;**属性**&#x200B;字段内单击。
1. 从定位维度中选择一个简单的字段，在我们的示例中是出生日期。
1. 单击&#x200B;**确认**。

### 收藏集链接 {#collection-link}

在这个更复杂的用例中，我们将选择一个收藏集链接，它是表之间具有 1 对多基数的链接。让我们检索最近三笔低于 100 美元的购买。为此，您需要定义：

* 扩充属性：**总金额**&#x200B;字段
* 要检索的行数：3
* 筛选条件：筛选掉大于 100 美元的项目
* 排序：**订购日期**&#x200B;字段的降序排序。

#### 添加属性 {#add-attribute}

您可以在此处选择用作扩充数据的收藏集链接。

1. 在&#x200B;**属性**&#x200B;字段内单击。
1. 单击&#x200B;**显示高级属性**。
1. 从&#x200B;**购买**&#x200B;表中选择&#x200B;**总金额**&#x200B;字段。

#### 定义收藏集设置{#collection-settings}

然后，定义数据的收集方式以及要检索的记录数。

1. 在&#x200B;**选择数据收集方式**&#x200B;下拉列表中选择&#x200B;**收集数据**。
1. 在&#x200B;**要检索的行（要创建的列）**&#x200B;字段中键入“3”。

例如，如果您想要获取客户的平均购买金额，请改选&#x200B;**汇总数据**，然后从&#x200B;**汇总函数**&#x200B;中选择&#x200B;**平均**。

#### 定义筛选条件{#collection-filters}

我们在此处定义扩充属性的最大值。我们将筛选掉大于100$的项目。 <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. 单击&#x200B;**编辑筛选条件**。
1. 添加以下两个筛选条件：**总金额**&#x200B;存在且&#x200B;**总金额**&#x200B;小于 100。第一个筛选条件筛选掉 NULL 值，因为它们将显示为最大值。
1. 单击&#x200B;**确认**。

#### 定义排序{#collection-sorting}

我们现在需要应用排序来检索这三个&#x200B;**最新**&#x200B;的购买。

1. 激活&#x200B;**启用排序**&#x200B;选项。
1. 在&#x200B;**属性**&#x200B;字段内单击。
1. 选择&#x200B;**订购日期**&#x200B;字段。
1. 单击&#x200B;**确认**。
1. 从&#x200B;**排序**&#x200B;下拉列表中选择&#x200B;**降序**。


### 使用链接数据进行扩充 {#link-example}

下方的示例显示了配置为在两个过渡之间创建链接的合成。 第一转变使用查询活动定位用户档案数据，而第二转变包括存储到通过加载文件活动加载的文件中的购买数据。

* 第一个 **扩充** 活动链接我们的主集(来自 **查询** 活动)中的架构 **加载文件** 活动。 这样，我们就可以将查询所定向的每个用户档案与相应的购买数据相匹配。
* 秒 **扩充** 添加了活动，以便使用来自的购买数据扩充构成表中的数据 **加载文件** 活动。 这样，我们便可以在进一步的活动中使用这些数据，例如，将发送给客户的消息与他们的购买信息个性化。





<!--

Add other fields
use it in delivery


cardinality between the tables (1-N)
1. select attribute to use as enrichment data

    display advanced fields option
    i button

    note: attributes from the target dimension

1. Select how the data is collected
1. number of records to retrieve if want to retrieve a collection of multiple records
1. Apply filters and build rule

    select an existing filter
    save the filter for reuse
    view results of the filter visually or in code view

1. sort records using an attribute

leverage enrichment data in campaign

where we can use the enrichment data: personalize email, other use cases?

## Example

-->
