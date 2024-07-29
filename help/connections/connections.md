---
audience: end-user
title: 创建和管理与联合数据库的连接
description: 了解如何创建和管理与联合数据库的连接
badge: label="限量发布版" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 5%

---

# 创建连接 {#connections-fdb}

Experience Platform联合受众构成允许客户从第三方数据仓库构建和丰富受众，并将受众导入到Adobe Experience Platform。

要使用联合数据库和Adobe Experience Platform，必须首先建立连接。 此连接是在Adobe Experience Platform用户界面中提供的专用用户界面中设置的，具体如本页所述。

要设置与数据库的连接，请执行以下步骤：

1. 在左边栏上浏览到&#x200B;**[!UICONTROL 联合数据]**&#x200B;部分。

1. 在&#x200B;**[!UICONTROL 联合数据库]**&#x200B;链接中，单击&#x200B;**[!UICONTROL 添加联合数据库]**&#x200B;按钮。

   ![](assets/connections_list.png){zoomable="yes"}

1. 使用数据库的名称和类型设置连接&#x200B;**[!UICONTROL 属性]**。

   ![](assets/connections_name.png){zoomable="yes"}

   选择其类型可让您访问要填写的其他属性。 在此处了解有关[此页面](federated-db.md)中支持的数据库的更多信息。

   ![](assets/connections_details.png){zoomable="yes"}

   配置设置取决于数据库的类型。 浏览下面的链接以访问设置连接所需的详细信息：

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Google Big Query](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. 填写详细信息后，单击&#x200B;**[!UICONTROL 测试连接]**&#x200B;按钮，然后单击&#x200B;**[!UICONTROL 部署函数]**&#x200B;按钮。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;按钮完成连接的创建。

   ![](assets/connections_testdeploy.png){zoomable="yes"}

   提供了联合数据库连接的概述，如下所示：

   ![](assets/connections_overview.png){zoomable="yes"}
