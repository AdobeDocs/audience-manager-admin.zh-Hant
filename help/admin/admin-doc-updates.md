---
description: 依日期列出 Audience Manager 管理員手冊的所有更新 (新增、刪除和更正項目)。
seo-description: All updates (additions, deletions, and corrections) to the Audience Manager Admin Guide, by date.
seo-title: Documentation Updates
title: 文件更新
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
exl-id: 8221b4df-99c2-47d3-a2ea-186a701a2b20
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 94%

---

# 文件更新 {#documentation-updates}

依日期列出 Audience Manager 管理員手冊的所有更新 (新增、刪除和更正項目)。

如需功能版本、增強功能和錯誤修正的詳細資訊，請參閱 [Experience Cloud 發行說明](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=en)。如需[!DNL Audience Manager]檔案變更，請參閱[檔案更新](https://experienceleague.adobe.com/docs/audience-manager/user-guide/documentation-updates/docs-2019.html?lang=en)。

## AAM 2019檔案更新 {#aam-2019-docs-updates}

| 主題 | 說明 |
|--- |--- |
| HTTP 格式巨集 | 新巨集 `REGION_ID_LIST` 及三個新欄位 (`sda`、`sda` 和 `sda`) 均已新增至 `USER_LIST` 巨集。 |
| HTTP 格式巨集 | 新增兩個巨集：`ECID` 和 `MCID`。 |

## AAM 2018檔案更新 {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D">建立或編輯 FTP 伺服器</a> </p> </td> 
   <td colname="col2"> <p>我們已新增 SFTP 伺服器 SSH 金鑰驗證的詳細資訊 (第 5 步)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export">如何設定匯出 Experience Cloud 的目的地...</a> </p> </td> 
   <td colname="col2"> <p>此頁面說明如何設定目的地，以匯出「Outbound Data Files」中顯示您所需 ID 類型的資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7">方法：為批次目的地授予跨帳戶 Amazon S3 儲存貯體存取權</a> </p> </td> 
   <td colname="col2"> <p>如果我們的客戶不想共用 Amazon S3 存取金鑰和秘密金鑰，可在 Amazon S3 中使用跨帳戶儲存貯體權限，傳送傳出的資料檔案。此文件會說明如何在 Audience Manager 管理員 UI 中設定此替代方案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017檔案更新 {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE">HTTP 格式巨集</a> </td> 
   <td colname="col2">以 <code>legacySegmentId</code> 取代 <code>segmentId</code> 巨集，並新增 <code>newSegmentId</code> 巨集。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6">管理公司限制</a> </td> 
   <td colname="col2"> 限制文件中新增最大特徵檔案夾數量和特徵結構深度。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD">為傳出檔案啟用 Hadoop 序列檔案傳輸</a> </td> 
   <td colname="col2"> 參閱本文，以了解如何讓客戶將傳出的 SEQ 檔案傳送到自己的 Hadoop 執行個體。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967">管理容器</a> </td> 
   <td colname="col2"> 新增建立容器的簡短說明。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations">建立或編輯公司目的地</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">新增如何平衡使用完整同步和增量同步的相關說明。 </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7">在 <span class="keyword">Adobe Media Optimizer</span> 中將 <span class="keyword">Adobe Media Optimizer</span> 佈建為 <span class="keyword">Audience Manager</span> 目的地。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations">管理公司目的地</a> </p> </td> 
   <td colname="col2"> <p>小幅修訂。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83">與 Media Optimizer 同步的 ID</a> </p> </td> 
   <td colname="col2"> <p>此新增文件說明各公司容器的 AMO 同步核取方塊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D">適用於公司的裝置圖表選項</a> </p> </td> 
   <td colname="col2"> <p>此新增文件說明如何設定裝置圖形選項。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421">API 需求與建議</a> </p> </td> 
   <td colname="col2"> <p>此新增文件說明需注意及告知客戶的幾個需求和建議。內容與相同標題的公開文件大致相同，但會隨不同閱讀客群而有所調整。請參閱公開文件中的 <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html?lang=en#api-requirements-recommendations" format="https" scope="external">API 需求與建議</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016檔案更新 {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D">建立或編輯 FTP 伺服器</a> </td> 
   <td colname="col2">新增輸出 FTP IP <b>52.44.29.204</b>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations">管理公司目的地</a> </p> </td> 
   <td colname="col2"> <p>小幅修訂。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD">建立或編輯 HTTP 伺服器</a> </p> </td> 
   <td colname="col2"> <p>「Create Server Configuration」精靈新增 <b>HTTP 簽章</b>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA">測試版環境</a> </p> </td> 
   <td colname="col2"> <p>更新測試版環境中的 URL 和主機名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B">僅依活躍使用者篩選傳出資料</a> </p> </td> 
   <td colname="col2"> <p>說明如何產生僅含活躍使用者的完整同步檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE">HTTP 格式巨集</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>此新增文件列示 HTTP 巨集和常見範例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31">HTTP 格式巨集範例</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015檔案更新 {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2015 年 12 月 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2">格式</a> </p> </td> 
   <td colname="col2"> <p>修訂巨集區段並新增範例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014檔案更新 {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主題 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2014 年 11 月 12 日 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2">格式</a> </p> </td> 
   <td colname="col2"> <p>新增 &lt;MCID&gt; 巨集的相關資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 23 日 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67">建立或編輯格式</a> </p> </td> 
   <td colname="col2"> <p>新增<span class="wintitle">「.info Receipt」</span>選項的相關資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 23 日 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2">格式</a> </p> </td> 
   <td colname="col2"> <p>新增頁面。請注意，此頁面正在架設中，預計未來幾天內會完成更新。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 22 日 </p> <p><a href="admin-destination-troubleshooting.md#">目的地設定疑難排解</a> </p> </td> 
   <td colname="col2"> <p> 新主題。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 21 日 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations">管理公司目的地</a> </p> </td> 
   <td colname="col2"> <p>重寫整個主題。新增其他資訊和其他設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 9 月 25 日 </p> <p><a href="companies/admin-manage-company-profiles.md">建立公司</a> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">「Lifecycle」</span>和<span class="wintitle">「Account Types」</span>區段新增其他資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 9 月 25 日 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile">編輯公司設定檔</a> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">「Lifecycle」</span>和<span class="wintitle">「Account Types」</span>區段新增其他資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>
