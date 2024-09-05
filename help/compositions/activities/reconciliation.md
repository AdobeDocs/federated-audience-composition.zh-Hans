---
audience: end-user
title: 使用协调活动
description: 了解如何使用协调活动
badge: label="限量发布版" type="Informative"
exl-id: 933c3cba-9120-4a93-a668-866fb65ee197
source-git-commit: 682695357a9bd8f351b5152becd33088fa16f622
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 39%

---

# 协调 {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="协调活动"
>abstract=" **协调** 活动允许您定义数据库中的数据与工作表中的数据之间的链接。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="协调选择字段"
>abstract="协调选择字段"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="协调创建条件"
>abstract="协调创建条件"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="协调生成补集"
>abstract="协调生成补集"

**协调**&#x200B;活动允许您定义数据库中的数据与工作表中的数据（例如从外部系统加载的数据）之间的链接。

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

它允许您将未识别的数据链接到现有资源。 协调操作意味着要加入的数据已在数据库中。 例如，如果要协调显示购买哪个产品、购买时间、购买客户等内容的购买信息，则数据库中必须已存在该产品和客户。

## 配置协调活动 {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="架构"
>abstract="选择要应用于数据的新模式。通过模式（也称为目标选择维度）可以定义目标群体：收件人、应用程序订阅者、运营商、订阅者等。默认情况下会选择构成当前模式。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="协调规则"
>abstract="选择用于删除重复项的协调规则。若要使用属性，请选择&#x200B;**简单属性**&#x200B;选项，然后选择源字段和目标字段。若要使用查询建模器创建您自己的协调条件，请选择&#x200B;**高级协调条件**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="选择目标选择维度"
>abstract="选择要协调的入站数据的模式，也称为目标选择维度。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="保留未协调数据"
>abstract="默认情况下，未调节的数据保留在出站过渡中，并可在工作表中使用。要删除未协调的数据，请停用&#x200B;**保留未协调的数据**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="协调属性"
>abstract="选择要用于协调数据的属性，然后确认。"

按照以下步骤配置&#x200B;**协调**&#x200B;活动：

1. 将&#x200B;**协调**&#x200B;活动添加到合成中。

1. 选择&#x200B;**新架构**。 利用模式（也称为定向维度），可定义定向群体：收件人、应用程序订阅者、操作员、订阅者等。

1. 选择要用于协调的字段。 您可以使用一个或多个协调标准。

   1. 要使用属性协调数据，请选择&#x200B;**简单属性**&#x200B;选项，然后单击&#x200B;**添加规则**&#x200B;按钮。
   1. 为协调选择&#x200B;**Source**&#x200B;和&#x200B;**目标**&#x200B;字段。 **Source**&#x200B;字段。 **目标**&#x200B;字段对应于所选架构的字段。

      当源和目标相等时，将协调数据。 例如，选择&#x200B;**电子邮件**&#x200B;字段，以根据用户档案的电子邮件地址删除重复的用户档案。

      要添加其他协调条件，请单击&#x200B;**添加规则**&#x200B;按钮。 如果指定了多个连接条件，则必须对所有连接条件进行验证，以便将数据链接在一起。

      ![](../assets/reconciliation-rules.png)

   1. 要使用其他属性协调数据，请选择&#x200B;**高级协调条件**&#x200B;选项，然后单击&#x200B;**创建条件**&#x200B;按钮。 然后，您可以使用查询建模器创建自己的协调条件。 [了解如何使用查询建模器](../../query/query-modeler-overview.md)

      ![](../assets/reconciliation-advanced.png)

1. 您可以使用&#x200B;**创建筛选器**&#x200B;按钮筛选要协调的数据。 这使您可以使用查询建模器创建自定义条件。

默认情况下，未协调的数据将保留在叫客过渡中，并可在工作表中供将来使用。 要删除未协调的数据，请停用&#x200B;**保留未协调的数据**&#x200B;选项。

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
