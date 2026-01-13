---
audience: end-user
title: 活动概述
description: 了解可在联合受众构成中使用的各种活动和过渡。
source-git-commit: 93f4a16d00c71059672c4c6a51ff36debb6c9cee
workflow-type: tm+mt
source-wordcount: '4619'
ht-degree: 33%

---

# 活动概述

在联合受众构成中，您可以添加有助于定义受众的活动和过渡。

## 活动 {#activities}

利用活动，可在受众中定义组件。

有&#x200B;**两个**&#x200B;不同类型的活动可在联合受众组合中使用：定位活动和流量控制活动。

### 目标选择活动 {#targeting}

利用定向活动，可定义构成构成受众的内容是什么。

#### 构建受众

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="受众"
>abstract="选择受众。"

通过&#x200B;**构建受众**&#x200B;活动，可为组合定义目标群体。 您可以选择现有受众或使用查询建模器来定义您自己的查询。

+++ 配置详情

将&#x200B;**构建受众**&#x200B;活动添加到合成画布后，请为受众提供一个名称。 现在，您可以指定是要创建受众还是使用现有受众。

>[!BEGINTABS]

>[!TAB 创建新受众]

选择&#x200B;**创建受众**&#x200B;后，为您的受众选择&#x200B;**架构**。 利用模式，可定义操作所定向的群体，如收件人、合同受益人、操作员或订阅者。 默认情况下，从收件人中选择架构。

![](./assets/activities/build-audience-create.png)

选择架构后，选择&#x200B;**继续**。 您现在可以在查询Modeler中定义受众的定义。 有关使用查询Modeler的更多信息，请阅读[查询Modeler概述](../query/home.md)。

>[!TAB 使用现有受众]

选择&#x200B;**读取受众**&#x200B;后，选择&#x200B;**继续**。

![](./assets/activities/build-audience-read.png)

您现在可以选择要在合成中使用的受众。

>[!ENDTABS]

选择选项后，您可以选择&#x200B;**生成叫客过渡**。 选择此选项可添加叫客过渡，如果受众群体为空，该过渡将在活动执行结束时激活。

+++

#### 更改数据源

通过&#x200B;**更改数据源**&#x200B;活动，可更改合成正在使用的数据源。

+++ 配置详情

将&#x200B;**更改数据源**&#x200B;活动添加到合成画布后，您可以定义将用于合成的数据源。

![数据源选项在联合受众组合工作区中突出显示。](./assets/activities/configure.png){zoomable="yes"}{width="70%"}

| 来源 | 描述 |
| ------ | ----------- |
| FDA外部帐户 | 连接到联合受众组合的外部云数据库。 |

选择&#x200B;**[!UICONTROL 联合数据访问(FDA)外部帐户]**&#x200B;后，您可以选择要与哪个外部帐户连接。

![显示外部帐户选项的弹出框已显示。](./assets/activities/fda-external-account.png){zoomable="yes"}{width="70%"}

+++

#### 更改维度

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="更改维度活动"
>abstract="通过此活动，可在生成受众时更改架构，也称为定位维度。它根据数据模板和输入架构移动轴。例如，您可以从“合同”架构切换到“客户端”架构。"

通过&#x200B;**更改维度**&#x200B;活动，您可以更改构成的结构描述（也称为定向维度）。

+++ 配置详情

将&#x200B;**更改维度**&#x200B;活动添加到合成画布后，您可以定义新架构以替换以前的架构。 在此模式更改期间，将保留所有记录。

![](./assets/activities/change-dimension.png)

执行合成后，将更新结果。

+++

