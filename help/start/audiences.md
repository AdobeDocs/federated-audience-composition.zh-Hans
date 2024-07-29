---
audience: end-user
title: 使用受众
description: 了解如何使用受众
badge: label="限量发布版" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 25%

---

# 使用受众 {#gs-audiences}

Experience Platform联合受众合成允许您[创建合成](../compositions/gs-compositions.md)，您可以在其中将各种活动利用到可视画布中创建受众并将它们存储到Adobe Experience Platform受众门户中。

然后，您可以在Journey Optimizer中定位这些受众，或将其激活到Adobe Experience Platform支持的任何目标。

## 使用合成创建受众 {#creation}

要使用联合受众组合创建受众，您需要创建包含&#x200B;**[!UICONTROL 保存受众]**&#x200B;活动的组合。 利用此活动，可将受众保存到受众门户，并从外部数据库中选择要包含在受众中的字段。 [了解如何配置保存受众活动](../compositions/activities/save-audience.md)

使用Adobe联合数据组合创建的受众包括&#x200B;**[!UICONTROL 保存受众]**&#x200B;活动中选择的所有字段，并与所有Adobe Experience Platform受众一起存储在受众门户中。

执行组合后，生成的受众将作为外部受众保存在Adobe Experience Platform中，并可用于Adobe实时客户数据平台和/或Adobe Journey Optimizer中。

您可以将这些受众激活到Adobe Experience Platform支持的任何目标。 了解如何在[Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}中使用目标

>[!NOTE]
>
>使用 Adobe 联合受众构成创建的受众无法编辑。要对其中一个受众进行修改，您需要使用构成来创建一个新的受众。

## 在Adobe Experience Platform中访问受众 {#access-audience}

使用联合受众合成创建的受众可在受众门户中访问，该门户可从&#x200B;**受众**&#x200B;菜单访问。

**[!UICONTROL 浏览]**&#x200B;选项卡列出了存储到 Adobe Experience Platform 中的所有现有受众。您可以使用&#x200B;**[!UICONTROL 来源]**&#x200B;列或左侧窗格中的过滤器来识别列表中的联合受众构成受众。

![](assets/audiences-list.png)

有关如何在Adobe Experience Platform中使用受众的更多信息，请参阅[受众门户文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->