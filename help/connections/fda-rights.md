---
title: 访问外部数据库的权限
description: 了解特定于每个数据库引擎的权限
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 3%

---

# FDA权限矩阵 {#fda-rights}

下表概述了每个系统所需的数据库权限，使用户能够通过FDA对外部数据库执行操作。

|   | Snowflake | Redshift | Google BigQuery | 数据块 |
|:-:|:-:|:-:|:-:|:-:|
| **正在连接到远程数据库** | 仓库使用情况、数据库使用情况以及架构权限使用情况 | 创建链接到AWS帐户的用户 | 创建服务帐户并授予主体对项目的访问权限 | 对目录使用CATALOG权限，对SQL仓库使用CAN_USE权限 |
| **正在创建表** | 根据方案权限创建表 | CREATE权限 | 分配给服务帐户的角色必须包含：bigquery.jobs.create和bigquery.tables.create权限 | USE SCHEMA权限和CREATE TABLE权限 |
| **正在创建索引** | 不适用 | CREATE权限 | BigQuery仅支持搜索索引。 分配给服务帐户的角色必须包含：bigquery.jobs.create、bigquery.tables.getData和bigquery.tables.createIndex权限 | 不适用 |
| **正在创建函数** | CREATE函数ON方案权限 | USAGE ON LANGUAGE plythonu权限用于调用外部python脚本 | 分配给服务帐户的角色必须包含： bigquery.jobs.create和bigquery.routines.create权限 | CREATE函数权限 |
| **正在创建过程** | 不适用 | USAGE ON LANGUAGE plythonu权限用于调用外部python脚本 | 分配给服务帐户的角色必须包含： bigquery.jobs.create和bigquery.routines.create权限 |  不适用 |
| **正在删除对象（表、索引、函数、过程）** | 拥有对象 | 拥有对象或成为超级用户 | 分配给服务帐户的角色必须包含：bigquery.jobs.create、bigquery.routines.delete、bigquery.tables.delete和bigquery.tables.deleteIndex权限 |
| **正在监视执行** | 对所需对象的MONITOR权限 | 使用EXPLAIN命令不需要任何特权 | monitoring.viewer角色 | CAN_VIEW权限 |
| **正在写入数据** | INSERT和/或UPDATE权限（取决于写入操作） | INSERT and UPDATE权限 | 分配给服务帐户的角色必须包含： bigquery.jobs.create和bigquery.tables.updateData |  MODIFY权限 |
| **将数据加载到表中** | 在方案上创建阶段，在目标表权限上选择并插入 | SELECT和INSERT权限 | 分配给服务帐户的角色必须包含：bigquery.jobs.create、bigquery.tables.getData和bigquery.tables.updateData | SELECT和MODIFY权限 |
| **正在访问客户端数据** | 选择（将来）表或视图权限 | SELECT权限 | 分配给服务帐户的角色必须包含：bigquery.jobs.create和bigquery.tables.getData for tables或bigquery.dataViewer角色 |  SELECT权限 |
| **正在访问元数据** | SELECT on INFORMATION_SCHEMA方案权限 | SELECT权限 | bigquery.metadataViewer角色 |  SELECT on INFORMATION_SCHEMA方案权限 |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **正在连接到远程数据库** | 读取（默认）权限 | CONNECT权限 | 无需权限 |
| **正在创建表** | 在数据库（仓库）上创建表并在方案上更改 | “创建表”权限 | “在方案上创建权限” |
| **正在创建索引** | 不适用 | ALTER权限 | 不适用 |
| **正在创建函数** | 不适用 | 创建函数权限 | “在方案上创建权限” |
| **正在创建过程** | 在数据库（仓库）上创建过程并在模式上更改 | “创建过程”权限 | “在方案上创建权限” |
| **正在删除对象（表、索引、函数、过程）** | 在架构上更改 | ALTER权限 | 拥有对象或对象的DROP权限 |
| **正在监视执行** | Workspace参与者或更高权限(queryinsights.exec_requests_history)  | 控制权限 | 使用EXPLAIN语句不需要特权 |
| **正在写入数据** | 在对象上插入和/或更新 | INSERT和UPDATE权限 | INSERT and UPDATE权限 |
| **将数据加载到表中** | 选择对象并插入对象 | 创建表、执行、选择、插入、更新、更改权限 | 表的INSERT权限，方案的USAGE权限 |
| **正在访问客户端数据** | 选择对象 | 选择权限 | SELECT权限 |
| **正在访问元数据** | 在INFORMATION_SCHEMA中选择 | 无需权限即可描述表 | 在方案上的用法、在表上选择以及表v_catalog.columns和v_catalog.view_columns的权限 |
