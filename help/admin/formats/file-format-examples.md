---
description: 如何使用巨集建立傳出FTP檔案範本的範例。
seo-description: Examples of how macros are used to create outbound, FTP file templates.
seo-title: File Format Macro Examples
title: 檔案格式巨集範例
uuid: f00d431d-7e43-457a-b633-c79cbc4c8f10
exl-id: 132a8e40-8001-4a49-9304-82e852ee28fd
TQID: https://experienceleague.adobe.com/G90HDd1wpf-fgftySBnc-JG-l-DMi7X-sPopemyXpGg
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 0%

---

# 檔案格式巨集範例 {#file-format-macro-examples}

如何使用巨集建立輸出[!DNL FTP]檔案範本的範例。

>[!NOTE]
>
>在表格中，**boldface**&#x200B;型別會識別每個巨集及其相關輸出。 在格式範例中，已新增&lt; >符號，以幫助在視覺上分隔每個巨集。

## 通用巨集 {#common-macros}

這些巨集可用於任何格式欄位。 如需完整清單和定義，請參閱[檔案格式巨集](../formats/file-formats.md)。

<table id="table_B5073597219B470298EE614902DACAE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 格式和輸出範例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DPID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_ &lt;DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>輸出： <code>ftp_215_ 888_iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_ &lt;MASTER_DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>輸出： <code>ftp_215_888_ 20915_iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;SYNC_TYPE&gt;_ &lt;ORDER_ID&gt;_&lt;DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>輸出： <code>ftp_ 215_888_iter_1449756724.sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_ &lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>輸出： 
     <ul id="ul_F63D7B78AF1246639D6ED85C1621B17C"> 
      <li id="li_4D0D7B4D047345FE861FCBA2BD0408ED">完整： <code>ftp_215_888_ full_1449756724.sync </code> </li> 
      <li id="li_23F4D1F6B2784E599EDA29AA457327E6">增量： <code>ftp_215_888_ iter_1449756724.sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_&lt;SYNC_MODE&gt;_&lt;TIMESTAMP&gt;.sync </code> </p> <p>輸出： 
     <ul id="ul_11B14E740E40474F8302BDB809C428FE"> 
      <li id="li_54A3EAA468B44AC8B2528F855E03D04B">FTP： <code>ftp_215_888_iter_1449756724.sync </code> </li> 
      <li id="li_93468C56B661463CA7F62B1F5D3A53FF">https： <code>http_215_888_iter_1449756724.sync </code> </li> 
      <li id="li_8A204C7BEDBC41C096FE953B5F827DEC">S3： <code>s3_215_888_iter_1449756724.sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;SYNC_TYPE&gt;_&lt;ORDER_ID&gt;_&lt;DPID&gt;_&lt;SYNC_MODE&gt;_ &lt;TIMESTAMP&gt;.sync </code> </p> <p>輸出： <code>ftp_215_888_iter_ 1449756724.sync </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標題欄位巨集 {#header-field-macros}

巨集僅用於標頭欄位。 如需完整清單和定義，請參閱[檔案格式巨集](../formats/file-formats.md)。

<table id="table_ABC31B3D660D47969E111EBC734D5BBC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 格式和輸出範例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;ORDER_ID&gt; &lt;TAB&gt;&lt;SYNC_TYPE&gt; </code> </p> <p>輸出： <code>888 full.sync </code> </p> <p>在輸出中，非列印定位字元會分隔每個元素。 </p> </td>
  </tr>
 </tbody>
</table>

## 資料列巨集 {#data-row-macros}

巨集僅用於標頭欄位。 如需完整清單和定義，請參閱[檔案格式巨集](../formats/file-formats.md)。

<table id="table_408C6DD2B9D54550B003EAC93562E64F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 格式和輸出範例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;DP_UUID&gt;&lt;TAB&gt;&lt;DP_UUID_LIST;separator=TAB&gt; </code> </p> <p>輸出： <code>123456 UUID1 UUID2 UUID3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;DP_UUID&gt;&lt;TAB&gt; &lt;DP_UUID_LIST;separator=TAB&gt; </code> </p> <p>輸出： <code>123456 UUID1 UUID2 UUID3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST </code> </p> </td> 
   <td colname="col2"> <p>此範例會建立格式，傳回伺服器對伺服器摘要中已移除的區段。 </p> <p> 
     <code>
       {"AdvertiserId":"&lt;PIDALIAS&gt;",&nbsp;"DataCenterId":&nbsp;2,"TDID":"&lt;DP_UUID&gt;", 
      "Data":[&lt;SEGMENT_LIST:{seg|&lt;OPEN_CURLY_BRACKET&gt;"Name":"&lt;seg.alias&gt;"&lt;CLOSE_CURLY_BRACKET&gt;}; 
      separator=","&gt;&lt;if(SEGMENT_LIST&nbsp;&amp;&amp;&nbsp;REMOVED_SEGMENT_LIST)&gt;&lt;COMMA&gt;&lt;endif&gt; 
      &lt;REMOVED_SEGMENT_LIST:{seg|&lt;OPEN_CURLY_BRACKET&gt;"Name":"&lt;seg.alias&gt;", 
      "TtlInMinutes":0&lt;CLOSE_CURLY_BRACKET&gt;};&nbsp;separator=","&gt;]} 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;DP_UUID&gt; &lt;SEGMENT_LIST&gt;;separator=" "&gt; </code> </p> <p>輸出： <code>123456 105955 101183 101180 101179 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;PID&gt;&lt;TAB&gt;&lt;UUID&gt;&lt;TAB&gt;&lt;DP_UUID&gt;&lt;TAB&gt; &lt;SET_ATTRIBUTES&gt;&lt;TAB&gt;&lt;OPT_OUT&gt;&lt;TAB&gt;&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.alias&gt;,&lt;OUTPUT_ATTRIBUTE_VALUE&gt;,&lt;seg.lastUpdateTime&gt;&amp;}&gt; </code> </p> <p>輸出： <code>1159 00088008579683653741516297509717335000 17t0aj01b120hp 1 0 5,103714,1,1344114661000&amp;5,103713,1,1343250661000 </code> </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <code>TAB </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;DP_UUID&gt;&lt;TAB&gt;&lt;DP_UUID_LIST;separator=TAB&gt; </code> </p> <p>輸出： <code>123456 UUID1 UUID2 UUID3 </code> </p> <p>在輸出中，非列印定位字元會分隔每個元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt;PID&gt;&lt;TAB&gt;&lt;DP_UUID&gt;&lt;TAB&gt;&lt;SET_ATTRIBUTES&gt;&lt;TAB&gt; &lt;TRAIT_LIST;separator=“|”&gt; </code> </p> <p>輸出： <code>1131 12345 1 123|456|789 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>
