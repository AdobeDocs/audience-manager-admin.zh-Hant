---
description: 您可以在「OAuth2從屬端」頁面，檢視Audience Manager組態中的OAuth2從屬端清單。 您可以編輯或刪除現有的使用者端或建立新使用者端，前提是您已指派適當的使用者角色。
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: Oauth2使用者端
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
TQID: https://experienceleague.adobe.com/8thJUCb1zoj8trr-6Zw4Uyq89KvJcw2xb8dRz8W7oVE
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: baaa0dd2-d27e-4921-aae3-7888623a5fa5
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 572
ht-degree: 1%

---

# Oauth2使用者端 {#oauth-clients}

使用[!UICONTROL OAuth2 Clients]頁面檢視您[!DNL Audience Manager]組態中的[!UICONTROL OAuth2]使用者端清單。 您可以編輯或刪除現有的使用者端或建立新使用者端，前提是您已指派適當的使用者角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>確保您的客戶閱讀Audience Manager使用手冊中的[OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth)檔案。

[!DNL OAuth2]是授權代表資源擁有者提供[!DNL Audience Manager]資源之安全委派存取權的開放標準。

![](assets/oauth.png)

您可以按一下所需欄的標頭，以遞增或遞減順序排序每個欄。

使用[!UICONTROL Search]方塊或清單底部的分頁控制項來尋找所需的使用者端。

## 建立或編輯OAuth2使用者端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience Manager [!UICONTROL Admin]工具中的[!UICONTROL OAuth2 Clients]頁面來建立新的[!UICONTROL Oauth2]使用者端或編輯現有的使用者端。

1. 若要建立新的[!UICONTROL OAuth2]使用者端，請按一下&#x200B;**[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**。 若要編輯現有的[!UICONTROL OAuth2]使用者端，請在&#x200B;**[!UICONTROL Client ID]**&#x200B;欄中按一下所需的使用者端。
1. 指定此[!UICONTROL OAuth2]使用者端的所需名稱。 請注意，這是僅記錄的名稱。
1. 指定[!UICONTROL OAuth2]使用者端的電子郵件地址。 電子郵件地址數不得超過1個。
1. 從&#x200B;**[!UICONTROL Partner]**&#x200B;下拉式清單中，選取所需的夥伴。
1. 在&#x200B;**[!UICONTROL Client ID]**&#x200B;方塊中，指定所需的ID。 這是提交[!DNL API]請求時使用的值。 在您於先前步驟中的下拉式清單中選擇[!UICONTROL Partner]後，當您開始輸入時，前置詞會自動填入。 正確的格式為&lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>。
1. 視需要選取或取消選取&#x200B;**[!UICONTROL Restrict to Partner Users]**&#x200B;核取方塊。 如果選取此核取方塊，使用者必須是針對所選合作夥伴列出的[!DNL Audience Manager]使用者。 建議您選取此選項，作為最佳實務。
1. 在&#x200B;**[!UICONTROL Scope]**&#x200B;區段中，視需要選取或取消選取&#x200B;**[!UICONTROL Read]**&#x200B;及&#x200B;**[!UICONTROL Write]**&#x200B;核取方塊。
1. 在&#x200B;**[!UICONTROL Grant Type]**&#x200B;區段中，選取所需的授權方式。 建議您使用[!UICONTROL Password]和[!UICONTROL Refresh-token]選項的預設設定。

   * **[!UICONTROL Implicit]**：如果您選取此選項，[!UICONTROL Redirect URI]方塊就會啟用。 使用者在經過驗證後會獲得自動存取權杖，且會立即傳送至重新導向[!DNL URI]。
   * **[!UICONTROL Authorization Code]**：如果您選取此選項，[!UICONTROL Redirect URI]方塊就會啟用。 使用者在驗證後會傳回至使用者端，然後傳送至重新導向[!DNL URI]。
   * **[!UICONTROL Password]**：使用者是以使用者輸入的密碼驗證，而非透過授權伺服器自動驗證嘗試。
   * **[!UICONTROL Refresh_token]**：用來重新整理過期的存取Token超過一段時間。

1. 在&#x200B;**[!UICONTROL Redirect URI]**&#x200B;方塊中，指定所需的[!DNL URI]。 只有在選取&#x200B;**[!UICONTROL Implicit]**&#x200B;和&#x200B;**[!UICONTROL Authorization_code]**&#x200B;授權型別時，才會啟用此選項。 **[!UICONTROL Redirect URI]**&#x200B;方塊可讓您指定可接受[!DNL URI]值的逗號分隔值。 這是核准使用者端[!DNL API]存取權後，使用者端使用者被重新導向的[!DNL URI]。
1. 指定存取和重新整理權杖到期所需的到期時間（以秒為單位）。

   * **[!UICONTROL Access Token Expiration Time]**：存取權杖簽發後有效的秒數。 可為Null以使用平台預設值（12小時）。 也可能是–1，表示存取權杖未過期。
   * **[!UICONTROL Refresh Token Expiration Time]**：重新整理權杖發行後有效的秒數。 可為Null以使用平台預設值（30天）。

1. 按一下 **[!UICONTROL Save]**。

若要刪除[!UICONTROL OAuth2]使用者端，請按一下&#x200B;**[!UICONTROL OAuth2 Clients]**，然後按一下所需使用者端&#x200B;**[!UICONTROL Actions]**&#x200B;欄中的![](assets/icon_delete.png)。

>[!MORELIKETHIS]
>
>* [API 需求與建議](../admin-oauth2/aam-admin-api-requirements.md)