#### 合并

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="合并活动"
>abstract="通过&#x200B;**合并**&#x200B;活动，可对集客群体执行分段。因此，您可以合并多个群体、排除其中的一部分或者仅保留多个目标共有的数据。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="交叉合并选项"
>abstract="**交集**&#x200B;可仅在活动中保留不同集客群体的共有元素。在&#x200B;**要加入的集合**&#x200B;部分中，选中您之前想要加入的所有活动。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="排除合并选项"
>abstract="**排除项**&#x200B;允许您根据特定条件从一个群体中排除某些元素。 在&#x200B;**要加入的集合**&#x200B;部分中，选中您之前想要加入的所有活动。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="选择分段类型"
>abstract="选择合并受众的方式：并集、交叉或排除。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="交叉协调选项"
>abstract="选择协调类型以定义如何处理重复项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="“协调”选项"
>abstract="选择&#x200B;**协调**&#x200B;类型以定义如何处理重复项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="差集规则"
>abstract="必要时，您可以操作集客表。事实上，要从另一个架构（也称为定位维度）排除一个目标，必须将该目标返回到与主目标相同的架构。为此，请在E **排除规则**&#x200B;部分中选择&#x200B;**添加规则**&#x200B;并指定架构更改条件。 数据协调是通过属性或联接来执行的。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="选择要合并的集合"
>abstract="在&#x200B;**要加入的集合**&#x200B;部分中，从集客过渡中选择&#x200B;**主要设置**。这是排除了元素的集合。其他集合用于匹配从主要设置中排除之前的元素。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="差集规则"
>abstract="必要时，您可以操作集客表。事实上，要从另一个架构（也称为定位维度）排除一个目标，必须将该目标返回到与主目标相同的架构。为此，请在&#x200B;**排除规则**&#x200B;部分中选择&#x200B;**添加规则**&#x200B;并指定架构更改条件。 数据协调是通过属性或联接来执行的。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="合并生成补集"
>abstract="开启&#x200B;**生成补集**&#x200B;选项以在额外的过渡中处理剩余群体。"

>[!NOTE]
>
>**组合**&#x200B;活动&#x200B;**必须**&#x200B;放在另一个活动之后，且&#x200B;**不能放在组合的开头**。

**合并**&#x200B;活动允许您通过多种方式（并集、交叉或排除）加入多个受众。

- **合并**：合并将不同的受众合并为单个受众。 这等同于OR操作。
- **交叉点**：交叉点将不同的受众合并为单个受众，只保留&#x200B;**共享**&#x200B;内容。 这等同于AND操作。
- **排除项**：排除项将不同的受众合并为单个受众，而无需指定的排除项规则。 这等同于XOR操作。

+++ 配置详情

添加多个活动以形成至少&#x200B;**两个**&#x200B;不同的分支后，将&#x200B;**合并**&#x200B;活动添加到其中一个分支的末尾。 您现在可以选择以下组合选项之一：“并集”、“交集”或“排除”。

![](./assets/activities/combine.png)

>[!BEGINTABS]

>[!TAB 并集]

![](./assets/activities/combine-union.png)

如果选择&#x200B;**合并**，则需要为合并活动选择&#x200B;**协调类型**。 协调类型允许您定义如何处理重复条目。

- **仅键**：当多个元素具有相同的键时，选择&#x200B;**仅键**&#x200B;将保留&#x200B;**一个**&#x200B;元素。 仅当传入群体是同质群体时，才能使用此选项。
- **列选择**：选择&#x200B;**列选择**&#x200B;允许您定义应用数据协调的列列表。 您可以选择包含源数据的主数据集，然后选择要用于连接的列。

>[!TAB 交集]

![](./assets/activities/combine-intersection.png)

如果选择&#x200B;**交集**，则需要为合并活动选择&#x200B;**协调类型**。 协调类型允许您定义如何处理重复条目。

- **仅键**：当多个元素具有相同的键时，选择&#x200B;**仅键**&#x200B;将保留&#x200B;**一个**&#x200B;元素。 仅当传入群体是同质群体时，才能使用此选项。
- **列选择**：选择&#x200B;**列选择**&#x200B;允许您定义应用数据协调的列列表。

配置协调类型后，您还可以选择&#x200B;**生成补码**&#x200B;选项。 生成补数会处理剩余的群体，并包含数据&#x200B;**not**&#x200B;作为交叉点的一部分。 将向活动添加其他叫客过渡。

>[!TAB 排除]

![](./assets/activities/combine-exclusion.png)

如果选择&#x200B;**排除项**，则需要从集客过渡中选择&#x200B;**主集**。 这表示将从其中排除元素的集。

选择主集后，您可以设置&#x200B;**排除规则**。 您可以选择&#x200B;**按属性匹配**&#x200B;或&#x200B;**加入**。

