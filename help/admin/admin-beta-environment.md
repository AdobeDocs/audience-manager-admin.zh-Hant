---
description: 測試版環境用於測試Audience Manager實作。 在測試版中進行的變更不會影響生產資料。 Audience Manager測試版環境是生產環境的小型獨立版本。 必須在此環境中輸入並收集您要測試的所有資料。
seo-description: The beta environment is for testing Audience Manager implementations. Changes made in beta do not affect production data. The Audience Manager beta environment is a smaller-scale, standalone version of the production environment. All the data that you want to test must be entered and collected in this environment.
seo-title: Beta Environment
solution: Audience Manager
title: 測試版環境
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
exl-id: 78d5a1ff-c016-4366-ba34-9814a0d92067
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 3%

---

# 測試版環境 {#beta-environment}

測試版環境用於測試Audience Manager實作。 在測試版中進行的變更不會影響生產資料。 Audience Manager測試版環境是生產環境的小型獨立版本。 必須在此環境中輸入並收集您要測試的所有資料。

## 概述 {#overview}

<!-- beta_environment_admin.xml -->

| 服務 | URL/主機名稱 | 布建步驟 |
|--- |--- |--- |
| S3 |  | 請參閱[布建Amazon S3貯體](admin-beta-environment.md#provision-s3-buckets)。 |
| DCS | https&amp;amp；冒號；//dcs-beta.demdex.net/.. | 我們這邊不需要額外的步驟。 請參閱[存取測試版環境中的DCS](admin-beta-environment.md#access-dcs-beta-environment)。 |
| UI | https&amp;amp；冒號；//bank-beta.demdex.com | 資料會每月從生產環境複製到測試版環境。 生產憑證對測試版有效。 |
| API | https&amp;amp；冒號；//api-beta.demdex.com/... | 資料會每月從生產環境複製到測試版環境。 生產憑證對測試版有效。 |

## 布建Amazon S3貯體 {#provision-s3-buckets}

>[!NOTE]
>
>我們正在遠離使用[!DNL FTP/SFTP]。 此外，請注意，傳出資料傳輸不適用於測試版環境。

要為入站資料布建[!DNL S3]貯體，請執行以下操作：

1. 使用&#x200B;[**SKMS要求TechOps說明**](https://skms.adobe.com/)功能。
1. 前往左側導覽邊欄中的&#x200B;**[!UICONTROL Request TechOps Help]**。
1. 在&#x200B;**[!UICONTROL Request Search]**&#x200B;中，在搜索欄位中鍵入Audience Manager。
1. 向下捲動搜尋結果，然後按一下&#x200B;**Audience Manager- S3入站/出站帳戶布建**。
1. 填寫布建窗口中的欄位，並在&#x200B;**[!UICONTROL Environment]**&#x200B;欄位中指定&#x200B;**沙箱環境**。

>[!NOTE]
>
>我們不鼓勵使用[!DNL FTP/SFTP]，並鼓勵使用[!UICONTROL Amazon S3]。 我們鼓勵使用[!UICONTROL Amazon S3]的原因列於[Amazon S3:About](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html)中。

## 存取測試版環境中的DCS {#access-dcs-beta-environment}

要訪問測試版環境中的[!UICONTROL DCS]:

1. 使用[!DNL curl] [命令](https://curl.haxx.se/docs/manpage.html)進行[!UICONTROL DCS]呼叫。 [!DNL Curl] 是使用許多支援協定之一，從伺服器傳輸資料或將資料傳輸到伺服器的工具。

   例如︰`curl -v https://dcs-beta.demdex.net/event`

1. 查看[!UICONTROL DCS]回應標題中的「[!DNL sandbox]」，確認您的要求已由測試版[!UICONTROL DCS]提供。

   例如：

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->
