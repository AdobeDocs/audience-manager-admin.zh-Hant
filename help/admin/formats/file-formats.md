---
description: 列出可用來建立FTP型資料檔案的巨集。 有些巨集可用於所有資料檔案欄位和列。 其他巨集僅特定於標題和資料列。
seo-description: Lists the macros you can use to create FTP-based data files. Some macros can be used for all data file fields and rows. Other macros are specific to header and data rows only.
seo-title: File Format Macros
title: 檔案格式巨集
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
exl-id: e686bc33-da3e-49a9-8c71-2bc6ca399bfb
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 1%

---

# 檔案格式巨集 {#file-format-macros}

列出可用來建立[!DNL FTP]型資料檔案的巨集。 有些巨集可用於所有資料檔案欄位和列。 其他巨集僅特定於標題和資料列。

## 通用巨集 {#common-macros}

這些巨集可用於任何格式欄位。 如需範例，請參閱[檔案格式巨集範例](../formats/file-format-examples.md)。

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>非列印ASCII字元。 它表示一列或一節內容的開頭。 它也可以用來分隔檔案中的資料欄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>目標資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>使用者ID金鑰資料提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>訂單/目的地ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>訂單/目的地ID的別名。 </p> <p>此別名的值設定於目的地的<span class="wintitle">外部帳戶識別碼</span>欄位中（在<span class="wintitle">基本設定</span>區段中）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>指示同步型別。 接受下列可選變數： </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>：完整同步處理。 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>：增量同步處理。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>表示資料傳輸方法。 接受下列可選變數： </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>10位數、UTC、Unix時間戳記。 </p> <p>也可以依照Java日期/時間戳記格式規則將其格式化為<code>YYYYMMDDhhmmss</code>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 標題欄位巨集 {#header-field-macros}

巨集僅用於標頭欄位。 如需範例，請參閱[檔案格式巨集範例](../formats/file-format-examples.md)。

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>此巨集會當作分隔符號使用，在欄位之間插入定位字元。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 資料列巨集 {#data-row-macros}

巨集僅用於資料列。 如需範例，請參閱[檔案格式巨集範例](../formats/file-format-examples.md)。

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 巨集 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>插入右大括弧<code>}</code>字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>插入逗號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term">資料合作夥伴唯一使用者識別碼</span>。 如果指派給使用者/網站訪客的ID已與<span class="keyword">Audience Manager</span>裝置ID同步，則傳回該ID。 </p> <p>如果DPID為0，此巨集會傳回<span class="keyword">Audience Manager</span> ID，而不是您使用者的識別碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回包含資料合作夥伴多個ID的清單。 如果您的大型組織擁有多個子部門或您可與其共用資料的其他組織群組，這會很有用。 這個巨集會傳回這些從屬群組的ID清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>這個巨集的輸出會將資料提供者ID (DPID)對應到相關的不重複使用者ID (DPUUID)。 此巨集必須有格式字串才能控制其輸出。 範例輸出如下所示： </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p><code>maxMappings</code>設定決定您想要巨集傳回多少對應。 當<code>maxMappings=0</code>時，此巨集會傳回每個指定DPID的所有對應。 資料會依時間戳記排序（最近的時間在前），並會先傳回時間戳記最大的結果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>使用條件式<code>if</code>以及<code>SEGMENT_LIST</code>和<code>REMOVED_SEGMENT_LIST</code>巨集時需要。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>這個巨集組合會建立條件陳述式，列出使用者屬於<i>和</i>的區段。 如果不符合兩個條件或沒有資料，則會傳回空字串。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>插入左大括弧<code>{</code>字元。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。請勿使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>不再提倡。請勿使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>傳回<code>1</code>為靜態的硬式編碼值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>合作夥伴ID (PID)。 PID出現在管理UI中的<span class="wintitle">設定檔</span>標籤下。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回已移除的區段清單（若有）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回清單中的區段清單。 接受下列可選變數： </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>：舊版識別碼。 不再提倡。使用<code>sid</code> （僅限小寫）。 </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>：舊版識別碼。 不再提倡。使用<code>sid</code> （僅限小寫）。 </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>：區段識別碼。 </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>：傳回<code>5</code>，這個靜態的硬式編碼值會將資料識別為區段資料。 </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>：區段的對應。 不再提倡。使用<code>sid</code> （僅限小寫）。 </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>：表示上次實現區段時間的Unix時間戳記。 </li> 
    </ul> <p>將這些變數放在巨集後面的大括弧中。 例如，此程式碼會以垂直號「|」字元分隔結果： <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>傳回<code>1</code>為靜態的硬式編碼值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>插入定位字元分隔符號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>傳回特徵清單。 接受下列選用引數： </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>：以數值ID識別的特徵型別。 此變數會傳回： 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> 識別DPM特徵的<code>10</code> （離線、由輸入工作上線）。 </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> 識別規則型特徵的<code>3</code> （即時，；透過<span class="wintitle"> DCS </span>上線）。 </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>：特徵識別碼。 </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>：上次實現此特徵的時間。 Unix時間戳記。 </li> 
    </ul> <p>將這些變數放在巨集後面的大括弧中。 例如，此程式碼會以垂直號「|」字元分隔結果： <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span>使用者識別碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>
