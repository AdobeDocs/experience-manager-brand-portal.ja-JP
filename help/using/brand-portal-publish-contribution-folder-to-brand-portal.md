---
title: Experience Manager Assets での投稿フォルダーの設定と Brand Portal への公開
description: Experience Manager Assets での投稿フォルダーの設定と Brand Portal への公開について説明します。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
exl-id: 9acad588-977a-45de-b544-f2cc8874ba12
TQID: https://experienceleague.adobe.com/o--c7CzIqcaLPuOVG81dQpALRa0wxI-Aul6F-pN-spI
product_v2:
  - id: d09181b5-a36a-43de-ba01-36641440bc43
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e48edcb1ed5d76686794f7a7ed6389c7f4ab1ed3
workflow-type: tm+mt
source-wordcount: 1063
ht-degree: 59%

---

# Experience Manager Assets での投稿フォルダーの設定 {#configure-contribution-folder}

共同作業アセットの取得を行う場合、Experience Manager Assets ユーザー（管理者および権限を持つ管理者以外のユーザー）は、**Asset Contribution** タイプのフォルダーを作成できます。作成したフォルダーは、Brand Portal ユーザーがアセットを送信するために開かれます。  このメソッドは、新しく作成された&#x200B;**貢献度** フォルダー内に&#x200B;**SHARED**&#x200B;と&#x200B;**NEW**&#x200B;という2つのサブフォルダーを作成するワークフローを自動的にトリガーします。

Experience Manager Assets ユーザーは、投稿フォルダーに追加する必要のあるアセットの種類に関する概要をアップロードすることで、アセット要件を定義します。 また、SHARED フォルダーに一連のベースラインアセットをアップロードして、Brand Portalのユーザーが必要な情報を確実に入手できるようにします。 その後、管理者は、アクティブな Brand Portal ユーザーに投稿フォルダーへのアクセスを許可してから、新しく作成した投稿フォルダーを Brand Portal に公開することができます。

次のビデオでは、Experience Manager Assetsで投稿フォルダーを設定する方法を示します。

