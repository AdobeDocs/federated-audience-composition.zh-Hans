---
title: 访问联合受众构成
description: 了解联合受众组合所需的权限
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 0f4bba9c749a6548da07d78136e914cc53314684
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 93%

---

# 访问联合受众构成 {#feature-access}

## 管理对沙盒的访问 {#access-sandboxes}

购买Adobe Experience Platform联合受众组合时，将同时为每个活动沙盒创建产品配置文件。 此产品轮廓是在 Admin Console 中的 **Adobe Experience Platform** 产品卡下创建的，并遵循以下命名惯例：`ACP_FAC - <<SandboxName>> - admin.`要访问特定沙盒的联合受众构成，必须将用户添加到为该沙盒创建的产品轮廓中。

例如，如果激活了一个名为“fac-test”的新沙盒，则会创建相应的产品轮廓“ACP_FAC - fac-test - admin”。为了使用此沙盒访问联合受众构成，需要将用户添加到此产品轮廓中。

## 管理对联合受众构成的访问权限

要访问&#x200B;**联合受众结构**，您必须首先确保&#x200B;**管理联合数据**&#x200B;的权限已分配给适当的角色。然后必须将这些角色分配给需要访问&#x200B;**联合受众结构**&#x200B;的用户。

请注意，只有管理员才有分配权限的权力。

1. 导航到&#x200B;**[!UICONTROL 权限]**&#x200B;菜单。

1. 从&#x200B;**[!UICONTROL 角色]**&#x200B;菜单中，选择您想要更新的&#x200B;**[!UICONTROL 角色]**。

   ![](assets/access_fda_1.png)

1. 单击&#x200B;**[!UICONTROL 编辑]**&#x200B;以修改您的角色权限。

   ![](assets/access_fda_2.png)

1. 添加&#x200B;**联合数据**&#x200B;资源，然后从下拉菜单中选择&#x200B;**[!UICONTROL 管理联合数据]**。

   ![](assets/access_fda_3.png)

1. 完成必要的更改后，请单击&#x200B;**[!UICONTROL 保存]**。

任何已分配此角色的用户的权限都将自动更新，并可访问联合受众构成。

要将此角色分配给新用户：

1. 导航到角色仪表板中的&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 添加用户]**。

   ![](assets/access_fda_4.png)

1. 输入用户的姓名或电子邮件地址，或从可用列表中选择。完成后单击&#x200B;**[!UICONTROL 保存]**。

然后，用户会收到一封电子邮件，其中包含访问实例的说明。如果之前没有创建用户，请参阅[此文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/users)。
