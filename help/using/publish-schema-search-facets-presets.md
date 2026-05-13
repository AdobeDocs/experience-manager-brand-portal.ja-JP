---
title: Brand Portal へのプリセット、スキーマ、ファセットの公開
description: プリセット、スキーマ、ファセットを Brand Portal に公開する方法を説明します。
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
exl-id: 9b585606-6538-459b-87a9-2e68df0087b3
TQID: https://experienceleague.adobe.com/M2TJ3UdBegFbtGRdzdqrPDXMovdtf0BcPoY3FVNoQSw
product_v2: id: d09181b5-a36a-43de-ba01-36641440bc43id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: bd0d2470-932c-4269-8eca-6d939b72d9ef
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: e48edcb1ed5d76686794f7a7ed6389c7f4ab1ed3
workflow-type: tm+mt
source-wordcount: 1131
ht-degree: 44%

---

# Brand Portal へのプリセット、スキーマ、ファセットの公開 {#publish-presets-schema-and-facets-to-brand-portal}

この記事では、画像プリセット、メタデータスキーマおよびカスタム検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開する方法について説明します。 公開機能を使用すると、AEM オーサーインスタンスで作成または編集された画像プリセット、メタデータスキーマ、検索ファセットを再利用できます。 これにより、重複する作業を減らすことができます。

>[!NOTE]
>
>画像プリセット、メタデータスキーマ、検索ファセットをAEM オーサーインスタンスからBrand Portalに公開する機能は、AEM 6.2 SP1-CFP7およびAEM 6.3 SP 1-CFP 1 （6.3.1.1）以降で利用できます。

## Brand Portal への画像プリセットの公開 {#publish-image-presets-to-brand-portal}

画像プリセットとは、画像配信の際に画像に適用される一連のサイズ変更コマンドやフォーマットコマンドをまとめたものです。 画像プリセットは Brand Portal で作成したり修正したりできます。 または、AEM オーサーインスタンスがDynamic Media モードで実行されている場合は、AEM オーサーでプリセットを作成し、AEM Assets Brand Portalに公開できます。 この方法では、Brand Portalで同じプリセットを再作成する必要はありません。
プリセットを作成すると、アセットの詳細レンディションパネルとダウンロードダイアログボックスに動的レンディションとして表示されます。

>[!NOTE]
>
>AEM オーサーインスタンスが&#x200B;**[!UICONTROL Dynamic Media Mode]**&#x200B;で実行されていない場合（お客様がDynamic Mediaを購入していない場合）、アセットの&#x200B;**[!UICONTROL ピラミッド TIFF]** レンディションはアップロード時に作成されません。 画像プリセットまたは動的レンディションは、アセットの&#x200B;**[!UICONTROL ピラミッドTIFF]**&#x200B;で機能します。 したがって、**[!UICONTROL ピラミッド TIFF]**&#x200B;がAEM オーサーインスタンスで使用できない場合、Brand Portalでは使用できません。 その結果、アセットの詳細ページとダウンロードダイアログボックスのレンディションパネルにダイナミックレンディションが表示されません。

画像プリセットを Brand Portal に公開するには、次のようにします。

1. AEM オーサーインスタンスで、AEM ロゴをクリックしてグローバルナビゲーションコンソールにアクセスし、ツールアイコンをクリックして&#x200B;**[!UICONTROL Assets/画像プリセット]**&#x200B;に移動します。
1. 画像プリセットのリストから画像プリセットまたは複数の画像プリセットを選択し、**[!UICONTROL Brand Portalに公開]**&#x200B;をクリックします。

![](assets/publishpreset.png)

>[!NOTE]
>
>ユーザーが「**[!UICONTROL Brand Portalに公開」をクリックすると、画像プリセットは公開用にキューに入れられます。]**&#x200B;レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portal への画像プリセットの公開を取り消すには、次のようにします。

1. AEM オーサーインスタンスで、AEM ロゴをクリックしてグローバルナビゲーションコンソールにアクセスし、**[!UICONTROL ツール]** アイコンをクリックして、**[!UICONTROL Assets/画像プリセット]**&#x200B;に移動します。
1. 画像プリセットを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

## Brand Portal へのメタデータスキーマの公開 {#publish-metadata-schema-to-brand-portal}

メタデータスキーマは、アセットまたはコレクションのプロパティページに表示されるレイアウトとプロパティを記述します。

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

ユーザーがAEM オーサーインスタンスでデフォルトスキーマを編集し、Brand Portalのデフォルトスキーマと同じスキーマを使用する場合は、メタデータスキーマフォームをBrand Portalに公開します。 このような場合、AEM オーサーインスタンスから公開されたデフォルトスキーマは、Brand Portalのデフォルトスキーマを上書きします。

