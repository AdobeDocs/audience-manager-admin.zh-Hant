---
description: 使用「Audience Manager管理工具」中的「伺服器」頁可建立新的HTTP伺服器或編輯現有伺服器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: 建立或編輯 HTTP 伺服器
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 6%

---

# 建立或編輯 HTTP 伺服器 {#create-or-edit-an-http-server}

使用「Audience Manager管理工具」中的[!UICONTROL Servers]頁可建立新的HTTP伺服器或編輯現有伺服器。

>[!NOTE]
>
>您必須具有[!UICONTROL DEXADMIN]角色，才能建立新伺服器或編輯現有伺服器。

1. 要建立新伺服器，請轉至&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要編輯現有伺服器，請在&#x200B;**[!UICONTROL Label]**&#x200B;列中按一下所需的伺服器。
1. 為此伺服器指定所需的標籤。
1. 從&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉式清單中，選取所需的通訊協定：[!DNL HTTP]。
1. 填寫欄位: 

   * **[!UICONTROL Domain]:** 指定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]:** 指定此伺服器的所需埠。每種加密類型都會顯示預設埠。 如有必要，您可以變更預設埠
   * **[!UICONTROL Maximum Users Per Request]:** 指定此伺服器允許的每個請求的使用者人數上限。
   * **[!UICONTROL URL Prefix]:** 指定用 [!DNL URL] 於此伺服器的前置詞。
   * **[!UICONTROL Authentication URL]:** 指定此 [!UICONTROL Authentication URL] 伺服器 `HTTP` 的。
   * **[!UICONTROL Authentication]:** 指定所需的驗證方法： **[!UICONTROL None]**、  **[!UICONTROL Username/Password]**&#x200B;或 **[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]:** 客戶提 [!DNL HTTP] 供的包含簽名密鑰的標題 [!DNL HTTP] 名稱。預設值為[!UICONTROL X-Signature]，如下例所示：

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** 客戶提供用來簽署 [!DNL HTTP] 請求的金鑰。
   * **[!UICONTROL Show Signature Key]:** 切換是否要在瀏覽器中顯示簽名。
   * **[!UICONTROL HTTP Signature Encryption Method]:** 指定加密簽名的方法。除非客戶另有偏好，否則請使用[!UICONTROL SHA1]。

   >[!NOTE]
   >
   >如果您想要為合作夥伴的即時資料傳輸啟用[OAuth 2.0驗證](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en)，請填寫下表中的欄位。 *斜體*&#x200B;中的欄位需如實填入表格。

   | 名稱 | 值 |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *授權*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 如果要建立新伺服器，請按一下&#x200B;**[!UICONTROL Create]**；如果要編輯現有伺服器，請按一下&#x200B;**[!UICONTROL Update]**。