配置排除规则后，您还可以选择&#x200B;**生成补码**&#x200B;选项。 生成补码会处理剩余的群体，并包含数据&#x200B;**not**，该数据包含在排除项中。 将向活动添加其他叫客过渡。

+++

#### 重复数据删除

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="用于识别重复项的字段"
>abstract="在&#x200B;**[!UICONTROL 用于标识重复项的字段]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 添加属性]**&#x200B;按钮以指定相同值允许标识重复项的字段，例如：电子邮件地址、名字、姓氏等。 栏位的顺序可让您指定首要处理的条件。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="重复数据删除活动"
>abstract="**重复数据删除活动可让您删除**&#x200B;入站活动结果中的重复项。主要在定位活动之后且在允许使用目标数据的活动之前使用。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="重复数据删除设置"
>abstract="要删除传入数据中的重复项，请在以下字段中定义重复数据删除方法。默认情况下，只会保留一条记录。您还应该根据表达式或属性选择重复数据删除模式。默认情况下，要避免重复的记录是随机选择的。"

**重复数据删除**&#x200B;活动会删除受众中的任何重复结果。

+++ 配置详情

>[!NOTE]
>
>如果您有多个集客过渡，您首先需要从下拉列表中选择&#x200B;**主集**。

添加&#x200B;**重复数据删除**&#x200B;活动后，您可以选择用于标识重复项的字段。 选择&#x200B;**添加属性**&#x200B;以标识可能发生重复项的字段。

![](./assets/activities/deduplication.png)

标识字段后，即可配置重复数据删除设置。

| 设置 | 描述 |
| ------- | ----------- |
| 要保留的重复项 | 要保留的重复记录数。 如果该值设置为0，将保留&#x200B;**所有**&#x200B;重复记录。 |
| 去重方法 | 用于删除重复记录的方法。 <ul><li>**随机选择**：已随机选择删除的记录。</li><li>**使用表达式**：删除的记录基于提交的表达式。 您可以按升序或降序排序，具体取决于要删除的值。</li><li>**非空值**：删除的记录基于提交的表达式。 将删除表达式没有值的记录。</li><li>**跟随值列表**：删除的记录基于提交的字段或表达式。 您可以按升序或降序随机对剩余值进行排序。</li></ul> |

此外，您还可以选择&#x200B;**生成补码**&#x200B;选项。 生成补码会处理剩余的群体，并包含数据&#x200B;**not**，该数据包含在重复数据删除中。 将向活动添加其他叫客过渡。

+++

#### 扩充

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="扩充活动"
>abstract="通过&#x200B;**扩充**&#x200B;活动，可利用来自数据库的其他信息增强目标数据。通常在分段活动之后的构成中使用它。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="“扩充”活动"
>abstract="一旦将扩充数据添加到构成中，它就可以在 **扩充** 活动之后添加的活动中使用，以根据行为、偏好和选择将轮廓划分为不同的组。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="链接定义"
>abstract="在表数据和联合数据库之间创建链接。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="扩充协调"
>abstract="设置协调参数"

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="扩充数据"
>abstract="选择用于扩充您的构成的数据。可选择两种类型的扩充数据：架构（也称为定位维度）中的单个扩充属性或收藏集链接（即在各表之间具有 1-N 基数的链接）。"

利用&#x200B;**扩充**&#x200B;活动，可通过从联合数据库中添加其他数据来增强合成。

如果已配置与联合受众组合目标的连接，则可以使用扩充活动通过外部数据库中的属性扩充来自Adobe Experience Platform的数据。 [了解如何使用外部数据扩充Adobe Experience Platform受众](../connections/destinations.md)

+++ 配置详情

>[!NOTE]
>
>如果您有多个集客过渡，您首先需要从下拉列表中选择&#x200B;**主集**。

将&#x200B;**扩充**&#x200B;活动添加到合成后，您可以选择&#x200B;**添加扩充数据**&#x200B;以选择要用于扩充合成的属性。 您可以选择&#x200B;**编辑表达式**&#x200B;来构建高级表达式以选择属性。

![](./assets/activities/enrichment.png)

+++

