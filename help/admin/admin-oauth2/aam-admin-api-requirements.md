---
description: 建議客戶在使用Audience Manager API時注意的事項。
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API需求與建議
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# API需求與建議 {#api-requirements-and-recommendations}

建議客戶在使用Audience Manager [!DNL API]時注意的事項。

## 要求 {#requirements}

使用[!DNL Audience Manager] [!DNL API]程式碼時，請注意下列事項：

* **要求引數：**&#x200B;除非另有指定，否則所有要求引數都是必要的。
* **[!DNL JSON]內容型別：**&#x200B;在您的程式碼中指定`content-type: application/json` *和* `accept: application/json`。

* **要求與回應：**&#x200B;以正確格式化的[!DNL JSON]物件傳送要求。 [!DNL Audience Manager]以[!DNL JSON]格式化的資料回應。 伺服器回應可包含要求的資料、狀態代碼或兩者。

* **存取：**&#x200B;您的[!DNL Audience Manager]顧問會提供您使用者端ID和金鑰，讓您提出[!DNL API]個請求。

* **檔案和程式碼範例：**&#x200B;斜體&#x200B;*的文字*&#x200B;代表您在製作或接收[!DNL API]資料時提供或傳入的變數。 將&#x200B;*斜體的*&#x200B;文字取代為您自己的程式碼、引數或其他必要資訊。

## Recommendations：建立一般API使用者 {#recommendations}

建議您建立個別的技術使用者帳戶，以便使用Audience Manager [!DNL API]。這是一般帳戶，不會繫結至使用者端組織中的特定使用者或與其相關聯。 此型別的[!DNL API]使用者帳戶有助於完成2件事：

* 識別呼叫[!DNL API]的服務（例如，來自使用我們[!DNL API]的使用者端應用程式或進行大量變更的呼叫）。
* 提供對[!DNL API]的不中斷存取。繫結至特定員工的帳戶可能會在員工離開公司時刪除。 這會導致您的客戶無法使用可用的[!DNL API]程式碼。 未與特定員工繫結的一般帳戶有助於避免此問題。

此帳戶型別的範例或使用案例，假設您的客戶想要使用[大量管理工具](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en)一次變更許多區段。 若要這麼做，他們需要[!DNL API]存取權。 請建立具有適當認證、金鑰和密碼的非特定[!DNL API]使用者帳戶，以進行[!DNL API]呼叫，而不新增許可權給特定使用者。 如果使用者端自行開發使用[!DNL Audience Manager] [!DNL API]的應用程式，這也很有用。
