---
description: 使用Audience Manager管理工具中的「伺服器」頁面，建立新的FTP伺服器或編輯現有的伺服器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: 建立或編輯FTP伺服器
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
TQID: https://experienceleague.adobe.com/vXm5k1APT6BVn0Ub7ntfDCnAdSfOWTLRo6ci-yK5cWk
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 397
ht-degree: 1%

---

# 建立或編輯FTP伺服器 {#create-or-edit-an-ftp-server}

使用Audience Manager管理工具中的[!UICONTROL Servers]頁面來建立新的FTP伺服器或編輯現有的伺服器。

>[!NOTE]
>
>您必須擁有[!UICONTROL DEXADMIN]角色，才能建立新伺服器或編輯現有伺服器。

1. 若要建立新伺服器，請按一下&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 若要編輯現有伺服器，請在&#x200B;**[!UICONTROL Label]**&#x200B;欄中按一下所需的伺服器。
1. 指定此伺服器的所需標籤。
1. 從&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉式清單中，選取所需的通訊協定： **FTP**。

   >[!NOTE]
   >
   >作為最佳實務，建議您使用[!DNL Amazon S3]作為從合作夥伴取得檔案並將檔案傳遞給合作夥伴的方法。 [!DNL Amazon S3]提供簡易的網頁服務介面，可隨時隨地從網頁上儲存及擷取任何數量的資料。 如需詳細資訊，請參閱&#x200B;*Amazon使用手冊*&#x200B;中的[關於Audience Manager S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html?lang=zh-Hant)。

1. 填寫欄位:

   * **[!UICONTROL Type]：**&#x200B;選取所需的加密型別： **[!UICONTROL SFTP]**&#x200B;或&#x200B;**[!UICONTROL FTPs/TLS]**。
   * **[!UICONTROL Domain]：**&#x200B;指定此伺服器的所需網域（主機）。
   * **[!UICONTROL Port]：**&#x200B;指定此伺服器的所需連線埠。 預設連線埠會針對每種加密型別顯示。 您可以視需要變更預設連線埠。
   * **[!UICONTROL Remote Path]：**&#x200B;指定此伺服器的所需遠端路徑。 如果您將此欄位留空，Audience Manager會將檔案置於預設目錄中。
   * **[!UICONTROL .tmp File Rename on Completion]：**&#x200B;啟用此選項以在完成時重新命名`.tmp`檔案。
   * **[!UICONTROL Filename Suffix]：**&#x200B;指定您要附加以傳輸檔案的文字。
   * **[!UICONTROL Moved to When Finished]：**&#x200B;指定要在完成時移動傳輸檔案的位置的路徑。
   * **[!UICONTROL Authentication]：**&#x200B;指定想要的伺服器驗證方法： **[!UICONTROL Username/Password]**&#x200B;或&#x200B;**[!UICONTROL SSH Key]**。

   >[!NOTE]
   >
   >記得將我們的輸出[!DNL FTP] [!DNL IP]新增到您的允許IP清單： **54.204.116.43**。

1. 針對&#x200B;**[!UICONTROL SSH Key]**&#x200B;驗證：

   >[!NOTE]
   >
   >設定SSH金鑰驗證時，請務必只以OpenSSH格式產生公開和私密金鑰。

   1. 從任何[!DNL Linux]或[!DNL Mac]電腦產生公開/私用金鑰組。
   1. 將&#x200B;**公開金鑰**&#x200B;提供給使用者端，以便在其[!DNL SFTP]伺服器上更新。 他們必須包含其伺服器上公開金鑰的所有文字，包括`-----BEGIN RSA PRIVATE KEY-----`和`-----END RSA PRIVATE KEY-----` 。 為了交換，他們必須提供安裝金鑰所用的使用者名稱。
   1. 請以使用者端提供的使用者名稱欄位更新使用者名稱欄位，並使用&#x200B;**私密金鑰**&#x200B;更新金鑰欄位。

1. 如果您正在建立新伺服器，請按一下&#x200B;**[!UICONTROL Create]**；如果您正在編輯現有伺服器，請按一下&#x200B;**[!UICONTROL Update]**。
