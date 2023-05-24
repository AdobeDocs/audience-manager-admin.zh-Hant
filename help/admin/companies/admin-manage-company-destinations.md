---
description: 建立、編輯和刪除Audience Manager目的地。
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: 管理公司目的地
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# 管理公司目的地 {#manage-company-destinations}

建立、編輯和刪除Audience Manager目的地。

<!-- t_company_destinations.xml -->

如需詳細資訊，請參閱 [目的地](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) 在 *Audience Manager使用手冊*.

## 建立或編輯公司目的地 {#create-edit-company-destinations}

捲動各節，取得如何建立新專案的逐步指示 [!DNL Audience Manager] 目的地或編輯現有的目的地。

<!-- create-edit-company-destinations.xml -->

造訪 [Experience Cloud合作夥伴整合頁面](https://wiki.corp.adobe.com/x/mPIMPw) 之後再設定目的地。 此頁面包含您需要為每個欄位填寫的特定資訊 [!DNL Audience Manager] 合作夥伴整合。

如果您的使用者端想要使用 [!DNL Adobe Media Optimizer] 作為中的目的地 [!DNL Audience Manager] ，您必須在「 」中設定此專案 [!DNL Adobe Media Optimizer].

## 導覽至「目的地」標籤 {#navigate-destinations}

1. 按一下 **[!UICONTROL Companies]**，然後找到並按一下所需的公司以顯示其 [!UICONTROL Profile] 頁面。 您可以使用 [!UICONTROL Search] 方塊或清單底部的分頁控制項，以尋找所需的公司。 您可以按一下所需欄的標頭，以遞增或遞減順序排序每個欄。
1. 按一下 **[!UICONTROL Destinations]** 標籤。
1. 若要建立新目的地，請按一下 **[!UICONTROL Add Destination]**. 若要編輯現有目的地，請在 **[!UICONTROL Name]** 欄。

## 基本設定 {#basic-settings}

填寫欄位 **[!UICONTROL Basic Settings]** 視窗。

* **[!UICONTROL Name]：** （必要）指定此目的地的名稱。
* **[!UICONTROL Description]：** 指定此目的地的描述性資訊。
* **[!UICONTROL Type]：** （必要）選取所需的目的地型別：
   * **[!UICONTROL Bulk ID]**：在不同平台之間同步ID。
   * **[!UICONTROL Bulk Trait]**：大量傳送特徵資訊至不同平台。
   * **[!UICONTROL Bulk Segment]**：大量傳送區段資訊至不同平台。
   * **[!UICONTROL S2S]**：使用伺服器對伺服器目的地，將即時和批次資料傳送至不同平台。
* **[!UICONTROL Auto-Fill Destination Mapping]：** ( [!UICONTROL S2S] 僅限)選取一個選項：
   * **[!UICONTROL Segment ID]：** 如果您選取此設定，則目的地值對應會填入 [!DNL Audience Manager] 區段ID。
   * **[!UICONTROL Integration Code Value]：** 如果您選取此設定，則目的地值對應會填入 [!DNL Audience Manager] 區段整合代碼。
* **[!UICONTROL User ID Key]：** （必要）從下拉式清單中為此目的地選取所需的使用者ID金鑰。

此ID會作為主要資料來源ID使用。 這會決定要在檔案中展開的使用者ID。

>[!NOTE]
>
>對於 [!UICONTROL Bulk ID] 目的地型別，則無法使用 [!DNL Audience Manager] [!UICONTROL User ID] 或 [!DNL Adobe Experience Cloud] ID。

如果您的資料來源ID ( [!UICONTROL DPID])不會顯示在下拉式清單中，您必須選取 **[!UICONTROL Outbound]** 上的資料來源層級核取方塊 [資料來源設定值頁面](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]：** （必要）從下拉式清單中為此目的地選取所需的資料來源。 此設定可啟用出站資料的標籤，允許將資料擷取到使用者端的個別系統中。
* **[!UICONTROL Foreign Account ID]：** 指定此目的地的外部帳戶ID。 這是收件者系統中此出站資料的識別值。
* **[!UICONTROL Outbound Sample Rate Denominator]：** 當傳回資料的總量不明時，請使用此設定來只傳回範例數量的資料，而非全部數量。 在此調整數字可代表資料的一小部分（例如，「100」值會傳回一般資料量的1/100，「10」值會傳回一般資料量的1/10）。 預設值為「1」，會傳回所有資料。

## 即時資料（適用於S2S目的地） {#realtime-s2s}

如果您要建立 [!UICONTROL S2S] 目的地，請填寫下列欄位：

**[!UICONTROL Servers]**：選取所需的 `HTTP` 此目的地的伺服器。
**[!UICONTROL Format]**：從下拉式清單中為此目的地選取所需的格式： [!UICONTROL HTTP only].

>[!NOTE]
>
>對象 [!DNL S2S] 您只能啟用或停用 [!UICONTROL Realtime] 或 [!UICONTROL Batch] 目的地使用熒幕關閉/開啟滑桿。 您無法同時停用這兩個選項。

## 批次資料 {#batch-data}

對象 [!UICONTROL Bulk ID]， [!UICONTROL Bulk Trait] 或 [!UICONTROL Bulk Segment] 目的地，請填寫下列欄位：

* **[!UICONTROL Protocol]**：（必要）從下拉式清單中為此目的地選取所需的通訊協定：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**：（必要）從下拉式清單中為此目的地選取所需的伺服器。
* **[!UICONTROL Format]**：（必要）從下拉式清單中為此目的地選取所需的格式： [!DNL HTTP] 或檔案型別，視您在上面選擇的通訊協定而定。
* **[!UICONTROL Sync Type]**：（必要）為此目的地選取所需的同步型別。 這表示使用者端要包含在出站訂單中的使用者活動等級。 選取 **[!UICONTROL Customer]** 如果客戶只想根據其屬性分析區段資格。 選取 **[!UICONTROL Platform]** 如果他們想要包含所有場外活動的區段資格 [!DNL Audience Manager] 客戶。
* **[!UICONTROL Customer]**：檔案包含僅在使用者端的屬性上具有至少1個特徵實現的活躍使用者（與使用者端的屬性相關聯） [!UICONTROL PID])。 您的使用者端應使用此選項來輸出其 *即時* 目的地的區段資格。
* **[!UICONTROL Platform]**：檔案包含的使用者至少擁有1個即時互動（不論是ID同步或特徵實現），且橫跨所有位置 [!DNL Audience Manager] 所選時段內的使用者端屬性（與所有使用者端PID相關聯）。 您的使用者端應使用此選項來輸出其 *總計* 目的地的區段資格。
* **[!UICONTROL Lifetime]**：檔案包含所有使用者中任何位置都可看到的作用中使用者 [!DNL Audience Manager] 自建立目的地以來的使用者端屬性。
* **[!UICONTROL Sync Type Lookback Period]**：如果您選取 [!UICONTROL Customer] 或 [!UICONTROL Platform]，選取時段。 檔案包含所選時段的作用中使用者。
接著，選取訂單型別。 這表示與合作夥伴的每次對外整合的頻率和範圍。 選取增量訂單與完整訂單。
* **[!UICONTROL Incremental Scheduled Run]**：每次執行時， [!DNL Audience Manager] 僅會傳出自上次傳出訂單以來符合資格的淨新使用者。 選取您想要的時間段 [!DNL Audience Manager] 執行增量同步化處理。 例如，您可以選取每24小時、每7天、每30天或從不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一個累加訂單等於完整訂單，因為先前沒有任何使用者傳送至目的地。

