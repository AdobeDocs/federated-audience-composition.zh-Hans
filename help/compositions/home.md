---
audience: end-user
title: 开始使用构成
description: 了解如何开始使用构成
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: e82f1c237927af983a32c848cb9d45d84f9cf3fe
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 82%

---

# 合成概述

>[!AVAILABILITY]
>
>要访问构成，您需要以下权限之一：
>
>-**管理联合构成**
>-**查看联合构成**
>
>有关所需权限的更多信息，请阅读[访问控制指南](/help/governance-privacy-security/access-control.md)。

联合受众构成功能可让您创建构成项目，通过在可视化画布中组合各类活动，以构建受众。在创建构成项目后，生成的受众将被保存至 Adobe Experience Platform，并可用于 Experience Platform 的目标定位功能以及 Adobe Journey Optimizer，实现精准客户投放。

![联合受众构成中展示了一个示例构成工作流。](assets/compositions/composition-example.png){zoomable="yes"}{width="70%"}

## 组合组件 {#components}

联合受众组合中的组合由以下部分组成：

- **[!UICONTROL 活动]**：活动是要执行的任务，在构成中用图标表示。
- **[!UICONTROL 过渡]**：过渡将源活动链接到目标活动并定义其序列。 过渡中包含的信息存储在工作表中。 每个构成都使用多个工作台。 这些表中传送的数据可在整个合成生命周期中使用。

## 访问和管理构成 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="构成"
>abstract="在此屏幕中可访问整个构成列表、检查他们当前的状态、上次/下次执行日期以及创建新构成。"

您可以通过 Adobe Experience Platform 中的&#x200B;**[!UICONTROL 受众]**&#x200B;菜单，进入&#x200B;**[!UICONTROL 客户]**&#x200B;部分下的&#x200B;**[!UICONTROL 联合构成]**&#x200B;标签页访问构成项目。

从此屏幕中，您可以创建新的构成并访问现有的构成。您还可以点击名称旁的![省略号](/help/assets/icons/more.png)按钮，复制或删除现有的构成项目。

您还可以查看有关构成项目的信息，包括名称、状态、创建者和上次修改日期。

| 状态 | 描述 |
| ------ | ----------- |
| **[!UICONTROL 草稿]** | 该构成已创建并保存。 |
| **[!UICONTROL 进行中]** | 该构成已执行并且正在运行。 |
| **[!UICONTROL 已停止]** | 对该构成的执行已完成并停止。 |
| **[!UICONTROL 暂停]** | 对该构成的执行已暂停。 |
| **[!UICONTROL 错误]** | 对该构成的执行遇到错误。如需查看有关错误的详细信息，请打开该构成项目并访问日志。 |

您可以在[创建合成指南](./create-composition.md#monitor-logs)中了解如何启动或停止合成。

![系统会显示一份可用构成项目的列表。](assets/compositions/compositions-list.png){zoomable="yes"}{width="70%"}

您可以通过搜索列表，并按状态或最近处理日期进行筛选，从而优化列表并快速找到所需的构成项目。

您还可以通过添加或移除列来自定义该列表。为此，请点击&#x200B;**[!UICONTROL 配置列]**&#x200B;按钮，添加或移除所需的输出列。

![系统会显示可添加到构成项目浏览页面的列的列表。](assets/compositions/compositions-columns.png){zoomable="yes"}{width="70%"}

### 应用访问标签 {#access-labels}

要为特定构成项目应用访问标签，请先选择该构成项目，然后点击&#x200B;**[!UICONTROL 管理访问权限]**。

![在构成画布中，“管理访问权限”按钮已高亮显示。](assets/compositions/select-manage-access.png){zoomable="yes"}{width="70%"}

**[!UICONTROL 管理访问权限]**&#x200B;弹出窗口将会显示。在此页面，您可以为构成项目应用相应的访问权限标签和数据治理标签。

![“管理访问权限”弹出窗口会显示。该窗口显示了可应用于构成项目的所有可用标签列表。](assets/compositions/manage-access.png){zoomable="yes"}{width="70%"}

| 标签类型 | 描述 |
| ---------- | ----------- |
| 合同标签 | 合同标签（“C”标签）用于对具有合约义务或与您组织的数据治理政策相关的数据进行分类。 |
| 身份标识标签 | 身份标识标签（“I”标签）用于对可识别或联系特定个人的数据进行分类。 |
| 敏感标签 | 敏感标签（“S”标签）用于对您和/或您的组织认为敏感的数据进行分类。 |
| 合作伙伴生态系统标签 | 合作伙伴生态系统标签用于对来自您组织外部来源的数据进行分类。 |

有关访问权限标签和数据治理标签的更多信息，请参阅[数据使用标签词汇表](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/data-governance/labels/reference)。

## 创建 {#create}

您可以使用受众组合为Adobe Experience Platform创建组合。 有关详细信息，请阅读[创建合成指南](./create-composition.md)。

## 后续步骤

阅读本指南后，您已了解如何访问、管理并为构成项目创建访问标签。有关整体管理受众的更多信息，请参阅[受众指南](../start/audiences.md)。
