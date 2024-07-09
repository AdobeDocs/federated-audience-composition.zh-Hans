---
audience: end-user
title: 使用查询建模器构建您的第一个查询
description: 了解如何在查询建模器中构建您的第一个查询
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '2066'
ht-degree: 10%

---

# 生成您的第一个查询 {#build-query}

要开始构建查询，请从您选择的位置访问查询建模器，具体取决于您要执行的操作。 此时将打开查询建模器，并显示一个空白画布。 单击 **+** 按钮以配置查询的第一个节点。

可添加两种类型的元素：

* **筛选组件** （自定义条件，选择受众）允许您构建自己的规则，或选择受众以优化查询。 它们会添加到查询的开头和点状过渡中。 [了解如何使用筛选组件](#filtering)

  示例： *订阅“体育”新闻稿的收件人*. *居住在纽约的收件人*， *居住在旧金山的收件人*

  ![](assets/query-add-component.png){zoomable="yes"}

* **组操作员** (AND、OR、EXCEPT)允许您将图中的过滤组件组合在一起。 它们会添加到现有过渡中，然后是筛选组件。 [了解如何使用操作员](#filtering)

  示例： *订阅“体育”新闻稿的收件人&#x200B;**和**住在纽约的人&#x200B;**或者**旧金山*.

  ![](assets/query-add-operator.png){zoomable="yes"}

## 添加筛选组件 {#filtering}

通过筛选组件，您可以使用以下内容优化查询：

* **[自定义完成情况](#custom-condition)**：通过使用数据库和高级表达式的属性构建您自己的条件来筛选查询。
* **[受众](#audiences)**：使用现有受众筛选查询。

### 配置自定义条件 {#custom-condition}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_customcondition"
>title="自定义条件"
>abstract="自定义条件是筛选组件，它们使您可通过从数据库和高级表达式构建您自己的带属性条件而筛选您的查询。"

要使用自定义条件筛选查询，请执行以下步骤：

1. 单击 **+** 按钮，然后选择 **[!UICONTROL 自定义完成情况]**. 自定义条件属性窗格将在右侧打开。

1. 在 **属性** 字段，从数据库中选择要用于创建条件的属性。 属性列表包含数据库中的所有属性，包括链接表中的属性。

   ![](assets/query-custom-condition-fields.png){zoomable="yes"}

   >[!NOTE]
   >
   >此 **编辑表达式** 按钮允许您利用表达式编辑器，使用数据库和帮助程序函数中的字段手动定义表达式。 [了解如何编辑表达式](expression-editor.md)

1. 从下拉列表中选择要应用的运算符。 可以使用各种运算符。 请注意，下拉列表中可用的运算符取决于属性的数据类型。

   +++可用运算符列表

   | 操作员 | 目的 | 示例 |
   |  ---  |  ---  |  ---  |
   | 等于 | 返回与在第二个“值”列中输入的数据相同的结果。 | 姓氏(@lastName)等于“Jones”，将仅返回姓氏为Jones的收件人。 |
   | 不等于 | 返回与输入值不相同的所有值。 | 等于“英语”的语言(@language) |
   | 大于 | 返回大于输入值的值。 | 年龄(@age)大于50</strong>，将返回所有大于“50”的值，如“51”、“52”等。 |
   | 小于 | 返回小于输入值的值。 | 创建日期(@created)早于“DaysAgo(100)”</strong>，将返回之前100天创建的所有收件人。 |
   | 大于或等于 | 返回所有等于或大于输入值的值。 | 年龄(@age)大于或等于“30”</strong>，将返回所有30岁或以上的收件人。 |
   | 小于或等于 | 返回等于或小于输入值的所有值。 | 年龄(@age)小于或等于“60”</strong>，将返回所有60岁或以下的收件人。 |
   | 包含在 | 返回指定值中包含的结果。 这些值必须以逗号分隔。 | 出生日期(@birthDate)包含在“12/10/1979,12/10/1984”中，将返回这些日期之间出生的收件人。 |
   | Not in | 其工作方式与包含在运算符中类似。 在本例中，我们要根据输入的值排除收件人。 | 出生日期(@birthDate)未列入`12/10/1979,12/10/1984`。 与上一个示例不同，不会返回这些日期内出生的收件人。 |
   | 为空 | 在这种情况下，我们要查找的结果与第二个“值”列中的空值匹配。 | Mobile (@mobilePhone)为空，则会返回所有没有手机号码的收件人。 |
   | 不为空 | 与Is empty运算符相反。 无需在第二个“值”列中输入数据。 | 电子邮件(@email)不为空。 |
   | 开始于 | 返回以输入值开头的结果。 | 帐户# (@account)以“32010”开头。 |
   | Does not start with | 返回不以输入值开头的结果 | 帐户# (@account)不以“20”开头 |
   | Contains | 返回至少包含输入值的结果。 | 电子邮件域(@domain)包含“mail”</strong>，将返回包含“mail”的所有域名。 因此，也会返回“gmail.com”域。 |
   | 不包含 | 返回不包含输入值的结果。 | 电子邮件域(@domain)不包含“vo”</strong>. 在这种情况下，将不返回包含“vo”的域名。 “voila.fr”域名将不会显示在结果中。 |
   | 喜欢 | Like与Contains运算符非常相似。 利用该运算符，可在值中插入%通配符。 | 姓氏(@lastName)，如“Jon%s”。 在本例中，如果操作员忘记了“n”和“s”之间缺少的字母，则使用通配符作为“绝招”来查找名称“Jones”。 |
   | 不相似 | Like与Contains运算符非常相似。 利用该运算符，可在值中插入%通配符。 | 姓氏(@lastName)不像“Smi%h”。 在此，将不会返回姓氏为“Smi%h”的收件人。 |

+++

1. 在 **值** 字段，定义预期值。 您还可以利用表达式编辑器，使用数据库和帮助程序函数中的字段手动定义表达式。 要执行此操作，请单击 **编辑表达式** 按钮。 [了解如何编辑表达式](expression-editor.md)

   *返回所有年龄为21岁或以上的用户档案的查询示例：*

   ![](assets/query-custom-condition.png){zoomable="yes"}

#### 链接表（1-1和1-N链接）上的自定义条件{#links}

自定义条件允许您查询链接到规则当前使用的表的表。 这包括具有1-1基数链接的表，或集合表（1-N链接）。

对于 **1-1链接**，导航到链接的表，选择所需的属性并定义预期值。

您也可以直接选择表格链接 **值** 选取并确认。 在这种情况下，需要使用专用选取器来选择对所选表可用的值，如下面的示例所示。

+++查询示例

在本例中，查询的目标品牌标签为“正在运行”。

1. 在 **品牌** 表并选择 **标签** 属性。

   ![](assets/1-1-attribute.png){zoomable="yes"}{width="85%" align="center"}

1. 定义属性的预期值。

   ![](assets/1-1-table.png){zoomable="yes"}{width="85%" align="center"}

以下是一个直接选择表链接的查询示例。 必须从专用选取器中选择此表的可用值。

![](assets/1-1-table-direct.png){zoomable="yes"}{width="85%" align="center"}

+++

对于 **1-N链接**，您可以定义子条件来优化查询，如下面的示例所示。

+++查询示例

在本例中，查询将定向购买与BrewMaster产品相关的收件人，购买总额至少为100$。

1. 选择 **购买** 表格并进行确认。

   ![](assets/1-N-collection.png){zoomable="yes"}{width="50%" align="center"}

1. 将添加叫客过渡，从而允许您创建子条件。

   ![](assets/1-n-subcondition.png){zoomable="yes"}{width="85%" align="center"}

1. 选择 **价格** 1000美元或以上的属性和目标购买

   ![](assets/1-n-price.png){zoomable="yes"}{width="85%" align="center"}

1. 根据您的需要添加子条件。 在此，我们添加了条件来定向购买BrewMaster产品的用户档案。

   ![](assets/custom-condition-1-N.png){zoomable="yes"}{width="85%" align="center"}

+++

#### 使用聚合数据 {#aggregate}

自定义条件允许您执行聚合操作。 要实现此目的，需要直接从集合表中选择属性：

1. 在所需的集合表中导航，并选择要对其执行聚合操作的属性。

   ![](assets/aggregate-attribute.png){zoomable="yes"}{width="85%" align="center"}

1. 在属性窗格中，切换 **聚合数据** 选项并选择所需的聚合函数。

   ![](assets/aggregate.png){zoomable="yes"}{width="85%" align="center"}

### 选择受众 {#audiences}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_selectaudience"
>title="选择受众"
>abstract="通过使用&#x200B;**选择受众**&#x200B;选项，您可以选择想要用来过滤查询的受众。"

要使用现有受众筛选查询，请执行以下步骤：

1. 单击 **+** 按钮，然后选择 **[!UICONTROL 选择受众]**.

1. 此 **选择受众** “属性”窗格将在右侧打开。 选择要用于筛选查询的受众。

   *查询示例返回属于“节日观看者”受众的所有用户档案：*

   ![](assets/query-audience.png){zoomable="yes"}

### 使用预定义过滤器 {#predefined-filters}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_predefinedfilter"
>title="预定义过滤器"
>abstract="通过使用&#x200B;**预定义过滤器**&#x200B;选项，您可以从自定义过滤器列表或收藏夹中选择一个预定义过滤器。"

要使用预定义过滤器过滤查询，请执行以下步骤：

1. 单击 **+** 按钮，然后选择 **[!UICONTROL 预定义过滤器]**.

1. 此 **预定义过滤器** “属性”窗格将在右侧打开。 从自定义筛选器列表或收藏夹中选择一个预定义筛选器。

   *返回与“不活跃客户”预定义过滤器对应的所有用户档案的查询示例：*

   ![](assets/query-predefined-filter.png){zoomable="yes"}

### 复制粘贴组件 {#copy}

查询建模器允许您复制一个或多个筛选组件并将它们粘贴到过渡的末尾。 可以在当前查询画布中或实例中的任何画布中执行此操作。

>[!NOTE]
>
>只要您在实例中工作，复制的选定内容就会保留。 如果您注销并重新登录，则您的选择将不再可用于粘贴。

要复制并粘贴筛选组件，请执行以下步骤：

1. 在查询画布中单击要复制的筛选组件，以选择该组件。 要选择多个组件，请使用位于画布右上角的工具栏中提供的多选工具。

1. 单击 **[!UICONTROL 复制]** 按钮时，该按钮位于组件的“属性”窗格中，或者位于屏幕底部的蓝带中（如果已选择多个组件）。

   | 复制单个组件 | 复制多个组件 |
   |  ---  |  ---  |
   | ![](assets/copy-single-component.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/copy-multiple-components.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

1. 要粘贴组件，请单击所需过渡末尾的+按钮，然后选择 **粘贴n项**.

   ![](assets/copy-paste.png){zoomable="yes"}

## 将过滤组件与运算符相结合 {#operators}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_group"
>title="组"
>abstract="在此窗格中，您可以更改用于链接过滤条件的运算符。"

每次将新的筛选组件添加到查询时，它都会通过 **和** 运算符。 这意味着来自两个过滤组件的结果将组合在一起。

在此示例中，我们在第二个过渡中添加了新的受众类型筛选组件。 该组件通过以下方式链接到预定义过滤器条件： **和** 运算符，这意味着查询结果包含受“Madridians”预定义过滤器定向的且属于“Discount hunter”受众的收件人。

![](assets/query-operator.png){zoomable="yes"}

要更改用于将筛选条件链接在一起的运算符，请单击它并在中选择所需的运算符 **组** 在右侧打开的窗格。

可用的运算符包括：

* **AND（交集）**：组合与叫客过渡中所有筛选组件匹配的结果。
* **OR（并集）**：包括与叫客过渡中的至少一个筛选组件匹配的结果。
* **排除（排除）**：排除与叫客过渡中所有筛选组件匹配的结果。

![](assets/query-operator-change.png){zoomable="yes"}

此外，通过单击 **+** 按钮进行转换。 这允许您在此特定位置添加运算符，以将多个组件分组在一起并细化查询。

在下面的示例中，我们创建了一个中间组，以包含来自“要奖励的VIP”或“超级VIP”受众的结果。

![](assets/query-intermediate-group.png){zoomable="yes"}

## 检查并验证您的查询

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_ruleproperties"
>title="规则属性"
>abstract="在画布中生成查询后，即可使用位于右侧的&#x200B;**规则属性**&#x200B;窗格检查该查询。<br/>通过此窗格，可显示所得的数据、检索该查询的某个 SQL 代码版本以及检查目标记录的数量。<br/>使用&#x200B;**选择或保存过滤器**&#x200B;按钮将您的查询另存为预定义的过滤器，或将画布内容替换为某个现有的过滤器。"

在画布中构建查询后，您可以使用 **规则属性** 窗格位于右侧。 构建查询以创建受众时，显示此窗格。 可用的操作包括：

* **查看结果：** 显示查询生成的数据。
* **代码视图**：显示SQL中查询的基于代码的版本。
* **计算**：更新和显示您的查询所定向的记录数。
* **选择或保存筛选器**：选择要在画布中使用的现有预定义过滤器，或将查询另存为预定义过滤器以供将来重用。

  >[!IMPORTANT]
  >
  >从规则属性窗格中选择一个预定义过滤器，将画布中构建的查询替换为所选过滤器。

查询就绪后，单击 **[!UICONTROL 确认]** 按钮进行保存。

您可以随时通过打开查询来修改查询。 请记住，打开现有查询时，它以简化视图显示，不显示  **+** 按钮。 要向查询添加新元素，请在画布上选择一个组件或运算符以显示 **+** 按钮。

![](assets/edit-audience.png){zoomable="yes"}
