---
description: 請依照這些指示來產生僅包含最近使用中之使用者的完整同步檔案。 您可以篩選作用中的使用者，以推送相關資料至網站上的鎖定目標系統，或限制傳送至DSP的檔案大小。 您無法將此篩選器用於增量同步處理。
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: 僅依活躍使用者篩選傳出資料
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
TQID: https://experienceleague.adobe.com/rr6ABB4pgrhkWG88VenqIcbyAaPQfbg258M6SVdE28k
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# 僅依活躍使用者篩選傳出資料 {#filter-outbound-data-by-active-users-only}

請依照這些指示來產生僅包含最近使用中之使用者的完整同步檔案。 您可以篩選作用中的使用者，以推送相關資料至網站上的鎖定目標系統，或限制傳送至DSP的檔案大小。 您無法將此篩選器用於增量同步處理。

>[!NOTE]
>
>訪客不需要出現在選取的客戶網站或其廣告流量中，即可符合「作用中」資格。 任何[!DNL Audience Manager]客戶或合作夥伴都可以看見這些事件，以符合「作用中」資格。

僅依作用中使用者篩選：

1. 按一下 **[!UICONTROL Companies]**。
1. 選取您要使用的公司，然後按一下&#x200B;**[!UICONTROL Destinations]**。
1. 在[!UICONTROL Batch Data]區段中，設定下列選項：

   * **[!UICONTROL Sync Type]**：選取&#x200B;**[!UICONTROL Customer]**&#x200B;或&#x200B;**[!UICONTROL Platform]**。
   * **[!UICONTROL Sync Type Lookback Period]**：這個時間間隔定義了資料檔的範圍。 選項包括&#x200B;**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**、**[!UICONTROL 30 days]**。
   * **[!UICONTROL Incremental Sync Scheduled Run]**：選取&#x200B;**[!UICONTROL Never]**。 請記住，此篩選器僅適用於完整同步檔案。
   * **[!UICONTROL Full Sync Scheduled Run]**：這會決定您接收此檔案的頻率。 選項包括&#x200B;**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**、**[!UICONTROL 30 days]**&#x200B;或&#x200B;**[!UICONTROL Never]** （要停用）。

1. 按一下 **[!UICONTROL Save]**。
