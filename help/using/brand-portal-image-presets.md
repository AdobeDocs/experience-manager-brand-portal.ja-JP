---
title: 画像プリセットまたは動的レンディションの適用
description: 画像プリセットは、マクロと同様、サイズとフォーマットに関するコマンドのコレクションを事前に定義し、名前を付けて保存したものです。 画像プリセット Experience Manager Assets Brand Portalでは、様々なサイズ、フォーマット、プロパティの画像を動的に配信できます。
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 212a1b3a-686f-4250-be06-b679b6039887
TQID: https://experienceleague.adobe.com/XWG-kCasFqDycZEmxS6SBEVh4Jz-79p-u56SilhfprY
product_v2:
  - id: d09181b5-a36a-43de-ba01-36641440bc43
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
  - id: cda65036-5305-4f01-89da-9b3506ae8c50
subfeature_v2:
  - id: cf50b0d2-df62-495c-a741-4fa0284ca4fc
  - id: ee69dd13-2aba-4eb0-912b-399e82368d73
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e48edcb1ed5d76686794f7a7ed6389c7f4ab1ed3
workflow-type: tm+mt
source-wordcount: 817
ht-degree: 54%

---

# 画像プリセットまたは動的レンディションの適用 {#apply-image-presets-or-dynamic-renditions}

画像プリセットは、マクロと同様、サイズとフォーマットに関するコマンドのコレクションを事前に定義し、名前を付けて保存したものです。 画像プリセット Experience Manager Assets Brand Portalでは、様々なサイズ、フォーマット、プロパティの画像を動的に配信できます。

画像プリセットを使用して、プレビューおよびダウンロード可能な画像の動的レンディションを生成します。 画像とそのレンディションをプレビューする際に、管理者が設定した仕様に合わせて画像を再フォーマットするプリセットを選択できます。

（*Experience Manager Assets オーサーインスタンスが&#x200B;**Dynamic Media ハイブリッドモード***で実行されている場合）。 Brand Portalでアセットのダイナミックレンディションを表示するには、Brand Portalに公開するExperience Manager Assets オーサーインスタンスにピラミッド TIFF レンディションが存在することを確認します。 アセットを公開すると、その PTIFF レンディションも Brand Portal に公開されます。