#### 协调

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="协调活动"
>abstract=" **协调**&#x200B;活动允许您定义数据库中的数据与工作表中的数据之间的链接。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="协调选择字段"
>abstract="协调选择字段"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="协调创建条件"
>abstract="协调创建条件"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="协调生成补集"
>abstract="协调生成补集"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="架构"
>abstract="选择要应用于数据的新架构。通过架构（也称为定位维度）可以定义目标群体：收件人、应用程序订阅者、运营商、订阅者等。默认情况下会选择构成当前架构。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="协调规则"
>abstract="选择用于重复数据删除的协调规则。若要使用属性，请选择&#x200B;**简单属性**&#x200B;选项，然后选择源字段和目标字段。若要使用查询建模器创建您自己的协调条件，请选择&#x200B;**高级协调条件**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="选择定位维度"
>abstract="选择要协调的入站数据的架构，也称为定位维度。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="保留未协调数据"
>abstract="默认情况下，未协调的数据保留在出站过渡中，并可在工作表中使用。要删除未协调的数据，请停用&#x200B;**保留未协调的数据**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="协调属性"
>abstract="选择要用于协调数据的属性，然后确认。"

>[!NOTE]
>
>默认情况下，未协调的数据会保留在叫客过渡中，并可在工作表中供将来使用。 如果您&#x200B;**不**&#x200B;希望使用已协调数据，请停用&#x200B;**保留未协调数据**&#x200B;选项。

**协调**&#x200B;活动允许您定义联合数据库中的数据与工作表中的数据之间的链接。

+++ 配置详情

将&#x200B;**协调**&#x200B;活动添加到合成后，您可以选择用于协调的架构。

选择架构后，您需要设置协调规则。 您可以选择&#x200B;**简单属性**&#x200B;或&#x200B;**高级协调条件**。

>[!BEGINTABS]

>[!TAB 简单属性]

选择&#x200B;**简单属性**&#x200B;后，选择&#x200B;**添加规则**。 您现在可以通过添加&#x200B;**Source**&#x200B;和&#x200B;**目标**&#x200B;字段来设置协调。 **目标**&#x200B;字段对应于所选架构的字段。

![](./assets/activities/reconciliation-rules.png)

当源和目标相等时，将协调数据。 您可以通过选择&#x200B;**添加规则**&#x200B;来添加更多协调条件。 如果指定了多个连接条件，则必须验证其中的&#x200B;**所有**，以便将数据链接在一起。

>[!TAB 高级协调条件]

选择&#x200B;**高级协调条件**&#x200B;后，选择&#x200B;**创建条件**。 您现在可以使用查询建模器创建自己的协调条件。 有关使用查询Modeler的更多信息，请阅读[查询Modeler概述](../query/home.md)

![](./assets/activities/reconciliation-advanced.png)

>[!ENDTABS]

您还可以筛选已协调的数据。 选择&#x200B;**创建过滤器**&#x200B;以使用查询Modeler创建自定义条件。 有关使用查询Modeler的更多信息，请阅读[查询Modeler概述](../query/home.md)

+++

#### 保存受众

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="保存受众"
>abstract="使用此活动从构成中的上游计算得出的群体创建新受众。创建的受众被添加到受众的列表，并可通过&#x200B;**受众**&#x200B;菜单找到这些受众。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="生成出站过渡"
>abstract="如果您想在&#x200B;**保存受众**&#x200B;活动之后添加过渡，请使用此选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="主要身份标识字段"
>abstract="选择要用于轮廓的主要身份标识。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="在 Experience Platform 文档中了解详情。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="身份标识命名空间"
>abstract="选择要用于轮廓的命名空间。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces" text="在 Experience Platform 文档中了解详情。"

>[!IMPORTANT]
>
>如果您的沙盒使用&#x200B;**数据集优先**&#x200B;的合并策略，请联系 Adobe 客户服务部门以将 `Halos UPS` 数据集添加到您的合并策略中。
>
>如需了解有关合并策略的更多信息，请参阅[合并策略概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/merge-policies/overview)。

通过&#x200B;**保存受众**&#x200B;活动，可根据组合创建受众。 创建受众后，您可以在Adobe Experience Platform的受众门户中使用它们。 有关将受众与联合受众组合结合使用的更多信息，请阅读[受众概述](../start/audiences.md)。 有关Experience Platform中受众的更多信息，请阅读[受众门户概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}。

+++ 配置详情

