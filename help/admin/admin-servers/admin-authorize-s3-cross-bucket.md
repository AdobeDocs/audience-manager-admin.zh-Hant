---
description: 有些客戶可能不想提供其Amazon Simple Storage Service (Amazon S3)存取權或Adobe的秘密金鑰，以授權將目的地資料上傳至其貯體。
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: 如何授權批次目標的跨帳戶Amazon S3儲存貯體存取
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
TQID: https://experienceleague.adobe.com/KFc06xetyatq5n-F8Uu-6nmepyjbFyQ3nYB-vXkdPdE
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 0%

---

# 如何授權批次目標的跨帳戶Amazon S3儲存貯體存取{#authorize-cross-account-bucket-batch}

有些客戶可能不想提供他們的[!DNL Amazon S3]存取權或秘密金鑰給Adobe，以授權將目的地資料上傳至其貯體。

我們可以提供給客戶的替代方案是[!DNL Amazon S3]中的[!UICONTROL Cross-Account Bucket Permissions]。 此程式在[AWS檔案](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)中說明。 若要在Audience Manager中啟用此替代方案，請遵循下列步驟：

1. 移至&#x200B;**[!UICONTROL Servers]**&#x200B;並選取&#x200B;**[!UICONTROL Create Server]**。
1. 在&#x200B;**[!UICONTROL Protocol/Credentials]**&#x200B;下拉式遮罩中選取&#x200B;**[!UICONTROL S3]**。
1. 核取&#x200B;**[!UICONTROL Use Internal Adobe Key]**&#x200B;選項。
1. 在[!DNL Amazon S3]中使用您客戶的帳戶和貯體名稱。
1. 請確定您的客戶白名單中[!DNL S3]儲存貯體上的[!DNL Amazon S3]帳戶`975822914085`。

>[!NOTE]
>
>我們的傳出發佈者會確保已針對上傳的資料設定許可權層級`bucket-owner-full-control`，讓您的客戶可以擁有該資料。
