---
audience: end-user
title: 更改数据Source活动
description: 了解如何使用更改数据源活动来更改构成所使用的数据源，从而更灵活地管理构成中的数据。
exl-id: 8f8e627a-fef9-42b8-a42a-bfa1c421b202
source-git-commit: 59983bb7fd0f8886cc38bfcfc8d7005db4747ac0
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# 更改数据源

>[!IMPORTANT]
>
>**[!UICONTROL 更改维度]**&#x200B;和&#x200B;**[!UICONTROL 更改数据源]**&#x200B;活动不应在一行中添加&#x200B;**和**。 如果需要连续使用这两个活动，请在它们之间包含&#x200B;**[!UICONTROL 扩充]**&#x200B;活动。 这可以确保正确执行并防止潜在的冲突或错误。

**[!UICONTROL 更改数据源]**&#x200B;活动允许您更改合成使用的数据源。

## 配置 {#configure}

将&#x200B;**[!UICONTROL 更改数据源]**&#x200B;活动添加到画布后，可以为工作流定义数据源。

![数据源选项在联合受众组合工作区中突出显示。](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}

| 来源 | 描述 |
| ------ | ----------- |
| FDA外部帐户 | 连接到联合受众组合的外部云数据库。 |

选择&#x200B;**[!UICONTROL 联合数据访问(FDA)外部帐户]**&#x200B;后，您可以选择要与哪个外部帐户连接。

![显示外部帐户选项的弹出框已显示。](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}