>[!IMPORTANT]
>
>受众的名称&#x200B;**必须**&#x200B;在当前沙盒中是唯一的，并且不能与任何现有受众具有相同的名称。

将&#x200B;**保存受众**&#x200B;活动添加到合成后，您可以指定新创建受众的名称。

![](./assets/activities/save-audience.png)

现在，您可以指定映射以选择要转移到新创建的受众的字段。 选择&#x200B;**添加受众映射**，然后选择源受众和目标受众字段，并根据需要重复任意次数。

添加映射后，您可以选择主身份和命名空间以标识数据库中的目标用户档案。 主身份字段用于识别用户档案，而身份命名空间用作识别身份的键。

+++

#### 拆分

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="拆分活动"
>abstract="通过&#x200B;**拆分**&#x200B;活动，可根据不同的选择标准（如筛选规则或群体大小）将传入的群体分为多个子集。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="拆分活动的区段"
>abstract="添加所需数量的子集以划分传入的群体。<br/></br>执行&#x200B;**拆分**&#x200B;活动时，将群体按将其添加到活动的顺序划分为不同的子集。在开始构成之前，请确保您已使用箭头按钮按照符合您需求的顺序为子集排序。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="拆分活动筛选条件"
>abstract="要将筛选条件应用到子集，请选择&#x200B;**[!UICONTROL 创建筛选器]**&#x200B;并使用查询建模器配置所需的筛选规则。 例如，包括其电子邮件地址位于数据库中的传入群体的轮廓。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="拆分活动限制"
>abstract="要限制子集选择的轮廓数，请打开&#x200B;**[!UICONTROL 启用限制]**&#x200B;选项，并指定要包括的群体的数量或百分比。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="拆分活动排序"
>abstract="在为子集设置群体限制时，您可以根据特定的轮廓属性按升序或降序顺序对所选轮廓进行排名。为此，请打开&#x200B;**启用排序**&#x200B;选项。例如，您可以限制子集以仅包含购买金额最高的前 50 个轮廓。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="拆分生成补集"
>abstract="配置完所有子集后，您可以选择与任何子集均不匹配的剩余群体，并将其包含到附加出站过渡中。为此，请打开&#x200B;**生成补集**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="在同一个表中生成所有子集"
>abstract="切换该选项可将所有子集组合到单个输出过渡中。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="跳过空过渡"
>abstract="如果传入的群体为空，则切换&#x200B;**[!UICONTROL 跳过空过渡]**&#x200B;选项，以禁用此子集的输出过渡。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="启用输出群体的重叠"
>abstract="**[!UICONTROL 启用输出群体重叠]**&#x200B;选项可让您管理属于多个子集的群体。当未选中该框时，拆分活动将确保收件人不会出现在多个输出转换中，即使它满足多个子集的标准。它们将位于符合条件的第一个选项卡的目标中。选中此框后，如果收件人符合筛选条件，则可以在多个子集中找到他们。 "

**拆分**&#x200B;活动根据给定的条件将传入的群体分成多个部分。

+++ 配置详情

>[!IMPORTANT]
>
>执行&#x200B;**Split**&#x200B;活动时，按照添加顺序&#x200B;**将群体分隔到不同的子集中**。 例如，如果第一个子集拆分初始群体的70%，则下一个子集将对其余30%应用其选择标准。
>
>在执行合成之前，请确保已按希望运行拆分的顺序对子集排序。

将&#x200B;**Split**&#x200B;活动添加到合成后，您现在可以决定如何对受众进行子集。 选择&#x200B;**添加区段**&#x200B;以创建不同的分支路径。

现在，您可以提供每个子路径的详细信息。 您可以为子路径命名并指定过滤条件。 要创建筛选条件，请选择&#x200B;**创建筛选器**&#x200B;并使用查询Modeler配置筛选规则。 有关使用查询Modeler的更多信息，请阅读[查询Modeler概述](../query/home.md)。

创建筛选条件后，可以应用以下附加规则：

- **启用限制**：限制允许拆分为子集的用户档案数。 您可以将其设置为群体的一个数字或百分比。
   - 如果启用限制，则还可以根据特定配置文件属性对选定的配置文件进行排名。 打开&#x200B;**启用排序**，您可以按升序或降序对属性进行排序。
