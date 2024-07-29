---
title: Brand Portal へのプリセット、スキーマ、ファセットの公開
seo-title: Publish presets, schema, and facets to Brand Portal
description: プリセット、スキーマ、ファセットを Brand Portal に公開する方法を説明します。
seo-description: Learn how to publish presets, schema, and facets to Brand Portal.
uuid: c836d9bb-074a-4113-9c91-b2bf7658b88d
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: bc305abc-9373-4d33-9179-0a5f3904b352
exl-id: 9b585606-6538-459b-87a9-2e68df0087b3
source-git-commit: 133ea1fc342e4460e7d0661205c7411a509143eb
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 88%

---

# Brand Portal へのプリセット、スキーマ、ファセットの公開 {#publish-presets-schema-and-facets-to-brand-portal}

この記事では、画像プリセット、メタデータスキーマおよびカスタム検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開する方法について説明します。公開機能を利用すると、AEM オーサーインスタンス上で作成または修正した画像プリセット、メタデータスキーマおよび検索ファセットを再利用して、重複作業を減らすことができます。

>[!NOTE]
>
>画像プリセット、メタデータスキーマおよび検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開する機能は、AEM 6.2 SP1-CFP7 および AEM 6.3 SP 1-CFP 1（6.3.1.1）以降で使用できます。

## Brand Portal への画像プリセットの公開 {#publish-image-presets-to-brand-portal}

画像プリセットとは、画像配信の際に画像に適用される一連のサイズ変更コマンドやフォーマットコマンドをまとめたものです。画像プリセットは Brand Portal で作成したり修正したりできます。あるいは、AEM オーサーインスタンスがダイナミックメディアモードで動作している場合は、ユーザーが AEM オーサーインスタンス上でプリセットを作成し、そのプリセットを AEM Assets Brand Portal に公開することができます。これにより、同じプリセットを Brand Portal 上で作り直す必要がなくなります。\
プリセットを作成すると、それがアセット詳細のレンディションパネルとダウンロードダイアログに動的レンディションとしてリストされます。

>[!NOTE]
>
>AEM オーサーインスタンスが **[!UICONTROL Dynamic Media モード]**&#x200B;で動作していない（顧客が Dynamic Media を購入していない）場合、アセットの&#x200B;**[!UICONTROL ピラミッド TIFF]** レンディションはアップロード時に作成されません。画像プリセットまたは動的レンディションは、アセットの&#x200B;**[!UICONTROL ピラミッド TIFF]** で機能するので、**[!UICONTROL ピラミッド TIFF]** が AEM オーサーインスタンスで使用できない場合は、Brand Portal 上でも使用できません。したがって、動的レンディションがアセット詳細ページのレンディションパネルやダウンロードダイアログに表示されません。

画像プリセットを Brand Portal に公開するには、次のようにします。

1. AEM オーサーインスタンスで、AEM のロゴをタップまたはクリックしてグローバルナビゲーションコンソールにアクセスし、ツールアイコンをタップまたはクリックして&#x200B;**[!UICONTROL アセット／画像プリセット]**&#x200B;の順に移動します。
1. 画像プリセットのリストから目的の画像プリセットを 1 つまたは複数選択し、「**[!UICONTROL Brand Portal に公開]**」をクリックまたはタップします。

![](assets/publishpreset.png)

>[!NOTE]
>
>ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、画像プリセットが公開用のキューに入ります。レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portal への画像プリセットの公開を取り消すには、次のようにします。

1. AEM オーサーインスタンスで、AEM ロゴをタップまたはクリックしてグローバルナビゲーションコンソールにアクセスし、**[!UICONTROL ツール]** アイコンをクリックして、**[!UICONTROL Assets/画像プリセット]** に移動します。
1. 画像プリセットを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

## Brand Portal へのメタデータスキーマの公開   {#publish-metadata-schema-to-brand-portal}

メタデータスキーマは、アセットまたはコレクションのプロパティページに表示されるレイアウトとプロパティを記述します。

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

AEM オーサーインスタンス上のデフォルトスキーマを編集済みで、デフォルトスキーマと同じスキーマを Brand Portal 上でも使用したい場合には、そのメタデータスキーマフォームを Brand Portal に公開することができます。このシナリオでは、Brand Portal 側のデフォルトスキーマが、AEM オーサーインスタンスから公開されたデフォルトスキーマによってオーバーライドされます。

AEM オーサーインスタンス上でカスタムスキーマを作成していた場合は、同じカスタムスキーマを Brand Portal 上で作り直す代わりに、そのカスタムスキーマを Brand Portal に公開できます。公開されたカスタムスキーマは Brand Portal 内の任意のフォルダーまたはコレクションに適用できます。

