---
audience: end-user
title: 使用查询建模器构建您的第一个查询
description: 了解如何在查询建模器中构建您的第一个查询。
badge: label="限量发布版" type="Informative"
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: 0efe4046cf30b4c447551c1cebbea0b4c2085a9f
workflow-type: tm+mt
source-wordcount: '2068'
ht-degree: 53%

---

# 编辑表达式 {#expression}

编辑表达式需要手动输入条件以形成规则。 利用此模式，可使用高级函数，这些函数允许您处理用于执行特定查询（如处理日期、字符串、数字字段、排序等）的值。

## 使用表达式编辑器 {#edit}

表达式编辑器可从查询建模器&#x200B;**[!UICONTROL 编辑表达式]**&#x200B;按钮获得，在配置自定义条件时，该按钮可用于&#x200B;**[!UICONTROL 属性]**&#x200B;和&#x200B;**[!UICONTROL 值]**&#x200B;字段。

| 从&#x200B;**[!UICONTROL 属性]**&#x200B;字段访问 | 从&#x200B;**[!UICONTROL 值]**&#x200B;字段访问 |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

表达式编辑器提供：

* 定义了表达式的&#x200B;**输入字段(1)**。
* 可用&#x200B;**字段(2)**&#x200B;的列表，这些字段可用于表达式中，并与查询的架构（也称为定向维度）相对应。
* **辅助函数(3)**，按类别排序。

通过直接在输入字段中输入表达式来编辑表达式。 要添加字段或辅助函数，请将光标置于要添加该字段或辅助函数的表达式中，然后单击+按钮。

![](assets/expression-editor.png){zoomable="yes"}

表达式就绪后，单击&#x200B;**[!UICONTROL 确认]**&#x200B;按钮。 表达式将显示在所选字段中。 要对其进行编辑，请打开表达式编辑器并进行所需的更改。

以下示例显示为&#x200B;**[!UICONTROL 值]**&#x200B;字段配置的表达式。 要编辑它，您需要使用&#x200B;**[!UICONTROL 编辑表达式]**&#x200B;按钮打开表达式编辑器。

![](assets/edit-expression-value.png){zoomable="yes"}

## 辅助函数

利用查询编辑工具，可使用高级功能根据所需结果和操作数据的类型执行复杂筛选。 可以使用以下函数：

### 总计

聚合函数用于对一组值执行计算。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>平均</strong><br /> </td> 
   <td> 返回数字类型列<br />的平均值 </td> 
   <td> Avg（&lt;值&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>计数</strong><br /> </td> 
   <td> 计算列<br />的非空值 </td> 
   <td> Count（&lt;值&gt;）<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>CountAll</strong><br /> </td> 
   <td> 计算返回的值（所有字段）<br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Countdistinct</strong><br /> </td> 
   <td> 计算列<br />的不同非空值 </td> 
   <td> Countdistinct（&lt;值&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>最大</strong><br /> </td> 
   <td> 返回数字、字符串或日期类型列<br />的最大值 </td> 
   <td> Max（&lt;值&gt;）<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>分钟</strong><br /> </td> 
   <td> 返回数字、字符串或日期类型列<br />的最小值 </td> 
   <td> Min（&lt;值&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>StdDev</strong><br /> </td> 
   <td> 返回数字、字符串或日期列<br />的标准偏差 </td> 
   <td> StdDev（&lt;值&gt;）<br /></td> 
  </tr>
  <tr> 
   <td> <strong>StringAgg</strong><br /> </td> 
   <td> 返回字符串类型列的值的串联，由第二个参数<br />中的字符分隔 </td> 
   <td> StringAgg（&lt;值&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>总和</strong><br /> </td> 
   <td> 返回数字、字符串或日期类型列<br />的值的总和 </td> 
   <td> Sum（&lt;值&gt;）<br /></td> 
  </tr> 
 </tbody> 
</table>

### 日期