AEM オーサーインスタンス上でカスタムスキーマを作成していた場合は、同じカスタムスキーマを Brand Portal 上で作り直す代わりに、そのカスタムスキーマを Brand Portal に公開できます。 公開されたカスタムスキーマは Brand Portal 内の任意のフォルダーまたはコレクションに適用できます。

>[!NOTE]
>
>デフォルトのスキーマがAEM インスタンスでロックされている場合、Brand Portalに公開できません。 つまり、編集されていません。

![](assets/default-schema-form.png)

>[!NOTE]
>
>フォルダーにAEM オーサーインスタンスでスキーマが適用されている場合は、Brand Portalにも同じスキーマが存在する必要があります。 これにより、AEM オーサーとBrand Portalのアセットプロパティページの一貫性を維持できます。

メタデータスキーマを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. AEM オーサーインスタンスで、AEM ロゴをクリックしてグローバルナビゲーションコンソールにアクセスし、ツールアイコンをクリックして&#x200B;**[!UICONTROL Assets/メタデータスキーマ]**&#x200B;に移動します。
1. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal に公開]**」を選択します。

>[!NOTE]
>
>ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、メタデータスキーマが公開用のキューに入ります。 レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portalからメタデータスキーマを非公開にするには：

1. AEM オーサーインスタンスで、AEM ロゴをクリックしてグローバルナビゲーションコンソールにアクセスし、ツールアイコンをクリックして&#x200B;**[!UICONTROL Assets/メタデータスキーマ]**&#x200B;に移動します。
1. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

## Brand Portal への検索ファセットの公開 {#publish-search-facets-to-brand-portal}

検索フォームは、Brand Portal のユーザーに[ファセット検索](../using/brand-portal-search-facets.md)の機能を提供します。 検索ファセットは Brand Portal 上での詳細検索を可能にします。 検索フォームに[追加されている述語](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/search-facets)はすべて、検索フィルター内の検索ファセットとしてユーザーに提供されます。

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

AEM オーサーインスタンスの&#x200B;**[!UICONTROL Assets管理者検索レール]**&#x200B;でカスタム検索フォームを使用するには、再作成する代わりにBrand Portalに直接公開します。

>[!NOTE]
>
>AEM AssetsからBrand Portalに&#x200B;**[!UICONTROL Assets管理者検索レール]**&#x200B;でロックされた検索フォームを公開するには、まず検索フォームを編集する必要があります。 編集して公開すると、この検索フォームはBrand Portalの既存の検索フォームよりも優先されます。

編集された検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. AEM ロゴをクリックし、**[!UICONTROL ツール/一般/Formsを検索]**&#x200B;に移動します。
1. 編集された検索フォームを選択し、「**[!UICONTROL Brand Portal に公開]**」を選択します。

   >[!NOTE]
   >
   >ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、検索ファセットが公開用のキューに入れられます。 レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portalから検索フォームを非公開にするには：

1. AEM オーサーインスタンスで、AEM ロゴをクリックしてグローバルナビゲーションコンソールにアクセスし、「ツール」アイコンをクリックして、**[!UICONTROL 一般/ Formsを検索]**&#x200B;に移動します。
1. 検索フォームを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

>[!NOTE]
>
>**[!UICONTROL Brand Portalから非公開にする]** アクションは、Brand Portalのデフォルトの検索フォームを残し、公開前に使用された最後の検索フォームに復元しません。

### 制限事項 {#limitations}

1. 検索用述語の中には、Brand Portal 上の検索フィルターに適用できないものがあります。 このような検索用述語が検索フォームの一部として AEM オーサーインスタンスから Brand Portal へ公開された場合は、適用できない検索用述語が削除されます。 したがって、Brand Portal 側では、公開されたフォーム内の述語の数が少なくなります。 詳しくは、[Brand Portal 上のフィルターに適用可能な検索用述語の一覧](../using/brand-portal-search-facets.md#list-of-search-predicates)を参照してください。

1. [!UICONTROL Options Predicate]の場合、ユーザーが任意のカスタムパスを使用してAEM オーサーインスタンスのオプションを読み取る場合、Brand Portalでは機能しません。 このような追加のパスやオプションは、検索フォームと一緒に Brand Portal へ公開されません。 その場合は、ユーザーが&#x200B;**[!UICONTROL オプションの述語]**&#x200B;内の「**[!UICONTROL オプションを追加]**」で「**[!UICONTROL 手動]**」オプションを選択して、Brand Portal 側でこれらのオプションを手動で追加できます。

![](assets/options-predicate-manual.png)
