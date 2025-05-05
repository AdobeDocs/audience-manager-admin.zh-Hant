---
description: 您可以在「Audience Manager管理」工具的「伺服器」頁面，建立新的HTTP伺服器或編輯現有的伺服器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: 建立或編輯HTTP伺服器
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 2%

---

# 建立或編輯HTTP伺服器 {#create-or-edit-an-http-server}

使用Audience Manager管理工具中的[!UICONTROL Servers]頁面來建立新的HTTP伺服器或編輯現有的伺服器。

>[!NOTE]
>
>您必須擁有[!UICONTROL DEXADMIN]角色，才能建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請移至&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 若要編輯現有伺服器，請在&#x200B;**[!UICONTROL Label]**&#x200B;欄中按一下所需的伺服器。
1. 指定此伺服器的所需標籤。
1. 從&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉式清單中，選取所需的通訊協定： [!DNL HTTP]。
1. 填寫欄位: 

   * **[!UICONTROL Domain]：**&#x200B;指定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]：**&#x200B;指定此伺服器的所需連線埠。 預設連線埠會針對每種加密型別顯示。 您可以視需要變更預設連線埠
   * **[!UICONTROL Maximum Users Per Request]：**&#x200B;指定此伺服器允許的每個要求使用者數目上限。
   * **[!UICONTROL URL Prefix]：**&#x200B;指定要用於此伺服器的前置詞[!DNL URL]。
   * **[!UICONTROL Authentication URL]：**&#x200B;指定此`HTTP`伺服器的[!UICONTROL Authentication URL]。
   * **[!UICONTROL Authentication]：**&#x200B;指定想要的驗證方法： **[!UICONTROL None]**、**[!UICONTROL Username/Password]**&#x200B;或&#x200B;**[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]：**&#x200B;客戶提供的[!DNL HTTP]標頭名稱，其中包含[!DNL HTTP]簽章金鑰。 預設值為[!UICONTROL X-Signature]，如下列範例所示：

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

   * **[!UICONTROL HTTP Signature Key]：**&#x200B;客戶提供的用來簽署[!DNL HTTP]要求的金鑰。
   * **[!UICONTROL Show Signature Key]：**&#x200B;切換是否要在瀏覽器中顯示簽章。
   * **[!UICONTROL HTTP Signature Encryption Method]：**&#x200B;指定我們用來加密簽章的方法。 除非客戶另有偏好，否則請使用[!UICONTROL SHA1]。

   >[!NOTE]
   >
   >如果您要為協力電腦的即時資料傳輸[&#128279;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=zh-Hant)啟用OAuth 2.0驗證，請填入下表中的欄位。 必須完全依照表格填入&#x200B;*斜體*&#x200B;中的欄位。

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

1. 如果您正在建立新伺服器，請按一下&#x200B;**[!UICONTROL Create]**；如果您正在編輯現有伺服器，請按一下&#x200B;**[!UICONTROL Update]**。
