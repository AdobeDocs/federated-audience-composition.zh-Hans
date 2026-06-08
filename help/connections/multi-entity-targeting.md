---
audience: end-user
title: 在Adobe Journey Optimizer中使用联合受众组合受众进行多实体定位
description: 了解如何在Adobe Journey Optimizer历程中定位联合受众组合受众的用户档案。
source-git-commit: 297a1d5019737c35ee07967a6d7330d3ad0bac1d
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 3%

---


# 在Adobe Journey Optimizer中使用联合受众组合受众进行多实体定位

通过多实体定位，您可以使用联合受众组合受众属性作为Adobe Journey Optimizer历程中的补充标识符。 利用这些属性，可在多个实体（如帐户或订阅级别）激活受众。

## 在联合受众组合中创建受众 {#create}

要开始使用多实体定位，您首先需要在联合受众构成中创建并保存受众。

在受众组合UI中，添加&#x200B;**构建受众**&#x200B;活动以在联合组合画布中创建受众，并添加&#x200B;**保存受众**&#x200B;活动以配置受众的映射、主要标识和数据过期。

![将显示联合受众合成UI，其中显示受众。](/help/connections/assets/multi-entity-targeting/build-activity.png)

完成受众的配置后，选择&#x200B;**开始**&#x200B;以开始执行合成。 此受众及其对应的数据集将在Experience Platform中使用。

有关在联合受众组合中创建组合的更多详细信息，请参阅[创建组合指南](/help/compositions/create-composition.md)。

## 在Adobe Journey Optimizer中激活受众 {#activate}

合成执行完成后，您可以在Journey Optimizer中激活受众。 在Adobe Journey Optimizer的&#x200B;**历程管理**&#x200B;部分中，选择&#x200B;**历程**，然后选择&#x200B;**创建旅程**&#x200B;以打开旅程用户界面。

![Adobe Journey Optimizer中的“创建旅程”按钮突出显示。](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

在历程界面中，添加&#x200B;**读取受众**&#x200B;节点。 您可以通过提供标签并选择之前创建的受众来配置此节点。

![读取受众节点显示在Journey Optimizer UI中。](/help/connections/assets/multi-entity-targeting/read-journey.png)

选择之前创建的受众后，启用&#x200B;**使用补充标识符**。

![已选中“使用补充标识符”复选框。](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

您现在可以选择补充标识符。 在选择器屏幕中，选择&#x200B;**高级模式**&#x200B;并导航到&#x200B;**Experience Platform**。 在此页面中，选择您之前创建的受众的名称，然后选择要用于受众的补充标识符。

![显示表达式编辑器。](/help/connections/assets/multi-entity-targeting/add-expression.png)

## 配置历程条件 {#configure-journey}

现在您已激活并配置受众设置，可以继续配置历程的其余条件。 对于此用例，您需要在&#x200B;**读取受众**&#x200B;节点之后添加&#x200B;**优化器**&#x200B;节点，然后添加&#x200B;**操作**&#x200B;节点。

配置其余节点后，选择&#x200B;**发布**&#x200B;以完成历程创建。

![发布按钮高亮显示。](/help/connections/assets/multi-entity-targeting/select-publish.png)

您的历程现在将基于&#x200B;**补充标识符**&#x200B;而不是主要标识符来定位受众配置文件。 使用此功能，您现在可以定位多个实体（如订阅ID、帐户ID或订单ID）并将其激活到所需的渠道。

## 后续步骤 {#next-steps}

阅读本指南后，您现在了解如何在Journey Optimizer历程中使用联合受众组合受众中的补充标识符。 有关使用补充历程的详细信息，请阅读历程指南](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier)中的[使用补充标识符。
