---
title: 访问外部数据库的权限
description: 了解您需要在每个数据库引擎上访问和执行任务所需的权限
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 5%

---

# 联合数据访问(FDA)权限矩阵 {#fda-rights}

下表概述了每个系统所需的数据库权限，允许您通过联合数据访问(FDA)对外部数据库执行操作。

|   | Snowflake | Redshift | Google BigQuery | 数据块 |
|:-:|:-:|:-:|:-:|:-:|
| **正在连接到远程数据库** | `USAGE ON WAREHOUSE`、`USAGE ON DATABASE`和`USAGE ON SCHEMA`权限 | 创建链接到AWS帐户的用户 | 创建服务帐户并授予主体对项目的访问权限 | 目录的`USE CATALOG`权限和SQL仓库的`CAN_USE`权限 |
| **正在创建表** | `CREATE TABLE ON SCHEMA`特权 | `CREATE`权限 | 分配给服务帐户的角色必须包含：`bigquery.jobs.create`和`bigquery.tables.create`权限 | `USE SCHEMA`和`CREATE TABLE`权限 |
| **正在创建索引** | 不适用 | `CREATE`权限 | BigQuery仅支持搜索索引。 分配给服务帐户的角色必须包含： `bigquery.jobs.create`、`bigquery.tables.getData`和`bigquery.tables.createIndex`权限 | 不适用 |
| **正在创建函数** | `CREATE FUNCTION ON SCHEMA`特权 | `USAGE ON LANGUAGE plpythonu`权限以调用外部Python脚本 | 分配给服务帐户的角色必须包含：`bigquery.jobs.create`和`bigquery.routines.create`权限 | `CREATE FUNCTION`权限 |
| **正在创建过程** | 不适用 | `USAGE ON LANGUAGE plpythonu`权限以调用外部Python脚本 | 分配给服务帐户的角色必须包含：`bigquery.jobs.create`和`bigquery.routines.create`权限 |  不适用 |
| **正在删除对象（表、索引、函数、过程）** | 拥有对象 | 拥有对象或成为超级用户 | 分配给服务帐户的角色必须包含： `bigquery.jobs.create`、`bigquery.routines.delete`、`bigquery.tables.delete`和`bigquery.tables.deleteIndex`权限 | 不适用 |
| **正在监视执行** | 所需对象的`MONITOR`权限 | 使用`EXPLAIN`命令不需要权限 | `monitoring.viewer`角色 | `CAN_VIEW`权限 |
| **正在写入数据** | `INSERT`和/或`UPDATE`权限（取决于写入操作） | `INSERT`和`UPDATE`权限 | 分配给服务帐户的角色必须包含： `bigquery.jobs.create`和`bigquery.tables.updateData` | `MODIFY`权限 |
| **将数据加载到表中** | 目标表权限上的`CREATE STAGE ON SCHEMA`、`SELECT`和`INSERT` | `SELECT`和`INSERT`权限 | 分配给服务帐户的角色必须包含： `bigquery.jobs.create`、`bigquery.tables.getData`和`bigquery.tables.updateData` | `SELECT`和`MODIFY`权限 |
| **正在访问客户端数据** | `SELECT on (FUTURE) TABLE(S)`或`VIEW(S)`特权 | `SELECT`权限 | 分配给服务帐户的角色必须包含： `bigquery.jobs.create`和`bigquery.tables.getData` （对于表或`bigquery.dataViewer`角色） | `SELECT`权限 |
| **正在访问元数据** | `SELECT on INFORMATION_SCHEMA SCHEMA`特权 | `SELECT`权限 | `bigquery.metadataViewer`角色 |  `SELECT on INFORMATION_SCHEMA SCHEMA`权限 |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **正在连接到远程数据库** | 读取（默认）权限 | `CONNECT`权限 | 无需权限 |
| **正在创建表** | `CREATE TABLE ON DATABASE` （仓库）和`ALTER ON SCHEMA` | `CREATE TABLE`权限 | `CREATE ON SCHEMA`特权 |
| **正在创建索引** | 不适用 | `ALTER`权限 | 不适用 |
| **正在创建函数** | 不适用 | `CREATE FUNCTION`权限 | `CREATE ON SCHEMA`特权 |
| **正在创建过程** | `CREATE PROCEDURE ON DATABASE` （仓库）和`ALTER ON SCHEMA` | `CREATE PROCEDURE`权限 | `CREATE ON SCHEMA`特权 |
| **正在删除对象（表、索引、函数、过程）** | `ALTER ON SCHEMA` | `ALTER`权限 | 拥有对象或对象的`DROP`权限 |
| **正在监视执行** | Workspace参与者或更高权限(`queryinsights.exec_requests_history`) | `CONTROL`权限 | 使用`EXPLAIN`语句不需要任何特权 |
| **正在写入数据** | `INSERT`和/或`UPDATE ON OBJECT` | `INSERT`和`UPDATE`权限 | `INSERT`和`UPDATE`权限 |
| **将数据加载到表中** | `SELECT ON OBJECT` 和 `INSERT ON OBJECT` | `CREATE TABLE`、`EXECUTE`、`SELECT`、`INSERT`、`UPDATE`和`ALTER`权限 | 对表的`INSERT`权限，对架构的`USAGE`权限 |
| **正在访问客户端数据** | `SELECT ON OBJECT` | `SELECT`权限 | `SELECT`特权 |
| **正在访问元数据** | `SELECT ON INFORMATION_SCHEMA` | 无需权限即可描述表 | `USAGE ON SCHEMA`、`SELECT on TABLE`以及表`v_catalog.columns`和`v_catalog.view_columns`的权限 |