日期函数用于操作日期或时间值。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddDays</strong><br /> </td> 
   <td> 向日期添加天数<br /> </td> 
   <td> AddDays(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddHours</strong><br /> </td> 
   <td> 向日期添加小时数<br /> </td> 
   <td> AddHours(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> 向日期添加分钟数<br /> </td> 
   <td> AddMinutes(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMonths</strong><br /> </td> 
   <td> 向日期添加月数<br /> </td> 
   <td> AddMonths(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> 向日期添加秒数<br /> </td> 
   <td> AddSeconds(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> 向日期添加年数<br /> </td> 
   <td> AddYears(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>ConvertNTZ</strong><br /> </td> 
   <td> 应用定义的会话TZ<br/>，将时间戳NTZ（不带时区的时间戳）转换为TZ（带有时区的时间戳） </td> 
   <td> ConvertNTZ （&lt;日期+时间&gt;）<br /> </td>  
  </tr>
  <tr> 
   <!--<td> <strong>ConvertTimezone</strong><br /> </td> 
   <td> <br/> </td> 
   <td> ConvertNTZ (&lt;date+time&gt;)<br /> </td>  
  </tr>-->
  <tr> 
   <td> <strong>DateCmp</strong><br /> </td> 
   <td> 比较两个日期<br/> </td> 
   <td> DateCmp（&lt;日期&gt;，&lt;日期&gt;）<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> 仅返回日期（时间为00:00）*<br /> </td> 
   <td> DateOnly(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Day</strong><br /> </td> 
   <td> 返回表示日期天数的数字<br /> </td> 
   <td> Day(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DayOfYear</strong><br /> </td> 
   <td> 返回日期<br />年中的天数 </td> 
   <td> DayOfYear(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> 返回与当前日期对应的日期减去n天<br /> </td> 
   <td> DaysAgo(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> 返回对应于当前日期减去n天<br />的日期（整数yyyymmdd） </td> 
   <td> DaysAgoInt(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> 两个日期之间的天数差<br /> </td> 
   <td> DaysDiff(&lt;结束日期&gt;, &lt;开始日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> 返回日期的年龄（以天为单位）<br /> </td> 
   <td> DaysOld(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> 返回服务器的当前系统日期<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hour</strong><br /> </td> 
   <td> 返回日期的小时数<br /> </td> 
   <td> Hour(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> 返回两个日期之间的小时数之差<br /> </td> 
   <td> HoursDiff(&lt;结束日期&gt;, &lt;开始日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Minute</strong><br /> </td> 
   <td> 返回日期的分钟数<br /> </td> 
   <td> Minute(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MinutesDiff</strong><br /> </td> 
   <td> 返回两个日期之间的分钟数之差<br /> </td> 
   <td> MinutesDiff(&lt;结束日期&gt;, &lt;开始日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Month</strong><br /> </td> 
   <td> 返回表示日期月份的数字<br /> </td> 
   <td> Month(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> 返回对应于当前日期 n 个月的日期<br /> </td> 
   <td> MonthsAgo(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsDiff</strong><br /> </td> 
   <td> 返回两个日期之间的月数之差<br /> </td> 
   <td> MonthsDiff(&lt;结束日期&gt;, &lt;开始日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> 返回日期的年龄（以月为单位）<br /> </td> 
   <td> MonthsOld(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Oldest</strong><br /> </td> 
   <td> 返回范围<br />中最早的日期 </td> 
   <td> 最旧（&lt;日期，日期&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Second</strong><br /> </td> 
   <td> 返回日期的秒数<br /> </td> 
   <td> Second(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SecondsDiff</strong><br /> </td> 
   <td> 返回两个日期之间的秒数之差<br /> </td> 
   <td> SecondsDiff(&lt;结束日期&gt;, &lt;开始日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubDays</strong><br /> </td> 
   <td> 从日期减去天数<br /> </td> 
   <td> SubDays(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubHours</strong><br /> </td> 
   <td> 从日期减去小时数<br /> </td> 
   <td> SubHours(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> 从日期减去分钟数<br /> </td> 
   <td> SubMinutes(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMonths</strong><br /> </td> 
   <td> 从日期减去月数<br /> </td> 
   <td> SubMonths(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> 从日期减去秒数<br /> </td> 
   <td> SubSeconds(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubYears</strong><br /> </td> 
   <td> 从日期减去年数<br /> </td> 
   <td> SubYears(&lt;日期&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDate</strong><br /> </td> 
   <td> 将日期+时间转换为日期<br /> </td> 
   <td> ToDate(&lt;日期 + 时间&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> 将字符串转换为日期+时间<br /> </td> 
   <td> ToDateTime(&lt;字符串&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToTimestamp</strong><br /> </td> 
   <td> 将字符串转换为时间戳<br /> </td> 
   <td> ToTimestamp（&lt;字符串&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToTimeZone</strong><br /> </td> 
   <td> 将日期+时间转换为时区<br /> </td> 
   <td> ToTimeZone（&lt;日期&gt;，&lt;时区&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> 将日期+时间舍入到最接近的秒数<br /> </td> 
   <td> TruncDate(@lastModified, &lt;秒数&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> 将日期+时间舍入为以秒表示的精度<br /> </td> 
   <td> TruncDateTZ(&lt;日期&gt;, &lt;秒数&gt;, &lt;时区&gt;&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> 将日期舍入到季度<br /> </td> 
   <td> TruncQuarter(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> 将时间部分舍入到最接近的秒<br /> </td> 
   <td> TruncTim（e&lt;日期&gt;， &lt;秒数&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> 将日期舍入到周<br /> </td> 
   <td> TruncWeek(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> 将日期+时间舍入到年度的 1 月 1 日<br /> </td> 
   <td> TruncYear(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>WeekDay</strong><br /> </td> 
   <td> 返回表示日期一周中某天的数字（0=星期一，6=星期日）<br /> </td> 
   <td> WeekDay(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Year</strong><br /> </td> 
   <td> 返回表示日期年份的数字<br /> </td> 
   <td> Year(&lt;日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearAnd Month</strong><br /> </td> 
   <td> 返回表示日期的年份和月份的数字<br /> </td> 
   <td> YearAndMonth(&lt;日期&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>年前</strong><br /> </td> 
   <td> 返回给定日期与当前日期之间的年数<br /> </td> 
   <td> YearsAgo（&lt;日期&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsDiff</strong><br /> </td> 
   <td> 返回两个日期之间的年数之差<br /> </td> 
   <td> YearsDiff(&lt;结束日期&gt;, &lt;开始日期&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> 返回日期的年龄（以年为单位）<br /> </td> 
   <td> YearsOld(&lt;日期&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>请注意，**Dateonly**&#x200B;函数考虑的是服务器的时区，而不是运算符的时区。

### 地理位置营销

利用地理位置营销函数来操作地理值。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> 返回由经度和纬度定义的两点之间的距离，以度表示。<br /> </td> 
   <td> Distance(&lt;经度 A&gt;, &lt;纬度 A&gt;, &lt;经度 B&gt;, &lt;纬度 B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 数值

数值函数用于将文本转换为数字。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> 返回数字的绝对值<br /> </td> 
   <td> Abs(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> 返回大于或等于某个数字的最小整数<br /> </td> 
   <td> Ceil(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> 返回大于或等于数字<br />的最大整数 </td> 
   <td> Floor(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> 返回两个数字中的较大者<br /> </td> 
   <td> Greatest(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> 返回两个数字中的较小者<br /> </td> 
   <td> Least(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> 返回n1除以n2<br />的整数除余数 </td> 
   <td> Mod(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> 返回两个数字的比值，以百分比表示<br /> </td> 
   <td> Percent(&lt;数字 1&gt;, &lt;数字 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> 返回随机值<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> 将数字舍入为 n 位小数<br /> </td> 
   <td> Round(&lt;数字&gt;, &lt;小数&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> 返回数字的符号<br /> </td> 
   <td> Sign(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> 将整数转换为浮点<br /> </td> 
   <td> ToDouble(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> 将浮点转换为 64 位整数<br /> </td> 
   <td> ToInt64(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> 将浮点转换为整数<br /> </td> 
   <td> ToInteger(&lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> 将 n1 取整到 n2 位小数<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 其他 

此表包含剩余的可用函数。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> 加密参数<br />中提供的字符串 </td> 
   <td> AESEncrypt（&lt;值&gt;）<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> 如果条件为true，则返回值1。 如果不存在，则返回值2.<br /> </td> 
   <td> Case(When(&lt;条件&gt;, &lt;值 1&gt;), Else(&lt;值 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> 删除值中的标志<br /> </td> 
   <td> ClearBit(&lt;标识符&gt;, &lt;标识&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> 如果值 1 为 0 或 null，则返回值 2，否则返回值 1<br /> </td> 
   <td> Coalesce(&lt;值 1&gt;, &lt;值 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> 如果值1 =值2，则返回值3。 如果未返回值4.<br /> </td> 
   <td> Decode(&lt;值 1&gt;, &lt;值 2&gt;, &lt;值 3&gt;, &lt;值 4&gt;)<br /> </td>  
  </tr> 
  <!--<tr> 
   <td> <strong>DefaultFolder</strong><br /> </td> 
   <td> Returns value 3 if value 1 = value 2. If not returns value 4.<br /> </td> 
   <td> Decode(&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;, &lt;value 4&gt;)<br /> </td>  
  </tr> -->
  <tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> 返回值 1（只能用作 case 函数的参数）<br /> </td> 
   <td> Else（&lt;值1&gt;， &lt;值2&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> 从电子邮件地址提取域名<br /> </td> 
   <td> GetEmailDomain(&lt;值&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> 检索镜像页面服务器的 URL<br /> </td> 
   <td> GetMirrorURL(&lt;值&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> 如果表达式为true，则返回值1。 如果不存在，则返回值2<br /> </td> 
   <td> Iif(&lt;条件&gt;, &lt;值 1&gt;, &lt;值 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> 指示标志是否在值中<br /> </td> 
   <td> IsBitSet(&lt;标识符&gt;, &lt;标识&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> 如果字符串1为空，则返回值2，否则返回值3<br /> </td> 
   <td> IsEmptyString（&lt;值1&gt;， &lt;值2&gt;， &lt;值3&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> 返回唯一ID<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> 如果参数为 NULL，则返回空字符串<br /> </td> 
   <td> NoNull(&lt;值&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> 返回行号<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> 强制将标志设在值中<br /> </td> 
   <td> SetBit(&lt;标识符&gt;, &lt;标识&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> 将数字转换为布尔值<br /> </td> 
   <td> ToBoolean(&lt;数字&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> 如果表达式为true，则返回值1。 如果不是，则返回值2（只能用作case函数的参数）<br /> </td> 
   <td> When(&lt;条件&gt;, &lt;值 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 字符串

字符串函数用于操作一系列字符串。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> 指示所有参数是否为非 null 且不为空<br /> </td> 
   <td> AllNonNull2（&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> 指示所有参数是否为非 null 且不为空<br /> </td> 
   <td> AllNonNull3（&lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> 返回字符串中第一个字符的ASCII值。<br /> </td> 
   <td> Ascii（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> 返回与 ASCII 代码"n"对应的字符<br /> </td> 
   <td> Char（&lt;数字&gt;）<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> 返回字符串1中字符串2的位置。<br /> </td> 
   <td> Charindex（&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>数据长度</strong><br /> </td> 
   <td> 返回字符串<br />的大小（以字节为单位） </td> 
   <td> dataLength（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> 返回字符串的 n（从 1 到 n）行<br /> </td> 
   <td> GetLine（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> 如果前两个参数相等，则返回第三个参数。 如果不是，则返回最后一个参数<br /> </td> 
   <td> IfEquals（&lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> 指示作为参数传递的 Memo 是否为 null<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> 将作为参数传递的字符串连接起来。 如有必要，在字符串之间添加空格。<br /> </td> 
   <td> JuxtWords（&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> 将作为参数传递的字符串连接起来。 如有必要，在字符串之间添加空格<br /> </td> 
   <td> JuxtWords3（&lt;字符串&gt;， &lt;字符串&gt;， &lt;字符串&gt;）<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> 返回字符串的前 n 个字符<br /> </td> 
   <td> Left（&lt;字符串&gt;， &lt;数字&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> 返回字符串<br />的长度 </td> 
   <td> Length（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>行</strong><br /> </td> 
   <td> 从字符串<br />中提取行n </td> 
   <td> Line（&lt;字符串&gt;，&lt;数字&gt;）<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> 以小写形式返回字符串<br /> </td> 
   <td> Lower（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> 返回左侧的已完成字符串<br /> </td> 
   <td> LPad （&lt;字符串&gt;， &lt;数字&gt;， &lt;字符&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> 删除字符串左侧的空格<br /> </td> 
   <td> Ltrim（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> 返回字符串以十六进制表示的 MD5 键值<br /> </td> 
   <td> Md5Digest（&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> 指定 Memo 是否包含作为参数传递的字符串<br /> </td> 
   <td> MemoContains（&lt;memo&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>节点值</strong><br /> </td> 
   <td> 从其XPath和字段数据提取XML字段的值<br /> </td> 
   <td> NodeValue （&lt;字符串&gt;， &lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> 将指定字符串值的所有匹配项替换为其他字符串值。<br /> </td> 
   <td> Replace（&lt;字符串&gt;，&lt;字符串&gt;，&lt;字符串&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> 返回字符串的最后 n 个字符<br /> </td> 
   <td> Right(&lt;字符串&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> 返回右侧的已完成字符串<br /> </td> 
   <td> RPad（&lt;字符串&gt;， &lt;数字&gt;， &lt;字符&gt;）<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> 删除字符串右侧的空格<br /> </td> 
   <td> Rtrim(&lt;字符串&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> 字符串的SHA256键的十六进制表示形式。<br /> </td> 
   <td> Sha256Digest （&lt;字符串&gt;）<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> 字符串的SHA512键的十六进制表示形式。<br /> </td> 
   <td> Sha512Digest （&lt;字符串&gt;）<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> 以大写方式返回带每个单词的第一个字母的字符串<br /> </td> 
   <td> Smart(&lt;字符串&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> 提取从字符串的字符n1开始的、长度为n2<br />的子字符串 </td> 
   <td> Substring(&lt;字符串&gt;, &lt;偏移&gt;, &lt;长度&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> 将数字转换为字符串<br /> </td> 
   <td> ToString（&lt;数字&gt;， &lt;数字&gt;）<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> 返回以大写表示的字符串<br /> </td> 
   <td> Upper(&lt;字符串&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> 如果其他两个参数相等，则返回作为参数传递的链接的外键<br /> </td> 
   <td> VirtualLink(&lt;数字&gt;, &lt;数字&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> 如果其他两个参数相等，则返回作为参数传递的链接的外键（文本）<br /> </td> 
   <td> VirtualLinkStr(&lt;字符串&gt;, &lt;数字&gt;, &lt;数字&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 窗口

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名称</strong><br /> </td> 
   <td> <strong>描述</strong><br /> </td> 
   <td> <strong>语法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_超过__</strong><br /> </td> 
   <td> 执行作为第1参数输入的SQL函数调用，通过Partition或Order By作为第2参数<br />输入的字段 </td> 
   <td> 超过_ （&lt;值&gt;， &lt;值&gt;）<br />(_Over_) </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> 应用降序排序<br /> </td> 
   <td> Desc(&lt;值 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> 对分区中的结果进行排序<br /> </td> 
   <td> OrderBy(&lt;值 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> 对表格上的查询结果进行分区<br /> </td> 
   <td> PartitionBy(&lt;值 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> 根据表分区和排序顺序生成行号。<br /> </td> 
   <td> RowNum(PartitionBy(&lt;值 1&gt;), OrderBy(&lt;值 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
