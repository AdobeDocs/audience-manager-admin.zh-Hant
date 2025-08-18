---
description: 為了防止檔案和資料意外上線至其他合作夥伴或客戶擁有的目標資料來源，Audience Manager在合作夥伴ID (PID)與其他合作夥伴擁有的資料來源之間新增對應需求。
title: 管理第二方資料的上線存取
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# 管理第二方資料的上線存取 {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> 此頁面的對象是Adobe內部員工。 如果您是Audience Manager客戶，要求本頁所述的第二方資料來源對應，請聯絡客戶服務或您的技術客戶經理。
> > 請注意，不需要請求現有資料共用關係的對應。 將資料上線至屬於您的PID的目標資料來源時，也不一定需要對應。

為了防止檔案和資料意外上線至其他合作夥伴擁有的目標資料來源，Audience Manager在合作夥伴ID (PID)與其他合作夥伴擁有的資料來源(DPID)之間新增對應需求。 深入瞭解Audience Manager ID[的](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html)索引中的PID與DPID。

基於第二方資料共用目的，如果Audience Manager合作夥伴或客戶想要將檔案擷取至他們未擁有的目標資料來源，則他們需要請求合作夥伴ID (PID)與該特定資料來源(DPID)之間的對應。 如果缺少對應，傳入資料工作將不會處理檔案，且資料不會上架到Audience Manager中。

若要建立該對應，請向Audience Manager工程團隊提交Jira票證。 在[這裡](https://jira.corp.adobe.com/browse/AAM-60353)檢視範例Jira票證。 您不需要請求為任何現有資料共用關係建立對應。