- **跳过空过渡**：如果传入的群体为空，则禁用该过渡。

现在，子集已配置完毕，您还可以设置其他几个选项。

| 选项 | 描述 |
| ------- | ----------- |
| **生成补码** | 创建包含剩余群体的叫客过渡。 |
| **启用输出群体的重叠** | 如果启用，则收件人&#x200B;**不能**&#x200B;存在于多个出站过渡中，而&#x200B;**仅**&#x200B;存在于第一个出站过渡中。 如果禁用，收件人&#x200B;**可以**&#x200B;出现在多个出站过渡中。 |
| **在同一表中生成所有子集** | 将所有子集分组到一个叫客过渡中。 |

+++

### 流程控制活动 {#flow-control}

流量控制活动允许您定义构成的组织和协调。

#### 并加入

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join 活动"
>abstract="利用 **And-join** 活动，允许你同步构成的多个执行分支。一旦完成所有之前的活动，即会触发该活动。这使您能够在继续执行构成之前确保某些活动已完成。"

**AND-join**&#x200B;活动允许您将组合的多个分支组合在一起。 此活动仅在激活&#x200B;**所有**&#x200B;集客过渡后触发。

+++ 配置详情

添加多个活动以形成至少两个不同的分支后，您可以将&#x200B;**AND-join**&#x200B;活动添加到任何分支的末尾。

![](./assets/activities/and-join.png)

在&#x200B;**合并选项**&#x200B;部分中，您可以选择要同步的所有活动。 此外，您还可以选择要保留在&#x200B;**主集**&#x200B;下拉列表中的集客过渡。

+++

#### 终止 

**End**&#x200B;活动以图形方式标记构成结束，且没有功能影响。

#### 分叉

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork"
>title="分叉活动"
>abstract="利用&#x200B;**分叉**&#x200B;活动，可创建叫客过渡以同时开始若干活动。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork_transitions"
>title="分叉活动过渡"
>abstract="默认情况下，使用&#x200B;**分叉**&#x200B;活动创建两个过渡。选择&#x200B;**添加过渡**&#x200B;按钮以定义其他出站过渡，并输入其标签。"

通过&#x200B;**分支**&#x200B;活动，可创建同时启动多个活动的多个叫客过渡。

+++ 配置详情

将&#x200B;**Fork**&#x200B;活动添加到合成中后，将自动生成两个叫客过渡。 您可以为这些叫客过渡提供一个名称。 此外，您还可以选择&#x200B;**添加过渡**&#x200B;以添加另一个出站过渡。

![](./assets/activities/fork.png)

+++

#### 调度程序

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="“调度程序”活动"
>abstract="通过&#x200B;**调度程序**&#x200B;活动，可计划何时开始受众构成。应将此活动视为已计划的一次开始。只能将它用作构成的第一个活动。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="调度程序有效期"
>abstract="可定义调度程序的有效期。它可为永久（默认），也可一直有效至特定日期。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="调度程序选项"
>abstract="定义调度程序的频率。可在特定时刻执行它、每天、每周或每月执行它一次或多次。"

**调度程序**&#x200B;活动允许您安排何时开始撰写的执行。 您&#x200B;**必须**&#x200B;将此项用作合成的第一个活动。

+++ 配置详情

将&#x200B;**调度程序**&#x200B;活动添加到合成后，可以设置合成的&#x200B;**执行频率**。 选项包括&#x200B;**一次**、**每日**、**一天多次**、**每周**&#x200B;和&#x200B;**每月**。

>[!BEGINTABS]

>[!TAB 一次]

>[!NOTE]
>
>时间设置为UTC。

如果选择&#x200B;**一次**，则合成仅执行一次。 您可以选择运行组合的日期和时间。

>[!TAB 每天]

如果选择&#x200B;**每日**，则合成每天执行一次。 但是，您可以在每月的&#x200B;**天**&#x200B;部分下执行合成。 可能的值包括&#x200B;**每天**、**工作日**、**通过选定的时段**&#x200B;和&#x200B;**选定的工作日**。