* **[!UICONTROL Full Sync Scheduled Run]**：每次執行時， [!DNL Audience Manager] 將輸出自第一次設定目的地以來的所有作用中使用者。 選取所需的排程 [!DNL Audience Manager] 以用來執行完整同步處理作業。 例如，您可以選取每24小時、每7天、每30天或從不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>我們建議使用增量同步的頻率高於完整同步。 增量同步只會傳送包含新特徵實現或ID同步的檔案。 完整同步會傳送所有檔案，無論檔案是否包含新的實現或ID同步。 僅使用 [!UICONTROL Full Sync Scheduled Run] 設定使用者端需要其所有使用者的完整復本，以減少傳出資料量。

## 設定資料來源 {#configure-data-sources}

對象 [!UICONTROL Bulk ID]， [!UICONTROL Bulk Trait] 或 [!UICONTROL Bulk Segment] 目的地，請填寫下列欄位。 這些設定可讓您傳送與資料來源相關聯的所有資料(特徵、區段或ID （根據選取的型別）)。

* **[!UICONTROL All Unrestricted First Party Data]**：選取以使用所有第一方資料來源。 如果您選取此選項， [!UICONTROL Available Data Sources] 選項已停用。
* **[!UICONTROL Available Data Sources]**：使用箭頭在 **[!UICONTROL Available Data Sources]** 和 **[!UICONTROL In File Data Sources]** 方塊。

## 儲存並完成 {#save-and-finalize}

此 **[!UICONTROL Save]** 填寫完所有必填欄位後，按鈕即會啟用。 按一下 **[!UICONTROL Save]** 以完成建立目的地程式。

## 刪除公司目的地 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

若要刪除目的地，請執行下列動作：

1. 按一下 **[!UICONTROL Companies]**，找到並按一下所需的公司，然後按一下 **[!UICONTROL Destinations]** 標籤。
1. 按一下  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 欄中的所需目的地。
1. 按一下 **[!UICONTROL OK]** 以確認刪除。

>[!NOTE]
>
>如果目的地有對應的區段，則無法刪除目的地。
