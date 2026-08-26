---
title: 使用专用连接连接到联合受众合成
description: 了解如何使用专用连接设置并连接到联合受众合成。 这包括PrivateLink或站点到站点VPN。
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# 与联合受众组合的专用连接

联合受众组合支持与多个数据库的专用连接。 通过专用连接，无需遍历公共Internet即可连接到客户托管的数据仓库。

## 支持的数据库 {#supported-databases}

以下数据库支持与联合受众组合的专用连接：

| 数据库 | 云 | 专用连接类型 |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink（VPC界面端点） |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink（专用端点） |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink（Managed VPC端点） |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink（VPC界面端点） |
| [!DNL Databricks] | [!DNL Microsoft Azure] | 站点到站点VPN |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | 站点到站点VPN |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | 站点到站点VPN |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | 站点到站点VPN |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>若要与[!DNL Snowflake]一起使用专用连接，您&#x200B;**必须**&#x200B;至少在[!DNL Snowflake]上的Business Critical层或更高。 有关与[!DNL Snowflake]的专用连接的详细信息，请参阅Snowflake文档中的[专用连接指南](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound)。

与[!DNL Snowflake]一起使用专用连接取决于[!DNL Snowflake]实例所在的云提供商。

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>在继续之前，请确保从Adobe客户关怀部门获取您的AWS帐户ID。 获取AWS帐户ID后，请与[!DNL Snowflake]支持部门联系，以便[!DNL Snowflake]能够授权您的AWS帐户使用PrivateLink。

在您的AWS帐户获得授权可与[!DNL Snowflake]一起使用后，您需要获取包括`privatelink-vpce-id`、`privatelink-account-url`和`privatelink_ocsp-url`在内的值，以便获取VPC界面端点。

您可以通过以ACCOUNTADMIN身份在[!DNL Snowflake]帐户中运行以下命令来获取这些值：

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

运行这些命令后，您可以将完整的SQL输出发送到Adobe客户关怀团队，以便Adobe可以为您创建VPC界面端点。

