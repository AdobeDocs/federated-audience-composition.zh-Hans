---
title: AI助手概述
description: 了解如何使用AI Assistant，包括产品知识、操作见解和创建联合受众合成。
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: 226679a38d0ad17726fd743f5df3b74879a2dd32
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 16%

---

# AI 助手概述 {#ai-assistant}

AI 助手是一种用户界面功能，旨在帮助您浏览和理解 Adobe 概念。 您可以使用AI Assistant在Adobe Experience Cloud的多个产品中更好地了解产品知识用例，包括联合受众合成。

>[!CAUTION]
>
>您必须同意 Adobe Experience Cloud 生成式 AI 用户指南，然后才能使用 AI 助手。 在[AI Assistant（旧版）概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home){target="_blank"}中了解有关协议的更多信息。

在联合受众构成中，您可以访问产品知识，学习与流程不同部分相关的 Adobe 概念。 AI Assistant支持四种类型的用例：**开放式发现** （浏览基于Experience League文档的产品概念）、**有针对性的学习和故障排除** （询问有关特定特性或功能的问题）、**操作分析** （询问有关联合受众组合中对象的问题）和&#x200B;**创建联合受众合成**。

## 访问 {#access}

要访问AI助手，请选择顶部栏上的![AI助手图标](/help/start/assets/ai-assistant/icon.png)。 AI 助手显示在屏幕右侧。 您可以选择![潜水图像替换文本](assets/do-not-localize/Smock_FullScreen_18_N.svg "展开图标")以展开AI助手窗口。

![AI助手图标突出显示，显示如何访问AI助手。](/help/start/assets/ai-assistant/access.png)

## 使用AI助手 {#using}

打开AI助手后，在屏幕底部的字段中输入您的问题，然后按Enter键。 此时会显示问题的答案。 你可以用大拇指或小拇指来评价你的回答。

![显示AI助手中的示例问题和答案。](/help/start/assets/ai-assistant/sample-question-answer.png)

## 示例问题 {#sample-questions}

以下查询显示您可以向AI Assistant提问的可用问题类型：

| 查询类型 | 示例问题 |
| ---------- | --------------- |
| 打开发现 | <ul><li>什么是联合受众构成？</li></ul> |
| 定向学习 | <ul><li>如何配置Snowflake联合数据库帐户？</li><li>如何创建联合构成？</li></ul> |
| 运营洞察 | <ul><li>我的沙盒中有多少个联合数据库？</li><li>我在过去30天内创建了多少个架构？</li></ul> |
| 创建联合受众组合 | <ul><li>创建生活在英国的客户的联合受众。</li></ul> |

此外，您可以使用AI Assistant自主创建联合受众合成。

## 创建受众 {#create-audience}

您可以使用AI Assistant通过自然语言提示创建联合受众合成。 当您使用AI Assistant创建受众时，AI Assistant会根据您的提示提出计划，并使用AI支持的自动化在浏览器中执行该计划。

例如，如果您请求AI Assistant“使用架构CUSTOMERS_Table为生活在英国的客户创建联合受众”，AI Assistant将制定创建受众的计划，包括导航到Federated Compositions页面、代理如何创建合成以及在合成完成后保存受众等步骤。

![显示示例问题和响应。](/help/start/assets/ai-assistant/ask-create.png)

如果计划看起来准确，则可以选择&#x200B;**[!UICONTROL 执行]**，让代理完成其自动化。 代理将在浏览器中自动执行在联合受众合成UI中创建所请求合成的步骤。 如果要在任何时候停止自动化，请选择&#x200B;**[!UICONTROL 停止]**。

![计划已执行，代理正在自动运行计划。](/help/start/assets/ai-assistant/execute-plan.png)

目前，受众创建技能支持以下附加功能：

- 调度程序
   - 您可以创建按定期计划运行的联合合成。 支持的值包括&#x200B;**一次**&#x200B;和&#x200B;**每日**。
- 重复数据删除
   - 您可以在数据协调期间对联合数据记录进行重复数据删除

## 后续步骤

有关AI Assistant的更多信息，包括您可以使用AI Assistant实现的示例目标，以及了解AI Assistant的工作方式，请阅读[AI Assistant概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home){target="_blank"}。

有关可向Federated Audience Composition询问的Insight操作问题的完整列表，请阅读[操作分析部分](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}。
