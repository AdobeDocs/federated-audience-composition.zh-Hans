---
audience: end-user
title: 使用扩充活动
description: 了解如何使用扩充活动
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 52%

---


# 扩充 {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="“扩充”活动"
>abstract="通过&#x200B;**扩充**&#x200B;活动，可利用来自数据库的其他信息增强目标数据。通常在分段活动之后的构成中使用它。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="“扩充”活动"
>abstract="一旦将扩充数据添加到构成中，它就可以在 **扩充** 活动之后添加的活动中使用，以根据行为、偏好和选择将轮廓划分为不同的组。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="链接定义"
>abstract="在表数据和联合数据库之间创建链接。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="扩充协调"
>abstract="设置协调参数"

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="扩充数据"
>abstract="选择用于扩充您的构成的数据。可选择两种类型的扩充数据：模式（也称为目标选择维度）中的单个扩充属性或收藏集链接（即在各表之间具有 1-N 基数的链接）。"

利用&#x200B;**扩充**&#x200B;活动，可使用联合数据库中的附加信息增强目标数据。 它通常用在分段活动后的合成中。

扩充数据可来自：

* **来自与组合中目标工作表相同的工作表**：

  *定位一组客户并将“出生日期”字段添加到当前工作表*。

* **另一个工作表**：

  *定位一组客户，并添加“采购”表中的“金额”和“产品类型”字段*。

将扩充数据添加到组合后，即可在在&#x200B;**扩充**&#x200B;活动之后添加的活动中使用，以根据客户的行为、偏好和选择将客户划分到不同的组中。

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## 配置扩充活动 {#enrichment-configuration}

请按照以下步骤操作，配置&#x200B;**扩充**&#x200B;活动：

1. 添加活动，例如&#x200B;**生成受众**&#x200B;和&#x200B;**合并**&#x200B;活动。
1. 添加&#x200B;**扩充**&#x200B;活动。

   ![](../assets/enrichment.png)

1. 如果您的构成中配置了多个过渡，则可以使用&#x200B;**[!UICONTROL 主集]**&#x200B;字段定义应将哪个过渡用作主集以扩充数据。

1. 单击&#x200B;**添加扩充数据**&#x200B;并选择要用于扩充数据的属性。

   ![](../assets/enrichment-add.png)

   >[!NOTE]
   >
   >属性选择屏幕中的&#x200B;**编辑表达式按钮**&#x200B;允许您构建高级表达式以选择属性。

<!--PAS VU SUR INSTANCE: You can select two types of enrichment data: a single enrichment attribute from the target dimension, or a collection link. Each of these types is detailed in the examples below:

    * [Single enrichment attribute](#single-attribute)
    * [Collection lnk](#collection-link)-->

## 示例 {#example}

### 单个扩充属性 {#single-attribute}

我们在此处只添加单个扩充属性，例如出生日期。执行以下步骤：

1. 在&#x200B;**属性**&#x200B;字段内单击。
1. 从架构中选择一个简单字段，也称为定向维度，在本例中是出生日期。
1. 单击&#x200B;**确认**。

<!--### Collection link {#collection-link}

In this more complex use case, we will select a collection link which is a link with a 1-N cardinality between tables. Let's retrieve the three latest purchases that are less than 100$. For this you need to define:

* an enrichment attribute: the **Total amount** field
* the number of lines to retrieve: 3
* a filter: filter out items that are greater than 100$
* a sorting: descendant sorting on the **Order date** field. 

#### Add the attribute {#add-attribute}

This is where you select the collection link to use as enrichment data.

1. Click inside the **Attribute** field.
1. Click **Display advanced attributes**.
1. Select the **Total amount** field from the **Purchases** table. 

#### Define the collection settings{#collection-settings}

Then, define how the data is collected and the number of records to retrieve.

1. Select **Collect data** in the **Select how the data is collected** drop-down.
1. Type "3" in the **Lines to retrieve (Columns to create)** field. 

If you want, for example, to get the average amount of purchases for a customer, select **Aggregated data** instead, and select **Average** in the **Aggregate function** drop-down.

#### Define the filters{#collection-filters}

Here, we define the maximum value for the enrichment attribute. We filter out items that are greater than 100$. [Learn how to work with the query modeler](../../query/query-modeler-overview.md)

1. Click **Edit filters**.
1. Add the two following filters: **Total amount** exists AND **Total amount** is less than 100. The first one filters NULL values as they would appear as the greatest value.
1. Click **Confirm**.

#### Define the sorting{#collection-sorting}

We now need to apply sorting in order to retrieve the three **latest** purchases.

1. Activate the **Enable sorting** option.
1. Click inside the **Attribute** field.
1. Select the **Order date** field.
1. Click **Confirm**. 
1. Select **Descending** from the **Sort** drop-down.-->