| 日期 | 描述 |
| ---------------- | ----------- |
| 每天 | 构成每天执行。 |
| 于工作日 | 构成在每个工作日执行。 |
| 在选定期间内 | 在整个选定时间段内，每天执行合成。 您可以设置循环时段的长度以及时段的开始日期。 |
| 一周的选定日期 | 构成在选定的一周中的每天执行。 |

选择运行计划当月的哪一天后，您可以选择&#x200B;**预览启动时间**&#x200B;以检查组合中接下来十次执行的计划。

>[!TAB 一天几次]

如果选择&#x200B;**一天多次**，则每天将多次执行合成。 您可以选择每天在特定时间执行合成，还是定期在设置时间执行合成。

如果选择&#x200B;**所选小时数**，则可以选择组合运行的特定时间。 如果选择&#x200B;**定期**，则可以选择组合在小时或分钟内的运行频率以及运行时间。 所有时间均采用UTC格式。

选择小时数后，您可以选择在&#x200B;**日期**&#x200B;分区下运行的频率。

| 日期 | 描述 |
| ---------------- | ----------- |
| 一周的每一天 | 构成每天执行。 |
| 在一周中的某些天 | 构成在选定的一周中的每天执行。 |

选择运行计划当月的哪一天后，您可以选择&#x200B;**预览启动时间**&#x200B;以检查组合中接下来十次执行的计划。

>[!TAB 每周]

如果选择&#x200B;**每周**，则按设置的每周频率执行合成。 如果将每周频率设置为大于1的数字，则还可以选择执行开始的日期。

选择评估频率后，您可以选择在每月的&#x200B;**天**&#x200B;部分下运行的频率。

| 日期 | 描述 |
| ---------------- | ----------- |
| 一周的每一天 | 构成每天执行。 |
| 在一周中的某些天 | 构成在选定的一周中的每天执行。 |

选择运行计划当月的哪一天后，您可以选择&#x200B;**预览启动时间**&#x200B;以检查组合中接下来十次执行的计划。

>[!TAB 每月]

如果选择&#x200B;**每月**，则按设置的每月频率执行合成。 您可以将其设置为每月或某些月。

选择每月频率后，您可以选择每月的&#x200B;**天**&#x200B;运行执行。

| 日期 | 描述 |
| ---------------- | ----------- |
| 每天 | 构成每天执行。 |
| 于工作日 | 构成在每个工作日执行。 |
| 在选定期间内 | 在整个选定时间段内，每天执行合成。 您可以设置循环时段的长度以及时段的开始日期。 |
| 一周的选定日期 | 构成在选定的一周中的每天执行。 |

一旦设置了&#x200B;**日期**，就可以选择开始时间。 所有时间均采用UTC格式。

>[!ENDTABS]

选择执行频率后，您可以选择计划的&#x200B;**有效期**。

| 有效期 | 描述 |
| --------------- | ----------- |
| **永久（永不过期）** | 构成将永不过期。 |
| **有效期** | 构成将在给定的日期之间运行。 |

+++

#### 等待

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="等待活动"
>abstract="**等待**&#x200B;活动用于将过渡从一个活动推迟另一个活动。"

**Wait**&#x200B;活动将组合的执行暂停指定的时间。

+++ 配置详情

将&#x200B;**等待**&#x200B;活动添加到合成中后，可将其设置为&#x200B;**持续时间**&#x200B;或&#x200B;**固定时间**&#x200B;等待。

![](./assets/activities/wait.png)

如果选择持续时间，则可以设置等待的时段。 此时间段的单位可以是秒、分钟、小时或天。

如果选择固定时间，则可以将构成设置为等到给定的日期和时间。 时间设置为您的&#x200B;**本地时区**。

+++

## 过渡 {#transitions}

在合成中，过渡显示了数据如何从一个活动传输到另一个活动。 过渡将数据存储在临时工作表中。 如果选择过渡，则可以查看以下信息：

- **预览架构**：您可以选择此项以查看工作表的架构。
- **预览结果**：您可以选择此项以可视化在所选过渡中传输的数据。 仅当启用了&#x200B;**保留两次执行之间的临时群体的结果**&#x200B;时，此选项才可用。

![](assets/transition-preview.png)

## 后续步骤 {#next-steps}

阅读本指南后，您将更好地了解可在构成中使用的活动和过渡。 有关一般合成的详细信息，请阅读[合成概述](./create-composition.md)。