>[!NOTE]
>
>画像とそのレンディションをダウンロードする場合、既存のプリセットから選択するオプションはありません。 代わりに、カスタム画像プリセットのプロパティを指定できます。 詳しくは、[画像のダウンロード時に画像プリセットを適用する](../using/brand-portal-image-presets.md#main-pars-text-1403412644)を参照してください。


画像プリセットの作成時に必要となるパラメーターについて詳しくは、[画像プリセットの管理](../using/brand-portal-image-presets.md)を参照してください。

## 画像プリセットの作成 {#create-an-image-preset}

Experience Manager Assets 管理者は、アセットの詳細ページに動的レンディションとして表示される画像プリセットを作成できます。 画像プリセットをゼロから作成することも、新しい名前で既存のものを保存することもできます。 画像プリセットを作成する場合は、画像配信用のサイズと書式設定コマンドを選択します。 画像が表示用に配信されるときには、選択したコマンドに応じて画像の外観が最適化されます。

>[!NOTE]
>
>画像の動的レンディションは、ピラミッド TIFF を使用して作成されます。 ピラミッド TIFFがどのアセットにも使用できない場合、そのアセットのダイナミックレンディションをBrand Portalで取得することはできません。
>
>Experience Manager Assets オーサーインスタンスが&#x200B;**Dynamic Media ハイブリッドモード**&#x200B;で実行されている場合、画像アセットのピラミッド TIFF レンディションが作成され、Experience Manager Assets リポジトリに保存されます。
>
>ただし、Experience Manager Assets オーサーインスタンスが&#x200B;**Dynamic Media Scene7 モード**&#x200B;で動作している場合、画像アセットのピラミッド TIFF レンディションはScene7 サーバーに存在します。
>
>これらのアセットがBrand Portalに公開されると、画像プリセットが適用され、ダイナミックレンディションが表示されます。


1. 上部のツールバーで Experience Manager ロゴをクリックして、管理ツールにアクセスします。

1. 管理ツールパネルの「**[!UICONTROL 画像プリセット]**」をクリックします。

   ![](assets/admin-tools-panel-4.png)

1. 画像プリセットページの「**[!UICONTROL 作成]**」をクリックします。

   ![](assets/image_preset_homepage.png)

1. **[!UICONTROL 画像プリセットを編集]**&#x200B;ページで、「**[!UICONTROL 基本]**」または「**[!UICONTROL 詳細]**」のどちらか該当するタブに、名前などの値を入力します。 プリセットは左側のウィンドウに表示され、他のアセットにすぐに使用できます。

   ![](assets/image_preset_create.png)

   >[!NOTE]
   >
   >**[!UICONTROL 画像プリセットを編集]**&#x200B;ページを使用して、既存の画像プリセットのプロパティを編集することもできます。 画像プリセットを編集するには、該当する画像プリセットを画像プリセットページから選択し、「**[!UICONTROL 編集]**」をクリックします。

1. 「**[!UICONTROL 保存]**」をクリックします。 画像プリセットが作成され、画像プリセットページに表示されます。
1. 画像プリセットを削除するには、画像プリセットページから削除する画像プリセットを選択し、「**[!UICONTROL 削除]**」をクリックします。 確認ページで「**[!UICONTROL 削除]**」をクリックして、削除することを確認します。 指定した画像プリセットが、画像プリセットページから削除されます。

## 画像をプレビューする際の画像プリセットの適用 {#apply-image-presets-when-previewing-images}

画像とそのレンディションをプレビューするときは、既存のプリセットから選択することで、管理者が設定した仕様で画像を再フォーマットできます。

1. Brand Portal インターフェイスで、画像をクリックして開きます。
1. 左側のオーバーレイアイコンをクリックし、「**[!UICONTROL レンディション]**」を選択します。

   ![](assets/image-preset-previewrenditions.png)

1. **[!UICONTROL レンディション]**&#x200B;リストから、適切な動的レンディション（例：「**[!UICONTROL サムネール]**」）を選択します。 プレビュー画像は、選択したレンディションに基づいてレンダリングされます。

   ![](assets/image-preset-previewrenditionthumbnail.png)

## 画像のダウンロード時に画像プリセットを適用する {#apply-image-presets-when-downloading-images}

Brand Portal から画像とそのレンディションをダウンロードするときは、既存の画像プリセットから選択することはできません。 ただし、再フォーマットする画像に基づいて、画像プリセットのプロパティをカスタマイズできます。

1. Brand Portal コンソールで、以下のいずれかの手順を実行します。

   * ダウンロードする画像の上にポインターを置きます。 使用できるクイックアクションサムネールから、**[!UICONTROL ダウンロード]**&#x200B;アイコンをクリックします。

   ![](assets/downloadsingleasset.png)

   * ダウンロードする画像を選択します。 上部のツールバーで「**[!UICONTROL ダウンロード]**」アイコンをクリックします。

   ![](assets/downloadassets.png)

1. **[!UICONTROL ダウンロード]**&#x200B;ダイアログボックスで、アセットとそのレンディションを一緒にダウンロードするかどうかに応じて、必要なオプションを選択します。

   ![](assets/donload-assets-dialog.png)

1. アセットの動的レンディションをダウンロードするには、**[!UICONTROL 動的レンディション]** オプションを選択します。
1. 画像プリセットプロパティをカスタマイズして、ダウンロード中に画像とそのレンディションを動的に再フォーマットします。 サイズ、形式、カラースペース、解像度、画像修飾子を指定します。

   ![](assets/dynamicrenditions.png)

1. 「**[!UICONTROL ダウンロード]**」をクリックします。 カスタムの動的レンディションが、ダウンロード対象として選択した画像とレンディションと一緒に ZIP ファイルにダウンロードされます。 ただし、1つのアセットがダウンロードされた場合、zip ファイルは作成されません。これにより、迅速なダウンロードが可能になります。
