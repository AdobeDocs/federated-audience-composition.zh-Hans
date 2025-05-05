---
audience: end-user
title: 审核记录
description: 了解如何在审核记录中记录并访问操作和事件
exl-id: 97142f54-53ce-4c2a-9d89-fdcb2a47b159
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 12%

---

# 审核记录 {#audit-trail}

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="审核记录"
>abstract="审核记录功能可实时按时间顺序详细记录对 Adobe Experience Platform 联合受众环境执行的所有操作和事件。"

**[!UICONTROL 审核跟踪]**&#x200B;功能会持续实时记录在Adobe联合构成实例中发生的操作和事件的详细日志。 它提供了一种方便的方法来访问按时间顺序排列的数据记录，从而解决各种查询，例如：工作流的状态、要修改它们的最新个人，或用户在实例中执行的活动。

+++ 了解有关审核记录可用实体的更多信息

* **Source架构审核跟踪**&#x200B;允许您在Adobe联合受众组合实例中监视活动以及最近对架构所做的修改。

  有关架构的详细信息，请参阅此[页面](../customer/schemas.md)。

* **工作流审核跟踪**&#x200B;允许您跟踪活动以及对工作流所做的最新更改，包括其当前状态，例如：

   * 开始
   * 暂停
   * 停止
   * 重新启动
   * 清除等于操作清除历史记录
   * 模拟在模拟模式下等于操作“开始”的项
   * 唤醒等于操作立即执行待处理任务
   * 无条件停止

  有关工作流的详细信息，请参阅此[页面](../compositions/gs-compositions.md)。

* **外部帐户**&#x200B;允许您检查对Adobe受众组合实例中的外部帐户所做的修改。

  有关外部帐户的详细信息，请参阅此[页面](../connections/federated-db.md)。

+++

## 访问审核记录 {#accessing-audit-trail}

要访问实例的&#x200B;**[!UICONTROL 审核跟踪]**，请执行以下操作：

1. 在&#x200B;**[!UICONTROL 联合数据]**&#x200B;菜单下，选择&#x200B;**[!UICONTROL 审核跟踪]**。

1. 将打开&#x200B;**[!UICONTROL 审核跟踪]**&#x200B;窗口，其中包含实体列表。 Federated Audience Composition审核工作流、选项、投放和模式的创建、编辑和删除操作。

   ![](assets/audit_trail.png)

1. **[!UICONTROL 审核实体]**&#x200B;窗口为您提供有关所选实体的更多详细信息，例如：

   * **[!UICONTROL 类型]**：工作流、选项、投放或架构。
   * **[!UICONTROL 实体]**：活动的内部名称。
   * **[!UICONTROL 修改者]**：上次修改此实体的人员的用户名。
   * **[!UICONTROL 操作]**：对此实体执行的最后一个操作，已创建、已修改或已删除。
   * **[!UICONTROL 修改日期]**：对此实体执行的上次操作的日期。
