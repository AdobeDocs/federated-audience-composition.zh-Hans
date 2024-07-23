---
audience: end-user
title: 创建和管理与联合数据库的连接
description: 了解如何创建和管理与联合数据库的连接
badge: label="限量发布版" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# 创建连接 {#connections-fdb}

直接在AEP中使用联合数据库意味着与其建立连接。

要设置与数据库的连接，请转到&#x200B;**[!UICONTROL 联合数据]**&#x200B;部分，在&#x200B;**[!UICONTROL 联合数据库]**&#x200B;链接中，单击&#x200B;**[!UICONTROL 添加联合数据库]**&#x200B;按钮。

![](assets/connections_list.png){zoomable="yes"}

您将访问连接&#x200B;**[!UICONTROL 属性]**&#x200B;的窗口，其中包含数据库的名称和类型。

![](assets/connections_name.png){zoomable="yes"}

选择其类型将允许您访问要填写的其他属性。 [在此处了解有关支持的数据库的更多信息](federated-db.md)。

![](assets/connections_details.png){zoomable="yes"}

根据数据库的类型，在下面的链接中了解设置连接所需的信息：

* [Amazon Redshift](federated-db.md#amazon-redshift)
* [azure synapse](federated-db.md#azure-synapse-redshift)
* [Google Big Query](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

填写详细信息后，单击&#x200B;**[!UICONTROL 测试连接]**&#x200B;按钮，然后单击&#x200B;**[!UICONTROL 部署函数]**按钮。
单击**[!UICONTROL 保存]**&#x200B;按钮完成连接的创建。

![](assets/connections_testdeploy.png){zoomable="yes"}

您将大致了解联合数据库连接，如下所示：

![](assets/connections_overview.png){zoomable="yes"}
