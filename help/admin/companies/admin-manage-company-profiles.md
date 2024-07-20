---
description: 使用「Audience Manager管理員」工具中的「公司」頁面來建立新公司。
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: 建立公司設定檔
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 2%

---

# 建立公司設定檔 {#create-a-company-profile}

使用Audience Manager管理工具中的[!UICONTROL Companies]頁面來建立新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必須擁有&#x200B;**[!UICONTROL DEXADMIN]**&#x200B;角色才能建立新公司。

1. 按一下&#x200B;**[!UICONTROL Companies]** > **[!UICONTROL Add Company]**。
1. 填寫欄位: 

   * **[!UICONTROL Name]**： （必要）指定公司的名稱。
   * **[!UICONTROL Description]**： （必要）提供公司的描述性資訊，例如產業或其全名。
   * **[!UICONTROL Subdomain]**： （必要）指定公司的子網域。 您輸入的文字會顯示為事件呼叫的子網域。 無法變更此設定。 它必須是包含[!DNL URL]個有效字元的字串。

     例如，如果貴公司名為[!DNL AcmeCorp]，則子網域將是[!DNL acmecorp]。

     Audience Manager使用[!UICONTROL Data Collection Server] (DCS)的子網域。 在上一個範例中，如果貴公司在[!UICONTROL DCS]中的完整[!DNL URL]為[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**：指定想要的公司階段：
      * **[!UICONTROL Active]**：指定公司將會是作用中Audience Manager使用者端。 [!UICONTROL Active]帳戶表示付費客戶，不僅是為了諮詢，而且也是為了使用Audience ManagerSKU。
      * **[!UICONTROL Demo]**：指定公司僅供示範之用。 系統會自動偽造報表資料。
      * **[!UICONTROL Prospect]**：指定公司是潛在的Audience Manager使用者端，例如公司獲得免費的[!DNL POC]或銷售示範的帳戶設定。
      * **[!UICONTROL Test]**：指定公司僅供內部測試之用。

   * **[!UICONTROL Account Types]**：指定此公司的完整帳戶型別集。 沒有帳戶型別與任何其他型別互斥。
      * **[!UICONTROL Full AAM]**：指定公司將擁有完整的Adobe Audience Manager帳戶，且使用者將擁有登入存取權。
      * **[!UICONTROL MMP]**：指定公司已啟用使用[!UICONTROL Master Marketing Profile] ([!UICONTROL MMP])功能。 [!UICONTROL MMP]允許使用指派給每個訪客然後由Audience Manager使用的[!UICONTROL Experience Cloud ID] ([!DNL MCID])，跨Experience Cloud共用對象。 如果您選取此帳戶型別，系統也會自動選取[!UICONTROL Experience Cloud ID Service]。

        如需詳細資訊，請參閱[Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。

   * **[!UICONTROL Data Source]**：指定公司是Audience Manager中的協力廠商資料提供者。
   * **[!UICONTROL Targeting Partner]**：指定公司將當作Audience Manager客戶的目標平台。
   * **[!UICONTROL Visitor ID Service]**：指定公司已啟用使用[!UICONTROL Experience Cloud Visitor ID Service]。

     [!UICONTROL Experience Cloud Visitor ID Service]提供跨Experience Cloud解決方案的通用訪客ID。 如需詳細資訊，請參閱[Experience Cloud訪客ID服務使用手冊](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en)。

   * **[!UICONTROL Agency]**：指定公司將會有[!UICONTROL Agency]帳戶。

1. 按一下&#x200B;**[!UICONTROL Create]**。 繼續執行[編輯公司設定檔](../companies/admin-manage-company-profiles.md#edit-company-profile)中的指示。

   ![步驟結果](assets/add_company.png)

## 編輯公司設定檔 {#edit-company-profile}

編輯公司的設定檔，包括其名稱、說明、子網域、生命週期等。

<!-- t_edit_company_profile.xml -->

1. 按一下&#x200B;**[!UICONTROL Companies]**，然後尋找並按一下所需的公司以顯示其[!UICONTROL Profile]頁面。

   使用[!UICONTROL Search]方塊或清單底部的分頁控制項來尋找所需的公司。 您可以按一下所需欄的標頭，以遞增或遞減順序排序每個欄。

   ![步驟結果](assets/profile_company.png)

1. 視需要編輯欄位：

   * **[!UICONTROL Name]**：編輯公司的名稱。 這是必填欄位。
   * **[!UICONTROL Description]**：編輯公司的說明。 這是必填欄位。
   * **[!UICONTROL Subdomain]**： （必要）指定公司的子網域。 您輸入的文字會顯示為事件呼叫的子網域。 無法變更此設定。 它必須是包含[!DNL URL]個有效字元的字串。

     例如，如果貴公司名為[!DNL AcmeCorp]，則子網域將是[!DNL acmecorp]。

     Audience Manager使用[!UICONTROL Data Collection Server] (DCS)的子網域。 在上一個範例中，如果貴公司在[!UICONTROL DCS]中的完整[!DNL URL]為[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**： ([!UICONTROL Identity Management System Organization ID])此ID可讓您連線公司與Adobe Experience Cloud。
   * **[!UICONTROL Lifecyle]**：指定想要的公司階段：
      * **[!UICONTROL Active]**：指定公司將會是作用中Audience Manager使用者端。 作用中帳戶表示付款客戶，不僅是為了諮詢，也是為了提供Audience ManagerSKU。
      * **[!UICONTROL Demo]**：指定公司僅供示範之用。 系統會自動偽造報表資料。
      * **[!UICONTROL Prospect]**：指定公司是潛在的Audience Manager使用者端，例如公司獲得免費的[!DNL POC]或銷售示範的帳戶設定。
      * **[!UICONTROL Test]**：指定公司僅供內部測試之用。
   * **[!UICONTROL Account Types]**：指定此公司的完整帳戶型別集。 沒有帳戶型別與任何其他型別互斥。
      * **[!UICONTROL Full AAM]**：指定公司將擁有完整的Adobe Audience Manager帳戶，且使用者將擁有登入存取權。
      * **[!UICONTROL MMP]**：指定公司已啟用使用主要行銷設定檔([!UICONTROL MMP])功能。

        如果您選取此帳戶型別，也會自動選取&#x200B;**[!UICONTROL Visitor ID Service]**。
如需詳細資訊，請參閱[Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。

   * **[!UICONTROL Data Source]**：指定公司是Audience Manager中的協力廠商資料提供者。
   * **[!UICONTROL Targeting Partner]**：指定公司將當作Audience Manager客戶的目標平台。
   * **[!UICONTROL Visitor ID Service]**：指定公司已啟用使用Experience Cloud訪客ID服務。

     Experience Cloud 訪客 ID 服務提供跨 Experience Cloud 解決方案的通用訪客 ID。如需詳細資訊，請參閱[Experience Cloud識別碼服務使用手冊](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)。

   * **[!UICONTROL Agency]**：指定公司將擁有代理帳戶。
   * **[!UICONTROL Features]**：選取所要的選項：
      * **[!UICONTROL Password Expiration]**：設定此公司內的所有使用者密碼在90天後過期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**：啟用此公司的Audience Manager報告。
      * **[!UICONTROL Role Based Access Controls]**：啟用此公司的角色型存取控制。 角色型存取控制可讓您建立具有不同存取許可權的使用者群組。 之後，這些群組內的個別使用者只能存取Audience Manager中的特定功能。

1. 按一下 **[!UICONTROL Submit Updates]**。

## 刪除公司設定檔 {#delete-company-profile}

使用Audience Manager[!UICONTROL Admin]工具中的[!UICONTROL Companies]頁面刪除現有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必須擁有[!UICONTROL DEXADMIN]角色才能刪除現有公司。

1. 若要刪除現有公司，請按一下&#x200B;**[!UICONTROL Companies]**。

   ![步驟結果](assets/companies.png)

1. 按一下所需公司&#x200B;**[!UICONTROL Actions]**&#x200B;欄中的![](assets/icon_delete.png)。
1. 按一下&#x200B;**[!UICONTROL OK]**&#x200B;以確認刪除。