有关创建与AWS的PrivateLink连接的更多详细信息，请阅读[AWS PrivateLink指南](https://docs.snowflake.com/en/user-guide/admin-security-privatelink)。

如果要授权PrivateLink以便与内部暂存环境一起使用，请联系Adobe客户关怀团队以启用该环境。

有关为内部暂存环境创建与AWS的PrivateLink连接的更多详细信息，请阅读[内部暂存的AWS VPC界面端点指南](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws)。

### Microsoft Azure {#snowflake-azure}

对于Microsoft Azure，您需要获取包括`privatelink-pls-id`、`privatelink-account-url`和`privatelink_ocsp-url`在内的值以创建Azure专用端点。

您可以通过在Snowflake帐户中运行以下命令来获取这些值：

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

运行这些命令后，您可以将完整的SQL输出发送到Adobe客户关怀团队，以便Adobe可以为您创建Azure专用端点。

一旦Adobe创建Azure私有端点，您即可获取私有端点资源ID。 现在您已经拥有私有端点资源ID，请联系[!DNL Snowflake]支持部门以授权您的[!DNL Snowflake]帐户，同时提供资源ID。

有关创建与Azure的PrivateLink连接的更多详细信息，请阅读[Azure PrivateLink指南](https://docs.snowflake.com/en/user-guide/privatelink-azure)。

如果要授权PrivateLink与内部暂存环境一起使用，请在[!DNL Snowflake]中运行以下命令，同时提供Adobe客户关怀部门提供的内部暂存资源ID：

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

有关为内部暂存环境创建与Azure的PrivateLink连接的更多详细信息，请阅读[Azure内部暂存专用端点指南](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure)。

## Amazon Redshift {#amazon-redshift}

预配的群集和Redshift无服务器都支持具有联合受众组合的专用连接。

>[!IMPORTANT]
>
>开始之前，请联系Adobe客户关怀团队，接收您的Amazon Web Services (AWS)帐户ID和Virtual Private Cloud (VPC) ID。 您将需要&#x200B;**两个**&#x200B;这些值才能获得跨帐户终结点访问权限。 有关授予对VPC的访问权限的更多详细信息，请参阅[授予对VPC的访问权限](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html)。

拥有AWS和VPC ID后，请转到AWS Management Console以授予受管VPC端点的跨帐户访问权限。

对于已设置的群集，请记下&#x200B;**Redshift群集标识符**&#x200B;和&#x200B;**群集所有者AWS帐户ID**&#x200B;值。 对于Redshift无服务器，请记下&#x200B;**工作组名称**&#x200B;和&#x200B;**所有者AWS帐户ID**&#x200B;值。

获取这些值后，请与Adobe客户关怀团队共享这些详细信息，以便Adobe可以创建托管的VPC端点。 然后Adobe将与您共享以下连接详细信息：**Redshift终结点URL**、**Redshift JDBC URL**&#x200B;和&#x200B;**Redshift ODBC URL**。

## 数据块 {#databricks}

>[!AVAILABILITY]
>
>若要使用与数据库的专用连接，您&#x200B;**必须**&#x200B;处于数据库的企业计划中。 有关与数据库的专用连接的详细信息，请阅读[专用链接概念指南](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts)。

将私有连接与数据库结合使用取决于您的数据库实例所在的云提供商。

### Amazon Web Services {#databricks-aws}

在使用Amazon Web Services配置之前，请与Adobe客户关怀团队联系，以便他们能够创建指向数据库的前端（入站）VPC界面端点。 此端点包括联合受众组合与您的数据库工作区的ODBC连接。

从Adobe客户关怀部门获取VPC端点ID和AWS区域后，您需要使用Adobe提供的信息注册VPC端点。

注册VPC端点后，您将需要创建一个专用访问设置(PAS)对象。 在创建端点时，将&#x200B;**专用访问级别**&#x200B;设置为&#x200B;**端点**&#x200B;级别，然后选择之前创建的VPC端点。 有关创建专用访问设置的详细信息，请参阅[配置入站PrivateLink指南](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings)。

配置专用访问设置后，您可以将VPC端点附加到工作区。 有关使用PrivateLink创建工作区的详细信息，请阅读[配置入站PrivateLink指南](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects)。

现在，所有设置均已配置，您可以与Adobe客户关怀团队共享您的数据库工作区URL。 共享数据库工作区URL后，Adobe可以配置将请求路由到工作区端点所需的DNS设置。

### Microsoft Azure {#databricks-azure}

站点到站点VPN用于安全地从Adobe连接到Azure上的Databriks工作区。 您需要设置Azure VPN网关来建立VPN通道，以安全地将数据传输到Adobe。

设置Azure VPN网关和Databricks专用端点后，请与Adobe客户关怀代表共享以下详细信息： **Azure虚拟网络网关**、**Databricks专用端点IP**、**Databricks Workspace URL**&#x200B;和&#x200B;**自治系统编号(ASN)**。

使用这些详细信息，Adobe可以建立您的连接所需的VPN通道。 建立VPN通道后，Adobe提供&#x200B;**VPN通道公共IP地址和私有IP地址**、**预共享密钥**&#x200B;以及&#x200B;**自治系统编号**。

您现在可以在Azure VNet网关中配置VPN通道。 有关详细信息，请参阅[使用VPN网关连接AWS和Azure指南](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp)。

### Google Cloud Platform {#databricks-gcp}

站点到站点VPN用于安全地从Adobe连接到Google Cloud平台上的Databricks工作区。 您需要设置Google Cloud Platform High Availability VPN网关和Cloud Router来建立VPN通道，以便安全地将数据传输到Adobe。

设置GCP HA VPN网关和云路由器后，请与Adobe客户关怀代表共享以下详细信息： **GCP HA VPN网关**、**Databricks Workspace URL**、**Private Service Connect (PSC) IP**&#x200B;以及&#x200B;**自治系统编号(ASN)**。

使用这些详细信息，Adobe可以建立您的连接所需的VPN通道。 建立VPN通道后，Adobe提供&#x200B;**VPN通道公共IP地址和私有IP地址**、**预共享密钥**&#x200B;以及&#x200B;**自治系统编号**。

您现在可以在Google Cloud Platform帐户中配置VPN通道。 有关详细信息，请阅读[创建HA VPN连接指南](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws)。

## Azure Synapse Analytics {#azure-synapse}

要与Azure Synapse Analytics连接，您首先需要创建Azure虚拟网络网关和Synapse专用端点。 Azure虚拟网络网关允许您在Azure虚拟网络之间向Synapse发送加密的流量，而Synapse私有端点允许您建立私有连接以安全地传输数据。

设置Azure虚拟网络网关和Synapse专用端点后，请与Adobe客户关怀代表共享以下详细信息： **Azure虚拟网络网关**、**Synapse专用端点IP**、**Synapse Workspace URL**&#x200B;和&#x200B;**自治服务编号(ASN)**。

使用这些详细信息，Adobe可以建立您的连接所需的VPN通道。 建立VPN通道后，Adobe提供&#x200B;**VPN通道配对**、**预共享密钥**&#x200B;以及&#x200B;**自治系统编号**。

您现在可以在Azure VNet网关中配置VPN通道。 有关详细信息，请参阅[使用VPN网关连接AWS和Azure指南](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp)。

## Google Big Query {#gbq}

要连接到Google Big Query，您首先需要创建一个Google Cloud Platform高可用性VPN网关和一个云路由器。

设置GCP HA VPN网关和云路由器后，请与Adobe客户关怀代表共享以下详细信息： **GCP HA VPN网关**、**Private Service Connect (PSC) IP**&#x200B;以及&#x200B;**自治系统编号(ASN)**。

使用这些详细信息，Adobe可以建立您的连接所需的VPN通道。 建立VPN通道后，Adobe提供&#x200B;**VPN通道公共IP地址和私有IP地址**、**预共享密钥**&#x200B;以及&#x200B;**自治系统编号**。

您现在可以在Google Cloud Platform帐户中配置VPN通道。 有关详细信息，请阅读[创建HA VPN连接指南](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws)。
