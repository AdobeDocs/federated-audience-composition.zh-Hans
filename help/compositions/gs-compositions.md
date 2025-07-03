---
audience: end-user
title: 开始使用构成
description: 了解如何开始使用构成
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 17%

---

# 开始使用构成 {#compositions}

>[!AVAILABILITY]
>
>要访问构成，您需要以下权限之一：
>
>-**管理联合构成**
>>-**查看联合构成**
>
>有关所需权限的详细信息，请参阅[访问控制指南](/help/governance-privacy-security/access-control.md)。

联合受众合成允许您创建合成，您可以在其中将各种活动利用到可视画布中创建受众。 创建组合后，生成的受众将保存到Adobe Experience Platform中，并可在Experience Platform目标和Adobe Journey Optimizer中用于定位客户。

![联合受众组合中显示了示例组合工作流。](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## 访问和管理构成 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="构成"
>abstract="在此屏幕中可访问整个构成列表、检查他们当前的状态、上次/下次执行日期以及创建新构成。"

合成可从&#x200B;**[!UICONTROL 客户]**&#x200B;部分的&#x200B;**[!UICONTROL Federated Compositions]**&#x200B;选项卡中的Adobe Experience Platform **[!UICONTROL 受众]**&#x200B;菜单访问。

从此屏幕中，您可以创建新的构成并访问现有的构成。您还可以通过选择现有合成名称旁边的![省略号](/help/assets/icons/more.png)按钮来复制或删除现有合成。

您还可以查看有关合成的信息，包括名称、状态、创建者和上次修改日期。

| 状态 | 描述 |
| ------ | ----------- |
| **[!UICONTROL 草稿]** | 已创建并保存合成。 |
| **[!UICONTROL 进行中]** | 构成已执行，当前正在运行。 |
| **[!UICONTROL 已停止]** | 构成执行已完成并已停止。 |
| **[!UICONTROL 已暂停]** | 构成执行已暂停。 |
| **[!UICONTROL 错误]** | 构成执行遇到错误。 要查看有关错误的更多信息，请打开构成并访问日志。 |

您可以在[启动和监视组合指南](./start-monitor-composition.md)中了解如何启动或停止组合。

![将显示可用合成列表。](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}{align="center"}

要优化列表并查找要查找的合成，可以搜索列表并按合成的状态或上次处理日期过滤合成。

您还可以通过添加或移除列来自定义列表。为此，请选择&#x200B;**[!UICONTROL 配置列]**&#x200B;按钮，然后添加或删除所需的输出列。

![将显示可添加到合成浏览页面的可用列的列表。](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}{align="center"}

### 应用访问标签 {#access-labels}

要将访问标签应用于特定构成，请选择该构成，然后选择&#x200B;**[!UICONTROL 管理访问权限]**。

![组合画布中突出显示“管理访问权限”按钮。](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

出现&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;弹出框。 在此页面上，您可以将适用的访问和数据治理标签应用于您的合成。

![将显示“管理访问权限”弹出框。 这会显示您可以应用于合成的所有可用标签的列表。](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

| 标签类型 | 描述 |
| ---------- | ----------- |
| 合同标签 | 合同标签（“C”标签）用于对具有合同义务或与组织的数据治理策略相关的数据进行分类。 |
| 身份标识标签 | 身份标签（“I”标签）用于对可以识别或联系特定人员的数据进行分类。 |
| 敏感标签 | 敏感标签（“S”标签）用于对您和/或您的组织视为敏感的内容进行分类。 |
| 合作伙伴生态系统标签 | 合作伙伴生态系统标签用于对来自组织外部来源的数据进行分类。 |

有关访问和数据治理标签的详细信息，请阅读[数据使用标签术语表](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference)。

## 后续步骤

阅读本指南后，您已了解如何访问、管理和创建构图的访问标签。 有关整体使用受众的详细信息，请阅读[受众指南](../start/audiences.md)。
