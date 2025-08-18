---
description: 依預設，所有公司都會與Adobe Media Optimizer (AMO)同步資料。 在管理UI中，每個公司容器都有一個資料來源來管理此程式。 此資料來源為Adobe AMO (ID 411)。 按一下所選公司的容器列（在「容器」標籤下），以停用此預設同步作業，或將其他資料來源新增至AMO同步作業程式，或從中移除資料來源。
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: ID與Media Optimizer同步
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 2%

---

# ID與Media Optimizer同步 {#id-syncing-with-media-optimizer}

依預設，所有公司都會與[!DNL Adobe Media Optimizer] ([!DNL AMO])同步資料。 在[!UICONTROL Admin UI]中，每個公司容器都有管理此程式的資料來源。 此資料來源為[!UICONTROL Adobe AMO] ([!UICONTROL ID] 411)。 按一下所選公司的容器列（[!UICONTROL Containers]標籤下），以停用此預設同步處理或新增及移除其他資料來源至[!DNL AMO]同步處理序。

![](assets/id-sync.png)

## ID同步狀態 {#id-sync-status}

下表說明資料來源的同步狀態。

| 狀態 | 說明 |
|------ | -------- |
| 關閉 | 從[!UICONTROL Selected Data Sources]中移除此容器的所有資料來源，以停用與[!DNL AMO]的ID同步 |
| 開啟（不論ID服務版本為何） | 資料來源會在下列情況與[!DNL AMO]同步（無論ID服務版本為何）： <ul><li>資料來源會顯示在[!UICONTROL Selected Data Sources]清單中。</li><li>[!DNL AMO]核取方塊&#x200B;*未選取*。</li></ul> |
| 開啟（不論ID服務版本為何） | 資料來源會在下列情況下與ID服務版本2.0 （或更新版本）的[!DNL AMO]同步： <ul><li>資料來源會顯示在[!UICONTROL Selected Data Sources]清單中。</li><li>[!DNL AMO]核取方塊&#x200B;*已選取*。</li></ul> |

>[!MORELIKETHIS]
>
>* [管理容器](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)
