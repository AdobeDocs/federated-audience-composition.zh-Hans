---
audience: end-user
title: 使用AND — 连接活动
description: 了解如何使用AND — 连接活动
exl-id: 9648f17b-e54c-4bc2-8dff-d35c438eeb8b
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 57%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join 活动"
>abstract="利用 **And-join** 活动，允许你同步构成的多个执行分支。一旦完成所有之前的活动，即触发该活动。这使您能够在继续执行构成之前确保某些活动已完成。"

**AND-join**&#x200B;活动允许您同步合成的多个执行分支。

一旦激活所有集客过渡，换言之，一旦完成所有先行工作，此活动就会触发其所有叫客过渡。这允许您在继续执行构成之前确保某些活动已完成。

## 配置 AND-join 活动 {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="配置 AND-join 活动"
>abstract="选择您要参加的活动。在&#x200B;**[!UICONTROL 主要集合]**&#x200B;下拉列表中，选择要保留的集客过渡群体。"

请按照以下步骤操作，配置 **AND-连接**&#x200B;活动：

1. 添加多个活动以形成至少两个不同的执行分支。
1. 向任何分支添加一个 **AND-连接**&#x200B;活动。

   ![](../assets/and-join.png)

1. 在&#x200B;**[!UICONTROL 合并选项]**&#x200B;部分中，检查要同步的所有先前活动。
1. 在&#x200B;**[!UICONTROL 主集]**&#x200B;下拉列表中，选择您要保留的集客过渡群体。叫客过渡只能包含其中一个集客过渡群体。 如果未配置活动，则叫客过渡将随机选择一个集客群体。
