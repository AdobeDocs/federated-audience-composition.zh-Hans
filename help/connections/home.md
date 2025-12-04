---
audience: end-user
title: 创建和管理与联合数据库的连接
description: 了解如何创建和管理与联合数据库的连接
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: tm+mt
source-wordcount: '2298'
ht-degree: 10%

---

# 创建连接 {#connections-fdb}

>[!AVAILABILITY]
>
>要访问连接，您需要以下权限之一：
>
>-**管理联合数据库**
>-**查看联合数据库**
>
>有关所需权限的更多信息，请阅读[访问控制指南](/help/governance-privacy-security/access-control.md)。

Experience Platform联合受众构成允许您从第三方数据仓库构建和丰富受众，并将受众导入到Adobe Experience Platform。

## 支持的数据库 {#supported-databases}

要使用联合数据库和Adobe Experience Platform，必须首先在这两个源之间建立连接。 使用联合受众合成，您可以连接到以下数据库。

* Amazon Redshift
* Azure Synapse Analytics
* 数据块
* Google BigQuery
* Microsoft Fabric
* Oracle
* Snowflake
* Vertica Analytics

## 创建连接 {#create}

要创建连接，请在联合数据部分中选择&#x200B;**[!UICONTROL 联合数据库]**。

![左侧导航中突出显示“联合数据库”按钮。](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

此时将显示“联合数据库”部分。 选择&#x200B;**[!UICONTROL 添加联合数据库]**&#x200B;以创建连接。

![“添加联合数据库”按钮在“联合数据库”显示页中突出显示。](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

出现“connection properties（连接属性）”弹出框。 您可以命名连接并选择要创建哪种类型的数据库。

![显示联合数据库类型。](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

选择类型后，将显示&#x200B;**[!UICONTROL 详细信息]**&#x200B;部分。 此部分根据之前选择的数据库类型而有所不同。

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>仅支持Amazon Redshift AWS、Amazon Redshift Spectrum和Amazon Redshift Serverless。
>
>此外，支持通过专用链接安全访问外部Amazon Redshift数据仓库。

选择Amazon Redshift后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| Server | 数据源的名称。 |
| 帐户 | 帐户的用户名。 |
| 密码 | 帐户的密码。 |
| 数据库 | 数据库的名称。 如果在服务器名称中指定此字段，可将此字段留空。 |
| 工作模式 | 用于工作表的数据库模式的名称。 有关此功能的更多信息，请参阅[Amazon架构文档](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}。<br/><br/>**注意：**&#x200B;您可以使用数据库中的任何架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限。 但是，在使用同一数据库连接多个沙盒时，**必须**&#x200B;使用不同的工作架构。 |

>[!TAB Azure Synapse Analytics]

>[!NOTE]
>
>如果要使用Azure Synapse Analytics创建安全连接，请联系您的Adobe客户关怀代表。

选择Azure Synapse Analytics后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| Server | Azure Synapse服务器的URL。 |
| 帐户 | Azure Synapse帐户的用户名。 |
| 密码 | Azure synapse帐户的密码。 |
| 数据库 | 数据库的名称。 如果在服务器名称中指定此字段，可将此字段留空。 |
| 选项 | 用于连接的其他选项。 对于Azure Synapse Analytics，您可以指定连接器支持的身份验证类型。 目前，联合受众组合支持`ActiveDirectoryMSI`。 有关连接字符串的更多信息，请参阅Microsoft文档[中的](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}示例连接字符串部分。 |

>[!TAB 数据库]

>[!NOTE]
>
>支持通过私有链接安全访问您的外部 Databricks 数据仓库。这包括通过私有链接与 Amazon Web Services (AWS) 上托管的 Databricks 数据库建立安全连接，以及通过 VPN 与 Microsoft Azure 上托管的 Databricks 数据库建立安全连接。请联系您的 Adobe 代表，以获取有关设置安全访问权限的帮助。

选择数据库后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| Server | Databricks服务器的名称。 |
| HTTP 路径 | 群集或仓库的路径。 有关路径的详细信息，请阅读有关连接详细信息[的](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}数据库文档。 |
| 密码 | 数据库服务器的访问令牌。 有关此值的更多信息，请阅读有关个人访问令牌的[数据库文档](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}。 |
| Catalog | 数据库目录的名称。 有关数据库目录的详细信息，请阅读有关目录[的](https://docs.databricks.com/aws/en/catalogs/){target="_blank"}数据库文档 |
| 工作模式 | 用于工作表的数据库模式的名称。 <br/><br/>**注意：**&#x200B;您可以从数据库使用&#x200B;**any**&#x200B;架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限。 但是，在使用同一数据库连接多个沙盒时，**必须**&#x200B;使用不同的工作架构。 |
| 选项 | 用于连接的其他选项。 下表列出了可用的选项。 |

对于数据库，可以设置以下附加选项：

| 选项 | 描述 |
| ------- | ----------- |
| TimeZoneName | 要使用的时区的名称。 此值表示`TIMEZONE`会话参数。 有关时区的详细信息，请阅读[关于时区的Databricks文档](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}。 |

>[!TAB Google BigQuery]

>[!NOTE]
>
>支持通过VPN安全访问外部Google BigQuery Data Warehouse。

选择Google BigQuery后，您可以选择在与联合受众构成连接时要使用的身份验证方法。

如果选择&#x200B;**[!UICONTROL 帐户/密码身份验证]**，则可以添加以下登录信息：

| 字段 | 描述 |
| ----- | ----------- |
| 服务帐户 | 服务帐户的电子邮件地址。 有关详细信息，请阅读[Google Cloud Service帐户文档](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}。 |

如果选择&#x200B;**[!UICONTROL OAuth 2.0]**，则可以添加以下登录信息：

>[!NOTE]
>
>在使用OAuth 2.0连接到Google BigQuery之前，您需要在Google Cloud项目中配置重定向URL。 在OAuth 2.0客户端ID配置下，将重定向URL `https://fac-oauth.adobe.io/oauth`添加到您的Google Cloud项目。

| 字段 | 描述 |
| ----- | ----------- |
| 客户端 ID | Google BigQuery项目中的客户端ID。 此字段充当项目的用户名。 |
| 客户端密码 | Google BigQuery项目的客户端密钥。 此字段充当项目的密码。 |
| 访问范围 | 预填充的信息，该信息列出您的OAuth令牌在Google云资源中有权使用的范围。 |

选择&#x200B;**[!UICONTROL 登录]**&#x200B;以完成您的身份验证。

输入登录详细信息后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| 项目 | 项目的ID。 有关详细信息，请阅读[Google Cloud项目文档](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}。 |
| 数据集 | 数据集的名称。 有关详细信息，请参阅[Google Cloud数据集文档](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}。 |
| 密钥文件路径 | 到服务器的密钥文件。 仅支持`json`个文件。 |
| 选项 | 用于连接的其他选项。 下表列出了可用的选项。 |

对于Google BigQuery，您可以设置以下附加选项：

| 选项 | 描述 |
| ------- | ----------- |
| ProxyType | 用于连接到BigQuery的代理的类型。 支持的值包括`HTTP`、`http_no_tunnel`、`socks4`和`socks5`。 |
| ProxyHost | 可访问代理的主机名或IP地址。 |
| ProxyUid | 运行代理的端口号。 |
| ProxyPwd | 代理的密码。 |
| bgpath | **注意：**&#x200B;这仅适用于&#x200B;**批量加载工具** (Cloud SDK)。 <br/><br/>服务器上云SDK bin目录的路径。 只有在已将`google-cloud-sdk`目录移动到其他位置或要避免使用PATH变量时，才需要设置此项。 |
| GCloudConfigName | **注意：**&#x200B;这仅适用于7.3.4以上版本的&#x200B;**批量加载工具** (Cloud SDK)。<br/><br/>存储用于加载数据的参数的配置名称。 默认情况下，此值为`accfda`。 |
| GCloudDefaultConfigName | **注意：**&#x200B;这仅适用于7.3.4以上版本的&#x200B;**批量加载工具** (Cloud SDK)。<br/><br/>为重新创建用于加载数据的主配置的临时配置的名称。 默认情况下，此值为`default`。 |
| GCloudRecreateConfig | **注意：**&#x200B;这仅适用于7.3.4以上版本的&#x200B;**批量加载工具** (Cloud SDK)。<br/><br/>一个布尔值，可让您决定批量加载机制是否应自动重新创建、删除或修改Google Cloud SDK配置。 如果此值设置为`false`，则批量加载机制将使用计算机上的现有配置来加载数据。 如果此值设置为`true`，请确保您的配置设置正确 — 否则，将显示`No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`错误，加载机制将还原为默认的加载机制。 |

>[!TAB Microsoft结构]

选择Microsoft Fabric后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| Server | Microsoft Fabric服务器的URL。 |
| 应用程序Id | Microsoft结构的应用程序ID。 有关应用程序ID的详细信息，请阅读有关应用程序设置[的](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app){target="_blank"}Microsoft Fabric文档。 |
| 客户端密码 | 应用程序的客户端密码。 有关客户端密钥的详细信息，请阅读有关应用程序设置[的](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}Microsoft Fabric文档。 |
| 选项 | 用于连接的其他选项。 下表列出了可用的选项。 |

对于Microsoft Fabric ，可以设置以下附加选项：

| 选项 | 描述 |
| ------ | ----------- |
| 身份验证 | 连接器使用的身份验证类型。 支持的值包括： `ActiveDirectoryMSI`。 有关详细信息，请阅读有关仓库连接的[Microsoft文档](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity){target="_blank"}。 |

>[!TAB Oracle]

>[!NOTE]
>
>联合受众组合支持联合连接设置，该连接设置可与11g或更高版本上的Oracle数据库配合使用，并托管在AWS、Azure、Exadata或私有云上（只要该数据库可由外部网络访问）。 如果您有与Oracle数据库设置相关的任何进一步查询或需要创建与Oracle的安全连接，请联系您的Adobe客户关怀代表。

选择Oracle后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| Server | Oracle服务器的URL。 |
| 帐户 | 帐户的用户名。 |
| 密码 | 帐户的密码。 |

>[!TAB Snowflake]

>[!NOTE]
>
>支持通过私有链接安全访问您的外部 Snowflake Data Warehouse。请注意，您的 Snowflake 帐户必须在 Amazon Web Services (AWS) 或 Azure 上托管，并且与您的联合受众构成环境位于同一区域。请联系您的 Adobe 代表，以获取有关设置 Snowflake 帐户安全访问权限的帮助。

选择Snowflake后，您可以选择在与联合受众构成连接时要使用的身份验证方法。

如果选择&#x200B;**[!UICONTROL 帐户/密码身份验证]**，则可以添加以下登录信息：

| 字段 | 描述 |
| ----- | ----------- |
| Server | 服务器的名称。 |
| 用户 | 帐户的用户名。 |
| 密码 | 帐户的密码。 |

如果选择&#x200B;**[!UICONTROL OAuth 2.0]**，则可以添加以下登录信息：

>[!NOTE]
>
>在使用OAuth 2.0连接到Snowflake之前，您需要在Snowflake OAuth集成对象中配置重定向URL。 将重定向URL `https://fac-oauth.adobe.io/oauth`添加到您的Snowflake OAuth集成配置。

| 字段 | 描述 |
| ----- | ----------- |
| Server | 服务器的名称。 |
| 客户端 ID | Snowflake项目中的客户端ID。 此字段充当项目的用户名。 |
| 客户端密码 | Snowflake项目中的客户端密钥。 此字段充当项目的密码。 |

选择&#x200B;**[!UICONTROL 登录]**&#x200B;以完成您的身份验证。

输入登录详细信息后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| 数据库 | 数据库的名称。 如果在服务器名称中指定此字段，可将此字段留空。 |
| 工作模式 | 用于工作表的数据库模式的名称。 <br/><br/>**注意：**&#x200B;您可以从数据库使用&#x200B;**any**&#x200B;架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限。 但是，在使用同一数据库连接多个沙盒时，**必须**&#x200B;使用不同的工作架构。 |
| 私钥 | 数据库连接的私钥。 您可以从本地系统上传`.pem`文件。 |
| 选项 | 用于连接的其他选项。 下表列出了可用的选项。 |

对于Snowflake，您可以设置以下其他选项：

| 选项 | 描述 |
| ------- | ----------- |
| workschema | 用于工作表的数据库模式的名称。 |
| TimeZoneName | 要使用的时区的名称。 此值表示`TIMEZONE`会话参数。 默认情况下，将使用系统时区。 有关时区的更多信息，请阅读[Snowflake关于时区的文档](https://docs.snowflake.com/en/sql-reference/parameters#timezone){target="_blank"}。 |
| WeekStart | 您希望一周开始的那一天。 此值表示`WEEK_START`会话参数。 有关周开始的详细信息，请阅读有关周开始参数[的](https://docs.snowflake.com/en/sql-reference/parameters#week-start){target="_blank"}Snowflake文档 |
| UseCachedResult | 一个布尔值，确定是否使用Snowflake缓存的结果。 此值表示`USE_CACHED_RESULTS`会话参数。 默认情况下，此值设置为true。 有关此参数的更多信息，请阅读有关保留结果[的](https://docs.snowflake.com/en/user-guide/querying-persisted-results){target="_blank"}Snowflake文档。 |
| bulkThreads | 用于Snowflake批量加载器的线程数。 添加线程越多，批量负载越大，性能越好。 默认情况下，此值设置为1。 |
| chunkSize | 每个批量加载程序块的文件大小。 与更多线程同时使用时，您可以提高批量加载的性能。 默认情况下，此值设置为128 MB。 有关区块大小的更多信息，请阅读有关准备数据文件的[Snowflake文档](https://docs.snowflake.com/en/user-guide/data-load-considerations-prepare){target="_blank"}。 |
| StageName | 预配置的内部暂存环境的名称。 这可用于批量加载，而不是创建新的临时阶段。 |

>[!TAB Vertica Analytics]

选择Vertica Analytics后，您可以添加以下详细信息：

| 字段 | 描述 |
| ----- | ----------- |
| Server | Vertica Analytics服务器的URL。 |
| 帐户 | 帐户的用户名。 |
| 密码 | 帐户的密码。 |
| 数据库 | 数据库的名称。 如果在服务器名称中指定此字段，可将此字段留空。 |
| 工作模式 | 用于工作表的数据库模式的名称。 <br/><br/>**注意：**&#x200B;您可以从数据库使用&#x200B;**any**&#x200B;架构，包括用于临时数据处理的架构，只要您具有连接到此架构所需的权限。 但是，在使用同一数据库连接多个沙盒时，**必须**&#x200B;使用不同的工作架构。 |
| 选项 | 用于连接的其他选项。 下表列出了可用的选项。 |

对于Vertica Analytics，您可以设置以下其他选项：

| 选项 | 描述 |
| ------- | ----------- |
| TimeZoneName | 要使用的时区的名称。 此值表示`TIMEZONE`会话参数。 有关时区的更多信息，请阅读[Vertica Analytics关于时区的文档](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"} |

>[!ENDTABS]

添加连接的详细信息后，请注意以下其他设置：

>[!NOTE]
>
>要对给定数据库使用联合受众合成，必须允许列表与该数据库关联的&#x200B;**所有** IP地址。

| 设置 | 详细信息 |
| -------- | ------- |
| 启用连接 | 布尔值切换，确定是否自动启用连接。 |
| 服务器IP | 一个弹出窗口，显示连接数据库需要列入允许列表的IP地址。 |
| 测试连接 | 允许您验证配置详细信息。 |

现在，您可以依次选择&#x200B;**[!UICONTROL 部署函数]**&#x200B;和&#x200B;**[!UICONTROL 添加]**&#x200B;以完成联合数据库与Experience Platform之间的连接。