>[!NOTE]
>
>デフォルトスキーマが AEM インスタンス側でロックされている場合（つまりデフォルトスキーマが未編集の場合）は、Brand Portal に公開できません。

![](assets/default-schema-form.png)

>[!NOTE]
>
>AEM オーサーインスタンス上でフォルダーにスキーマが適用されている場合、AEM オーサーインスタンス上と Brand Portal 上のアセットプロパティページで一貫性を維持するためには、Brand Portal 上にも同じスキーマが存在している必要があります。

メタデータスキーマを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. AEM オーサーインスタンスで、AEM ロゴをタップまたはクリックしてグローバルナビゲーションコンソールにアクセスし、ツールアイコンをクリックして、**[!UICONTROL Assets/メタデータスキーマ]** に移動します。
1. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal に公開]**」を選択します。

>[!NOTE]
>
>ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、メタデータスキーマが公開用のキューに入ります。レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portalからメタデータスキーマを非公開にするには：

1. AEM オーサーインスタンスで、AEM ロゴをタップまたはクリックしてグローバルナビゲーションコンソールにアクセスし、ツールアイコンをクリックして、**[!UICONTROL Assets/メタデータスキーマ]** に移動します。
1. メタデータスキーマを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

## Brand Portal への検索ファセットの公開 {#publish-search-facets-to-brand-portal}

検索フォームは、Brand Portal のユーザーに[ファセット検索](../using/brand-portal-search-facets.md)の機能を提供します。検索ファセットは Brand Portal 上での詳細検索を可能にします。検索フォームに[追加されている述語](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/search-facets.html?lang=ja)はすべて、検索フィルター内の検索ファセットとしてユーザーに提供されます。

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

AEM オーサーインスタンスのカスタム検索フォーム「**[!UICONTROL アセット管理者の検索パネル]**」を使用したい場合は、Brand Portal 上で同じフォームを作成し直す代わりに、カスタマイズされた検索フォームを AEM オーサーインスタンスから Brand Portal に公開できます。

>[!NOTE]
>
>AEM Assets 上のロックされた検索フォーム「**[!UICONTROL アセット管理者の検索パネル]**」は Brand Portal に公開できませんが、編集されている場合は公開可能です。編集されて Brand Portal に公開されると、この検索フォームが Brand Portal 上の検索フォームをオーバーライドします。

編集された検索ファセットを AEM オーサーインスタンスから Brand Portal へ公開するには、次のようにします。

1. AEMのロゴをクリックし、**[!UICONTROL ツール/一般/Formsを検索]** に移動します。
1. 編集された検索フォームを選択し、「**[!UICONTROL Brand Portal に公開]**」を選択します。

   >[!NOTE]
   >
   >ユーザーが「**[!UICONTROL Brand Portal に公開]**」をクリックすると、検索ファセットが公開用のキューに入れられます。レプリケーションエージェントのログを監視して、公開が成功したかどうかを確認することを推奨します。

Brand Portalから検索フォームを非公開にするには、次の手順を実行します。

1. AEM オーサーインスタンスで、AEM ロゴをタップまたはクリックしてグローバルナビゲーションコンソールにアクセスし、ツールアイコンをクリックして、**[!UICONTROL 一般/Formsを検索]** に移動します。
1. 検索フォームを選択し、上部にあるオプションから「**[!UICONTROL Brand Portal から削除]**」を選択します。

>[!NOTE]
>
>「**[!UICONTROL Brand Portal で非公開]**」アクションを実行しても、デフォルトの検索フォームが Brand Portal にそのまま残され、公開前まで使用された検索フォームには復元されません。

### 制限事項 {#limitations}

1. 検索用述語の中には、Brand Portal 上の検索フィルターに適用できないものがあります。このような検索用述語が検索フォームの一部として AEM オーサーインスタンスから Brand Portal へ公開された場合は、適用できない検索用述語が削除されます。したがって、Brand Portal 側では、公開されたフォーム内の述語の数が少なくなります。詳しくは、[Brand Portal 上のフィルターに適用可能な検索用述語の一覧](../using/brand-portal-search-facets.md#list-of-search-predicates)を参照してください。

1. [!UICONTROL オプションの述語]に関しては、ユーザーが AEM オーサーインスタンス側のオプションを読み取るために任意のカスタムパスを使用している場合、そのパスは Brand Portal 側では機能しません。このような追加のパスやオプションは、検索フォームと一緒に Brand Portal へ公開されません。その場合は、ユーザーが&#x200B;**[!UICONTROL オプションの述語]**&#x200B;内の「**[!UICONTROL オプションを追加]**」で「**[!UICONTROL 手動]**」オプションを選択して、Brand Portal 側でこれらのオプションを手動で追加できます。

![](assets/options-predicate-manual.png)