>[!VIDEO](https://video.tv.adobe.com/v/30547)

Experience Manager Assets ユーザーは、投稿フォルダーを設定する際に、次のアクティビティを実行します。

* [投稿フォルダーを作成](#create-contribution-folder)
* [アセット要件のアップロードと投稿者の割り当て](#configure-contribution-folder-properties)
* [ベースラインアセットのアップロード](#uplad-new-assets-to-contribution-folder)
* [Experience Manager Assets から Brand Portal への投稿フォルダーの公開](#publish-contribution-folder-to-brand-portal)

## 投稿フォルダーの作成 {#create-contribution-folder}

新しいフォルダーを作成する権限を持つExperience Manager Assets管理者と管理者以外のユーザーは、Experience Manager Assetsで投稿フォルダーを作成できます。
投稿フォルダーを作成するには、「アセット投稿」タイプのフォルダーを作成し、作成したフォルダーがBrand Portal ユーザーによるアセット送信に対して開かれるようにします。 これにより、投稿フォルダー内にSHAREDとNEWという2つのサブフォルダーが自動的にトリガーされます。

>[!NOTE]
>
>管理者は、1 つのフォルダー内に複数のアセット投稿フォルダーを作成できます。
>
>アセット投稿フォルダーには、アセットの配布と投稿をおこなうための NEW フォルダーと SHARED フォルダーが含まれます。 アセットフォルダーや投稿フォルダーは、投稿フォルダー内に作成しないでください。


投稿フォルダーの作成時だけでなく、個別に投稿フォルダーのプロパティを設定することもできます。 この例では、プロパティは個別に設定されています。

**投稿フォルダーを作成するには：**

1. Experience Manager Assets インスタンスにログインします。

1. **[!UICONTROL Assets]**／**[!UICONTROL ファイル]**&#x200B;に移動します。 Experience Manager Assets リポジトリに既に存在するすべてのフォルダーが一覧表示されます。

1. 「**[!UICONTROL 作成]**」をクリックして、新規フォルダーを作成します。 「**[!UICONTROL フォルダーを作成]**」ダイアログが開きます。

1. フォルダーの&#x200B;**[!UICONTROL タイトル]**&#x200B;と&#x200B;**[!UICONTROL 名前]**&#x200B;を入力し、**[!UICONTROL アセット貢献度]** チェックボックスを選択します。
Adobeでは、フォルダーに名前を付けるスペースなしで小文字を使用することをお勧めします。

1. 「**[!UICONTROL 作成]**」をクリックします。 Experience Manager Assets リポジトリに、投稿フォルダーがリストされます。

   >[!NOTE]
   >
   > * 空のフォルダーはBrand PortalからAEMに公開できないため、ソーシングフォルダーは空にできず、少なくとも1つのアセットを含める必要があります。
   > * 管理者以外のユーザーは、アセット投稿フォルダーを作成および共有できますが、変更または削除することはできません。


   ![](assets/create-contribution-folder.png)

1. 投稿フォルダーを開きます。 投稿フォルダー内に自動的に作成される2つのサブフォルダー（**[!UICONTROL SHARED]**&#x200B;と&#x200B;**[!UICONTROL NEW]**）が表示されます。

   ![](assets/contribution-folder.png)


## 投稿フォルダーのプロパティの設定 {#configure-contribution-folder-properties}

Experience Manager Assets 管理者は、投稿フォルダーのプロパティを設定する際に、次のアクティビティを実行します。

* **説明を追加**：投稿フォルダーの大まかな説明を提供します。
* **概要をアップロード**: アセットに関連する情報を含むアセット要件ドキュメントをアップロードします。
* **投稿者を追加**：Brand Portal ユーザーを追加し投稿フォルダーへのアクセス権を付与します。

アセット要件は、管理者によって提供された詳細を参照して、投稿者（Brand Portal ユーザー）が投稿フォルダーのニーズおよび要件を理解できるようにします。 管理者は、目的、画像タイプ、最大サイズなど、投稿フォルダーのアセットのタイプを詳しく説明したアセット要件ドキュメントをアップロードします。

**投稿フォルダーのプロパティを設定するには：**

1. Experience Manager Assets インスタンスにログインします。

1. **[!UICONTROL Assets／ファイル]**&#x200B;に移動して、投稿フォルダーを探します。
1. 投稿フォルダーを選択し、「**[!UICONTROL プロパティ]**」をクリックしてフォルダーのプロパティウィンドウを開きます。

   ![](assets/properties.png)

   ![](assets/contribution-folder-property1.png)

1. 「**[!UICONTROL アセット貢献度]**」タブに移動します。
1. 投稿フォルダーの上位レベル **[!UICONTROL 説明]**&#x200B;を入力します。
1. **[!UICONTROL 概要をアップロード]**&#x200B;をクリックし、ローカルマシンから参照して&#x200B;**アセット要件ドキュメント**&#x200B;をアップロードします。

   ![](assets/upload.png)

1. 「**[!UICONTROL ユーザーを追加]**」フィールドで、投稿フォルダーの共有相手となる Brand Portal ユーザーを追加します。 これらのユーザーは、Brand Portal インターフェイスを使用して、投稿フォルダーにアクセスし、コンテンツをアップロードできます。
1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/contribution-folder-property3.png)

>[!NOTE]
>
>検索結果は、Experience Manager Assets に設定された Brand Portal ユーザーリストに基づきます。 Brand Portal ユーザーリストを更新しておくようにします。

管理者は、[!DNL Admin Console] から `user.csv` ファイルをダウンロードして、Brand Portal ユーザーを追加する際の基本テンプレートとして使用できます。 「[!UICONTROL ユーザー]」に移動し、「[!UICONTROL ユーザーリストを CSV に書き出す]」オプションをクリックして `users.csv` ファイルをダウンロードします。 次のサンプルユーザーは、ユーザーの追加に必要な属性の詳細をリストします。 ユーザーエントリに必須の属性は`Email` で、その他の属性はすべてオプションです。

[ファイルを入手](assets/users.csv)

## 投稿フォルダーへのアセットのアップロード {#uplad-new-assets-to-contribution-folder}

Experience Manager Assets ユーザーが一連のベースラインアセットを&#x200B;**SHARED** フォルダーにアップロードして、Brand Portal ユーザーが必要な情報を確実に入手できるようにします。

**ベースラインアセットをアップロードするには：**

1. Experience Manager Assets インスタンスにログインします。

1. **[!UICONTROL Assets／ファイル]**&#x200B;に移動して、投稿フォルダーを探します。

1. 投稿フォルダーを選択し、クリックして開きます。

1. **[!UICONTROL NEW]** フォルダーをクリックします。

   ![](assets/upload-new-assets1.png)

1. **[!UICONTROL 作成]**／**[!UICONTROL ファイル]**&#x200B;をクリックして、複数のアセットを含む個別のファイルまたはフォルダー（.zip）をアップロードします。

   ![](assets/upload-new-assets2.png)

1. アセット（ファイルまたはフォルダー）を参照し、**[!UICONTROL NEW]** フォルダーへとアップロードします。

   ![](assets/upload-asset4.png)

すべてのアセットまたはフォルダーを NEW フォルダーにアップロードしたら、投稿フォルダーを Experience Manager Assets に公開します。


## Brand Portal への投稿フォルダーの公開 {#publish-contribution-folder-to-brand-portal}

投稿フォルダーが設定されると、Experience Manager Assets ユーザー（管理者／管理者以外のユーザー）は、Experience Manager Assets から Brand Portal に投稿フォルダーを公開できます。 投稿フォルダーにアクセスする権限を持つBrand Portal ユーザーは、公開アクションの完了時にメールまたはパルス通知を受け取ります。


**投稿フォルダーを公開するには：**

1. Experience Manager Assets インスタンスにログインします。

1. **[!UICONTROL Assets／ファイル]**&#x200B;に移動して、Brand Portal に公開する投稿フォルダーを探します。
1. 投稿フォルダーを選択し、**[!UICONTROL クイック公開]**/**[!UICONTROL Brand Portalに公開]**&#x200B;をクリックします。

   ![](assets/publish-contribution-folder-to-bp.png)

   投稿フォルダーがBrand Portalに公開されると、成功メッセージが表示されます。

投稿フォルダーに割り当てられた Brand Portal ユーザーにメール／パルス通知が送信されます。 Brand Portal ユーザーは、投稿フォルダーにアクセスして投稿を開始できます。 詳しくは、[Brand Portal での投稿フォルダーへのアセットのアップロードと Experience Manager Assets への投稿フォルダーの公開](brand-portal-publish-contribution-folder-to-aem-assets.md)を参照してください。
