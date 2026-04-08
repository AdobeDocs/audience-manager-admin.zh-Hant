---
description: 建立、編輯和刪除Audience Manager目的地。
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: 管理公司目的地
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
TQID: https://experienceleague.adobe.com/-MWpMACN0bFPIRAWejD0-VV5nG8BGAukmV1QXxXal-E
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2: id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 1101
ht-degree: 0%

---

# 管理公司目的地 {#manage-company-destinations}

建立、編輯和刪除Audience Manager目的地。

<!-- t_company_destinations.xml -->

如需詳細資訊，請參閱&#x200B;*Audience Manager使用手冊*&#x200B;中的[目的地](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html)。

## 建立或編輯公司目的地 {#create-edit-company-destinations}

請捲動各節，以取得如何建立新[!DNL Audience Manager]目的地或編輯現有目的地的逐步指示。

<!-- create-edit-company-destinations.xml -->

請先造訪[Experience Cloud合作夥伴整合頁面](https://wiki.corp.adobe.com/x/mPIMPw)，再設定目的地。 此頁面包含您需要為每個[!DNL Audience Manager]合作夥伴整合填寫的特定資訊。

如果您的使用者端想要使用[!DNL Adobe Media Optimizer]作為[!DNL Audience Manager]中的目的地，您需要在[!DNL Adobe Media Optimizer]中設定此專案。

## 導覽至「目的地」標籤 {#navigate-destinations}

1. 按一下&#x200B;**[!UICONTROL Companies]**，然後尋找並按一下所需的公司以顯示其[!UICONTROL Profile]頁面。 您可以使用[!UICONTROL Search]方塊或清單底部的分頁控制項來尋找所需的公司。 您可以按一下所需欄的標頭，以遞增或遞減順序排序每個欄。
1. 按一下「**[!UICONTROL Destinations]**」標籤。
1. 若要建立新的目的地，請按一下&#x200B;**[!UICONTROL Add Destination]**。 若要編輯現有的目的地，請在&#x200B;**[!UICONTROL Name]**&#x200B;欄中按一下目的地的名稱。

## 基本設定 {#basic-settings}

填寫&#x200B;**[!UICONTROL Basic Settings]**&#x200B;視窗中的欄位。

* **[!UICONTROL Name]：** （必要）指定此目的地的名稱。
* **[!UICONTROL Description]：**&#x200B;指定此目的地的描述性資訊。
* **[!UICONTROL Type]：** （必要）選取所要的目的地型別：
   * **[!UICONTROL Bulk ID]**：在不同平台之間同步識別碼。
   * **[!UICONTROL Bulk Trait]**：將特徵資訊大量傳送至不同平台。
   * **[!UICONTROL Bulk Segment]**：將區段資訊大量傳送至不同的平台。
   * **[!UICONTROL S2S]**：使用伺服器對伺服器目的地，將即時和批次資料傳送至不同的平台。
* **[!UICONTROL Auto-Fill Destination Mapping]：** （僅限[!UICONTROL S2S]）選取選項：
   * **[!UICONTROL Segment ID]：**&#x200B;若您選取此設定，則目的地值對應會填入[!DNL Audience Manager]區段識別碼。
   * **[!UICONTROL Integration Code Value]：**&#x200B;如果您選取此設定，則目的地值對應會填入[!DNL Audience Manager]區段整合代碼。
* **[!UICONTROL User ID Key]：** （必要）從下拉式清單中選取此目的地的所需使用者ID金鑰。

此ID會當作主要資料來源ID使用。 這會決定要在檔案中退出的使用者ID。

>[!NOTE]
>
>對於[!UICONTROL Bulk ID]目的地型別，您無法使用[!DNL Audience Manager] [!UICONTROL User ID]或[!DNL Adobe Experience Cloud] ID。

如果您的資料來源識別碼([!UICONTROL DPID])未顯示在下拉式清單中，您必須在[資料Source設定頁面](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html)上的資料來源層級選取&#x200B;**[!UICONTROL Outbound]**&#x200B;核取方塊。

* **[!UICONTROL Target Data Source]：** （必要）從下拉式清單中選取此目的地的所需資料來源。 此設定可啟用出站資料的標籤，以允許擷取到使用者端上的個別系統中。
* **[!UICONTROL Foreign Account ID]：**&#x200B;指定此目的地的外部帳戶識別碼。 這是收件者系統中此出站資料的識別值。
* **[!UICONTROL Outbound Sample Rate Denominator]：**&#x200B;當傳回資料的總量未知時，使用此設定可只傳回範例數量的資料，而非完整數量。 在此調整數字以代表資料的一小部分（例如，「100」的值傳回一般資料量的1/100，「10」的值傳回一般資料量的1/10）。 預設值為「1」，會傳回所有資料。

## 即時資料（適用於S2S目的地） {#realtime-s2s}

如果您正在建立[!UICONTROL S2S]目的地，請填寫下列欄位：

**[!UICONTROL Servers]**：為此目的地選取所需的`HTTP`伺服器。
**[!UICONTROL Format]**：從下拉式清單中選取此目的地的所需格式： [!UICONTROL HTTP only]。

>[!NOTE]
>
>僅適用於[!DNL S2S]，您可以使用熒幕上的「關閉/開啟」滑桿來啟用或停用[!UICONTROL Realtime]或[!UICONTROL Batch]目的地。 您無法同時停用這兩個選項。

## 批次資料 {#batch-data}

若為[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目的地，請填寫下列欄位：

* **[!UICONTROL Protocol]**： （必要）從下拉式清單中選取此目的地的所需通訊協定：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**： （必要）從下拉式清單中選取此目的地的所需伺服器。
* **[!UICONTROL Format]**： （必要）從下拉式清單中選取此目的地的所需格式： [!DNL HTTP]或檔案型別（視您在上面選擇的通訊協定而定）。
* **[!UICONTROL Sync Type]**： （必要）為此目的地選取所需的同步型別。 這表示使用者端要包含在傳出訂單中的使用者活動等級。 如果使用者端只想從其屬性分析區段資格，請選取&#x200B;**[!UICONTROL Customer]**。 如果他們想要包含來自所有[!DNL Audience Manager]客戶的站外活動的區段資格，請選取&#x200B;**[!UICONTROL Platform]**。
* **[!UICONTROL Customer]**：檔案包含在所選時段內在使用者端的屬性（與使用者端的[!UICONTROL PID]關聯）上至少具有1個特徵實現的作用中使用者。 您的使用者端應使用此選項將其&#x200B;*即時*&#x200B;區段資格輸出至目的地。
* **[!UICONTROL Platform]**：檔案包含在所選時段內，所有[!DNL Audience Manager]使用者端屬性（與所有使用者端PID相關聯）中任何位置具有至少1個即時互動的使用者，無論是ID同步還是特徵實現。 您的使用者端應使用此選項將其&#x200B;*總計*&#x200B;個區段資格輸出至目的地。
* **[!UICONTROL Lifetime]**：檔案包含自建立目的地後，在所有[!DNL Audience Manager]使用者端屬性中可看見的使用中使用者。
* **[!UICONTROL Sync Type Lookback Period]**：如果您選取[!UICONTROL Customer]或[!UICONTROL Platform]，請選取時段。 檔案包含所選時段的作用中使用者。
接著，選取訂單型別。 這表示與合作夥伴的每次對外整合的頻率和範圍。 選取增量訂單與完整訂單。
* **[!UICONTROL Incremental Scheduled Run]**：在每次執行中，[!DNL Audience Manager]將只會輸出自前次輸出訂單以來符合資格的淨新使用者。 選取您要[!DNL Audience Manager]執行增量同步處理程式的所需時段。 例如，您可以選取每24小時、每7天、每30天或從不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一個遞增訂單等於完整訂單，因為之前沒有任何使用者傳送至目的地。

* **[!UICONTROL Full Sync Scheduled Run]**：每次執行時，[!DNL Audience Manager]都會輸出目的地初次設定後所有作用中的使用者。 選取您要[!DNL Audience Manager]用來執行完整同步處理程式的所需排程。 例如，您可以選取每24小時、每7天、每30天或從不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>我們建議使用增量同步比完整同步更頻繁。 增量同步只會傳送包含新特徵實現或ID同步的檔案。 完整同步會傳送所有檔案，無論檔案是否包含新的實現或ID同步。 當使用者端需要其所有使用者的完整復本時，請只使用[!UICONTROL Full Sync Scheduled Run]設定，以減少輸出資料量。

## 設定資料來源 {#configure-data-sources}

若為[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目的地，請填寫下列欄位。 這些設定可讓您傳送與資料來源相關聯的所有資料(特徵、區段或ID （根據選取的型別）)。

* **[!UICONTROL All Unrestricted First Party Data]**：選取以使用所有第一方資料來源。 如果選取此選項，則會停用[!UICONTROL Available Data Sources]選項。
* **[!UICONTROL Available Data Sources]**：使用箭頭在&#x200B;**[!UICONTROL Available Data Sources]**&#x200B;和&#x200B;**[!UICONTROL In File Data Sources]**&#x200B;方塊之間行動資料來源。

## 儲存並完成 {#save-and-finalize}

填寫完所有必填欄位後，**[!UICONTROL Save]**&#x200B;按鈕就會啟動。 按一下&#x200B;**[!UICONTROL Save]**&#x200B;完成建立目的地程式。

## 刪除公司目的地 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

若要刪除目的地：

1. 按一下「**[!UICONTROL Companies]**」，尋找並按一下所需的公司，然後按一下「**[!UICONTROL Destinations]**」標籤。
1. 按一下所需目的地&#x200B;**[!UICONTROL Actions]**&#x200B;欄中的![](assets/icon_delete.png)。
1. 按一下&#x200B;**[!UICONTROL OK]**&#x200B;以確認刪除。

>[!NOTE]
>
>如果目的地有對應的區段，您無法刪除目的地。
