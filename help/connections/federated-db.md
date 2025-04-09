---
audience: end-user
title: 配置联合数据库
description: 了解如何配置联合数据库
exl-id: b8c0589d-4150-40da-ac79-d53cced236e8
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '2120'
ht-degree: 96%

---

# 配置联合数据库 {#federated-db}

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="联合数据库"
>abstract="此屏幕列出了与联合数据库的现有连接。要创建新连接，请单击&#x200B;**[!UICONTROL 添加联合数据库]**&#x200B;按钮。"

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="联合数据库属性"
>abstract="输入新的联合数据库的名称，并选择其类型。"

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="联合数据库详细信息"
>abstract="输入设置以连接到新的联合数据库。使用&#x200B;**[!UICONTROL 测试连接]**&#x200B;按钮验证您的配置。"

Experience Platform 联合受众构成允许客户从第三方数据仓库构建和扩充受众，并将受众导入到 Adobe Experience Platform 中。

了解如何在[此页面](connections.md)上创建、配置、测试和保存与外部数据库的连接。 您可以在下面找到受支持的数据库列表以及每个数据库需要配置的详细设置。

## 支持的数据库 {#supported-db}

通过联合受众构成，您可以连接到以下数据库。每个数据库的配置详细说明如下。

* [Amazon Redshift](#amazon-redshift)
* [Azure Synapse Analytics](#azure-synapse)
* [Google Big Query](#google-big-query)
* [Snowflake](#snowflake)
* [Vertica Analytics](#vertica-analytics)
* [数据块](#databricks)
* [Microsoft Fabric](#microsoft-fabric)

## Amazon Redshift {#amazon-redshift}

>[!AVAILABILITY]
>
>仅支持 Amazon Redshift AWS、Amazon Redshift Spectrum 和 Amazon Redshift Serverless。

使用联合数据库处理存储在外部数据库中的信息。按照以下步骤配置对 Amazon Redshift 的访问权限。

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 联合数据库]**。

1. 单击&#x200B;**[!UICONTROL 添加联合数据库]**。

   ![](assets/federated_database_1.png)

1. 为您的联合数据库输入一个&#x200B;**[!UICONTROL 名称]**。

1. 从&#x200B;**[!UICONTROL 类型]**&#x200B;下拉菜单中，选择 Amazon Redshift。

   ![](assets/federated_database_6.png)

1. 配置 Amazon Redshift 身份验证设置：

   * **[!UICONTROL 服务器]**：添加 DNS 的名称。

   * **[!UICONTROL 帐户]**：添加用户名。

   * **[!UICONTROL 密码]**：添加账号密码。

   * **[!UICONTROL 数据库]**：数据库的名称（如果未在 DSN 中指定）。如果已在 DSN 中指定，则可以将其留空

   * **[!UICONTROL 工作架构]**：用于工作表的数据库架构的名称。请参阅[Amazon文档](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}以了解详情

     >[!NOTE]
     >
     >您可以使用数据库中的任何架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限即可。
     >
     >当使用同一个数据库连接多个沙盒时，必须使用&#x200B;**不同的工作架构**。

1. 选择&#x200B;**[!UICONTROL 测试连接]**&#x200B;选项来验证您的配置。

1. 单击&#x200B;**[!UICONTROL 部署功能]**&#x200B;按钮来创建函数。

1. 配置完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;创建您的联合数据库。

## Azure Synapse Analytics {#azure-synapse}

使用联合数据库处理存储在外部数据库中的信息。按照以下步骤配置对 Azure Synapse Analytics 的访问权限。

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 联合数据库]**。

1. 单击&#x200B;**[!UICONTROL 添加联合数据库]**。

   ![](assets/federated_database_1.png)

1. 为您的联合数据库输入一个&#x200B;**[!UICONTROL 名称]**。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;下拉菜单中选择 Azure Synapse Analytics。

   ![](assets/federated_database_4.png)

1. 配置 Azure Synapse Analytics 身份验证设置：

   * **[!UICONTROL 服务器]**：输入 Azure Synapse 服务器的 URL。

   * **[!UICONTROL 帐户]**：输入用户名。

   * **[!UICONTROL 密码]**：输入账号密码。

   * **[!UICONTROL 数据库]** （可选）：如果 DSN 中未指定，请输入数据库的名称。

   * **[!UICONTROL 选项]**：该连接器支持下表中详述的选项。

1. 选择&#x200B;**[!UICONTROL 测试连接]**&#x200B;选项来验证您的配置。

1. 单击&#x200B;**[!UICONTROL 部署功能]**&#x200B;按钮来创建函数。

1. 配置完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;创建您的联合数据库。

| 选项 | 描述 |
|---|---|
| 身份验证 | 连接器支持的身份验证类型。当前支持的值：ActiveDirectoryMSI。有关详细信息，请参阅[Microsoft SQL文档](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}（连接字符串n°8示例） |

## Google Big Query {#google-big-query}

使用联合数据库处理存储在外部数据库中的信息。按照以下步骤配置对 Google Big Query 的访问权限。

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 联合数据库]**。

1. 单击&#x200B;**[!UICONTROL 添加联合数据库]**。

   ![](assets/federated_database_1.png)

1. 为您的联合数据库输入一个&#x200B;**[!UICONTROL 名称]**。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;下拉菜单中，选择 Google Big Query。

   ![](assets/federated_database_3.png)

1. 配置 Google Big Query 身份验证设置：

   * **[!UICONTROL 服务帐户]**：输入您的电子邮件&#x200B;**[!UICONTROL 服务帐户]**。有关更多信息，请参阅 [Google Cloud 文档](https://cloud.google.com/iam/docs/creating-managing-service-accounts){target="_blank"}。

   * **[!UICONTROL 项目]**：输入您的&#x200B;**[!UICONTROL 项目]** 的 ID。有关更多信息，请参阅 [Google Cloud 文档](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}。

   * **[!UICONTROL 数据集]**：输入您的&#x200B;**[!UICONTROL 数据集]**&#x200B;的名称。有关更多信息，请参阅 [Google Cloud 文档](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}。

   * **[!UICONTROL 密钥文件路径]**：将您的密钥文件上传到服务器。仅接受 .json 文件。

   * **[!UICONTROL 选项]**：该连接器支持下表中详述的选项。

1. 选择&#x200B;**[!UICONTROL 测试连接]**&#x200B;选项来验证您的配置。

1. 单击&#x200B;**[!UICONTROL 部署功能]**&#x200B;按钮来创建函数。

1. 配置完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;创建您的联合数据库。

| 选项 | 描述 |
|---|---|
| ProxyType | 用于通过 ODBC 和 SDK 连接器连接到 BigQuery 的代理类型。</br>目前支持 HTTP（默认）、http_no_tunnel、socks4 和 socks5。 |
| ProxyHost | 可以访问代理的主机名或 IP 地址。 |
| ProxyPort | 代理运行的端口号，例如 8080 |
| ProxyUid | 用于经过身份验证的代理的用户名 |
| ProxyPwd | ProxyUid 密码 |
| bqpath | 请注意，这仅适用于批量加载工具 (Cloud SDK)。</br> 为了避免使用 PATH 变量或者如果必须将 google-cloud-sdk 目录移动到其他位置，您可以使用此选项指定服务器上 cloud sdk bin 目录的确切路径。 |
| GCloudConfigName | 请注意，这适用于从版本 7.3.4 开始的版本，并且仅适用于批量加载工具 (Cloud SDK)。</br> Google Cloud SDK 使用配置将数据加载到 BigQuery 表中。名为 `accfda` 的配置存储加载数据的参数。但是，此选项允许用户为配置指定不同的名称。 |
| GCloudDefaultConfigName | 请注意，这适用于从版本 7.3.4 开始的版本，并且仅适用于批量加载工具 (Cloud SDK)。</br> 如果不先将活动标记转移到新配置，则无法删除活动的 Google Cloud SDK 配置。此临时配置对于重新创建用于加载数据的主要配置是必要的。临时配置的默认名称是 `default`，如果需要，该名称可以进行更改。 |
| GCloudRecreateConfig | 请注意，这适用于从版本 7.3.4 开始的版本，并且仅适用于批量加载工具 (Cloud SDK)。</br> 当设置为 `false` 时，批量加载机制不会尝试重新创建、删除或修改 Google Cloud SDK 配置。相反，它会使用机器上现有的配置继续加载数据。当其他操作依赖于 Google Cloud SDK 配置时，此功能很有价值。</br> 如果用户在没有正确配置的情况下启用此引擎选项，则批量加载机制会发出警告消息： `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`。为了防止进一步出现错误，它将会恢复使用默认的 ODBC 数组插入批量加载机制。 |

## Snowflake {#snowflake}

>[!NOTE]
>
>支持通过私有链接安全访问您的外部 Snowflake Data Warehouse。请注意，您的 Snowflake 帐户必须在 Amazon Web Services (AWS) 或 Azure 上托管，并且与您的联合受众构成环境位于同一区域。请联系您的 Adobe 代表，以获取有关设置 Snowflake 帐户安全访问权限的帮助。
>

使用联合数据库处理存储在外部数据库中的信息。执行以下步骤来配置对 Snowflake 的访问权限：

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 联合数据库]**。

1. 单击&#x200B;**[!UICONTROL 添加联合数据库]**。

   ![](assets/federated_database_1.png)

1. 为您的联合数据库输入一个&#x200B;**[!UICONTROL 名称]**。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;下拉菜单中，选择 Snowflake。

   ![](assets/federated_database_2.png)

1. 配置 Snowflake 身份验证设置：

   * **[!UICONTROL 服务器]**：输入您的服务器名称。

   * **[!UICONTROL 用户]**：输入您的用户名。

   * **[!UICONTROL 密码]**：输入您的帐户密码。

   * **[!UICONTROL 数据库]** （可选）：如果 DSN 中未指定，请输入数据库的名称。

   * **[!UICONTROL 工作架构]**（可选）：输入用于工作表的数据库架构的名称。

     >[!NOTE]
     >
     >您可以使用数据库中的任何架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限即可。
     >
     >当使用同一个数据库连接多个沙盒时，必须使用&#x200B;**不同的工作架构**。

   * **[!UICONTROL 私钥]**：单击&#x200B;**[!UICONTROL 私钥]**&#x200B;字段，从您的区域设置文件夹中选择您的 .pem 文件。

   * **[!UICONTROL 选项]**：该连接器支持下表中详述的选项。

1. 选择&#x200B;**[!UICONTROL 测试连接]**&#x200B;选项来验证您的配置。

1. 单击&#x200B;**[!UICONTROL 部署功能]**&#x200B;按钮来创建函数。

1. 配置完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;创建您的联合数据库。

该连接器支持以下选项：

| 选项 | 描述 |
|---|---|
| workschema | 用于工作表的数据库架构 |
| 仓库 | 默认使用的数据仓库名称。它将会覆盖用户的默认值。 |
| TimeZoneName | 默认为空，表示使用的是应用程序服务器的系统时区。该选项可用于强制使用 TIMEZONE 会话参数。<br>有关此内容的详细信息，请参阅[此页面](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone){target="_blank"}。 |
| WeekStart | WEEK_START 会话参数。默认设置为 0。<br>有关此内容的详细信息，请参阅[此页面](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start){target="_blank"}。 |
| UseCachedResult | USE_CACHED_RESULTS 会话参数。默认设置为真。此选项可用于禁用 Snowflake 缓存结果。<br>有关此内容的详细信息，请参阅[此页面](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html){target="_blank"}。 |
| bulkThreads | 用于 Snowflake 批量加载器的线程数，线程越多，对于更大的批量加载，性能就越好。默认设置为 1。可以根据机器线程数调整数量。 |
| chunkSize | 确定批量加载器块的文件大小。默认设置为 128MB。与 bulkThreads 一起使用时，可以进行修改，以获得更优化的性能。更多并发活动线程意味着性能更佳。<br>有关此类内容的更多信息，请参阅[Snowflake文档](https://docs.snowflake.net/manuals/sql-reference/sql/put.html){target="_blank"}。 |
| StageName | 预配置内部阶段的名称。它将会用于批量加载，而不是创建新的临时阶段。 |

## Vertica Analytics {#vertica-analytics}

使用联合数据库处理存储在外部数据库中的信息。按照以下步骤配置对 Vertica Analytics 的访问权限。

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 联合数据库]**。

1. 单击&#x200B;**[!UICONTROL 添加联合数据库]**。

   ![](assets/federated_database_1.png)

1. 为您的联合数据库输入一个&#x200B;**[!UICONTROL 名称]**。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;下拉菜单中，选择 Vertica Analytics。

   ![](assets/federated_database_5.png)

1. 配置 Vertica Analytics 身份验证设置：

   * **[!UICONTROL 服务器]**：添加 [!DNL Vertica Analytics] 服务器的 URL。

   * **[!UICONTROL 帐户]**：添加用户名。

   * **[!UICONTROL 密码]**：添加账号密码。

   * **[!UICONTROL 数据库]** （可选）：如果 DSN 中未指定，请输入数据库的名称。

   * **[!UICONTROL 工作架构]**（可选）：输入用于工作表的数据库架构的名称。

     >[!NOTE]
     >
     >您可以使用数据库中的任何架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限即可。
     >
     >当使用同一个数据库连接多个沙盒时，必须使用&#x200B;**不同的工作架构**。

   * **[!UICONTROL 选项]**：该连接器支持下表中详述的选项。

1. 选择&#x200B;**[!UICONTROL 测试连接]**&#x200B;选项来验证您的配置。

1. 单击&#x200B;**[!UICONTROL 部署功能]**&#x200B;按钮来创建函数。

1. 配置完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;创建您的联合数据库。

该连接器支持以下选项：

| 选项 | 描述 |
|---|---|
| TimeZoneName | 默认为空，表示使用的是应用程序服务器的系统时区。该选项可用于强制使用 TIMEZONE 会话参数。 |

## 数据块 {#databricks}

>[!NOTE]
>
>支持通过私有链接安全访问您的外部 Databricks 数据仓库。这包括通过私有链接与 Amazon Web Services (AWS) 上托管的 Databricks 数据库建立安全连接，以及通过 VPN 与 Microsoft Azure 上托管的 Databricks 数据库建立安全连接。请联系您的 Adobe 代表，以获取有关设置安全访问权限的帮助。

使用联合数据库处理存储在外部数据库中的信息。执行以下步骤来配置对 Databricks 的访问权限。

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 联合数据库]**。

1. 单击&#x200B;**[!UICONTROL 添加联合数据库]**。

   ![](assets/federated_database_1.png)

1. 为您的联合数据库输入一个&#x200B;**[!UICONTROL 名称]**。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;下拉菜单中，选择 Databricks。

   ![](assets/databricks-config.png)

1. 配置 Databricks 身份验证设置：

   * **[!UICONTROL 服务器]**：添加您的 Databricks 服务器的名称。

   * **[!UICONTROL HTTP 路径]**：将路径添加到您的群集或仓库中。[了解详情](https://docs.databricks.com/en/integrations/compute-details.html){target="_blank"}

   * **[!UICONTROL 密码]**：添加帐户访问令牌。[了解详情](https://docs.databricks.com/en/dev-tools/auth/pat.html){target="_blank"}

   * **[!UICONTROL 目录]**：为 Databricks 目录添加字段。

   * **[!UICONTROL 工作架构]**：用于工作表的数据库架构的名称。

     >[!NOTE]
     >
     >您可以使用数据库中的任何架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限即可。
     >
     >当使用同一个数据库连接多个沙盒时，必须使用&#x200B;**不同的工作架构**。

   * **[!UICONTROL 选项]**：该连接器支持下表中详述的选项。

1. 选择&#x200B;**[!UICONTROL 测试连接]**&#x200B;选项来验证您的配置。

1. 单击&#x200B;**[!UICONTROL 部署功能]**&#x200B;按钮来创建函数。

1. 配置完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;创建您的联合数据库。

该连接器支持以下选项：

| 选项 | 描述 |
|---|---|
| TimeZoneName | 默认为空，表示使用的是应用程序服务器的系统时区。该选项可用于强制使用 TIMEZONE 会话参数。 |

## Microsoft Fabric {#microsoft-fabric}


使用联合数据库处理存储在外部数据库中的信息。按照以下步骤配置对 Microsoft Fabric 的访问权限。

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 联合数据库]**。

1. 单击&#x200B;**[!UICONTROL 添加联合数据库]**。

   ![](assets/federated_database_1.png)

1. 为您的联合数据库输入一个&#x200B;**[!UICONTROL 名称]**。

1. 在&#x200B;**[!UICONTROL 类型]**&#x200B;下拉菜单中，选择 Microsoft Fabric。

   ![](assets/microsoft-config.png)

1. 配置 Microsoft Fabric 身份验证设置：

   * **[!UICONTROL 服务器]**：输入 Microsoft Fabric 服务器的 URL。

   * **[!UICONTROL 应用程序 ID]**：输入您的 Microsoft Fabric 应用程序 ID。

   * **[!UICONTROL 客户端密码]**：输入您的客户端密码。

   * **[!UICONTROL 选项]**：该连接器支持下表中详述的选项。

1. 单击&#x200B;**[!UICONTROL 服务器 IPS]** 选择您要授权的服务器 IPS。

1. 选择&#x200B;**[!UICONTROL 测试连接]**&#x200B;选项来验证您的配置。

1. 单击&#x200B;**[!UICONTROL 部署功能]**&#x200B;按钮来创建函数。

1. 配置完成后，单击&#x200B;**[!UICONTROL 添加]**&#x200B;创建您的联合数据库。

| 选项 | 描述 |
|---|---|
| 身份验证 | 连接器支持的身份验证类型。当前支持的值：ActiveDirectoryMSI。有关详细信息，请参阅[Microsoft SQL文档](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}（连接字符串n°8示例） |

