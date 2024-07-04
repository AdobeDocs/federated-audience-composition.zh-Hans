---
audience: end-user
title: 使用等待活动
description: 了解如何使用等待活动
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 60%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="等待活动"
>abstract="**等待**&#x200B;活动用于将过渡从一个活动推迟另一个活动。"

此 **等待** 活动允许两个执行的活动之间经过一段特定时间。 例如，在执行电子邮件投放活动后，等待几天，再分析这期间产生的打开次数和点击次数，然后再执行所有后续操作（提醒电子邮件、创建受众等）。

## 配置{#wait-configuration}

请按照以下步骤操作，配置&#x200B;**等待**&#x200B;活动：

1. 添加 **等待** 将活动添加到合成中。

1. 指定集客过渡和叫客过渡之间等待的&#x200B;**持续时间**。

1. 选择时间单位 **期间** 字段：秒、分钟、小时、天。


