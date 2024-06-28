---
audience: end-user
title: 使用AND — 连接活动
description: 了解如何使用AND — 连接活动
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 66%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join 活动"
>abstract="此 **And — 连接** 利用活动，可同步合成的多个执行分支。 一旦完成所有之前的活动，即触发该活动。这允许您在继续执行合成之前确保已完成某些活动。"

此 **And — 连接** 利用活动，可同步合成的多个执行分支。

一旦激活所有集客过渡，换言之，一旦完成所有先行工作，此活动就会触发其所有叫客过渡。这允许您在继续执行构成之前确保某些活动已完成。

## 配置 AND-join 活动 {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="配置 AND-join 活动"
>abstract="选择您要参加的活动。在&#x200B;**主要集合**&#x200B;下拉列表中，选择要保留的集客过渡群体。"

请按照以下步骤操作，配置 **AND-连接**&#x200B;活动：

1. 添加多项活动（例如渠道活动），来构成至少两个不同的执行分支。
1. 向任何分支添加一个 **AND-连接**&#x200B;活动。
1. 在&#x200B;**合并选项**&#x200B;部分中，选中您之前希望加入的所有活动。
1. 在&#x200B;**主集**&#x200B;下拉列表中，选择您要保留的集客过渡群体。叫客过渡只能包含集客过渡群体之一。

