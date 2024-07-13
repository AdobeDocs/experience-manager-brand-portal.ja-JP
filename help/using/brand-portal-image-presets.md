---
title: 画像プリセットまたは動的レンディションの適用
seo-title: Apply image presets or dynamic renditions
description: 画像プリセットは、マクロと同様、サイズとフォーマットに関するコマンドのコレクションを事前に定義し、名前を付けて保存したものです。画像プリセットを使用すると、サイズ、形式、プロパティが様々に異なる画像を Experience Manager Assets Brand Portal で動的に配信できます。
seo-description: Like a macro, an image preset is a predefined collection of sizing and formatting commands saved under a name. Image presets enable Experience Manager Assets Brand Portal to dynamically deliver images of different sizes, formats, and properties.
uuid: a3c8705c-5fbd-472c-8b61-f65b3e552c1b
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: a512dfa0-fef3-4c3f-a389-a0a3a7415bac
role: Admin
exl-id: 212a1b3a-686f-4250-be06-b679b6039887
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 81%

---

# 画像プリセットまたは動的レンディションの適用 {#apply-image-presets-or-dynamic-renditions}

画像プリセットは、マクロと同様、サイズとフォーマットに関するコマンドのコレクションを事前に定義し、名前を付けて保存したものです。画像プリセットを使用すると、サイズ、形式、プロパティが様々に異なる画像を Experience Manager Assets Brand Portal で動的に配信できます。

画像プリセットは、プレビューおよびダウンロード可能な画像の動的レンディションを生成するために使用されます。 画像とそのレンディションをプレビューする際に、プリセットを選択すると、管理者が設定した仕様に合わせて画像を再フォーマットできます。

（*Experience Manager Assets（オーサー）インスタンスが **Dynamic Media ハイブリッドモード***で実行されている場合）Brand Portal でアセットの動的レンディションを表示するには、Brand Portal に公開する Experience Manager Assets オーサーインスタンスにピラミッド TIFF レンディションが存在することを確認します。アセットを公開すると、その PTIFF レンディションも Brand Portal に公開されます。

>[!NOTE]
>
>画像とそのレンディションをダウンロードする場合、既存のプリセットから選択するオプションはありません。 代わりに、カスタム画像プリセットのプロパティを指定できます。 詳しくは、[ 画像のダウンロード時に画像プリセットを適用する ](../using/brand-portal-image-presets.md#main-pars-text-1403412644) を参照してください。


画像プリセットの作成時に必要となるパラメーターについて詳しくは、[画像プリセットの管理](../using/brand-portal-image-presets.md)を参照してください。

## 画像プリセットの作成 {#create-an-image-preset}

Experience Manager Assets 管理者は、アセットの詳細ページに動的レンディションとして表示される画像プリセットを作成できます。画像プリセットは、最初から作成することも、既存の画像プリセットを新しい名前で保存することもできます。 画像プリセットを作成する際は、画像配信のサイズと書式設定コマンドを選択します。 画像が表示用に配信されるときには、選択したコマンドに応じて画像の外観が最適化されます。

>[!NOTE]
>
>画像の動的レンディションは、ピラミッド TIFF を使用して作成されます。ピラミッド TIFF がどのアセットにも使用できない場合、そのアセットの動的レンディションを Brand Portal で取得することはできません。
>
>Experience Manager Assets オーサーインスタンスが **Dynamic Media ハイブリッドモード**&#x200B;で実行されている場合、画像アセットのピラミッド TIFF レンディションが作成されて Experience Manager Assets リポジトリに保存されます。
>
>これに対して、Experience Manager Assets オーサーインスタンスが **Dynamic Media Scene7 モード**&#x200B;で実行されている場合、画像アセットのピラミッド TIFF レンディションは Scene7 サーバー上に存在します。
>
>このようなアセットが Brand Portal に公開されると、画像プリセットが適用されて動的レンディションが表示されます。


1. 上部のツールバーで Experience Manager ロゴをクリックして、管理ツールにアクセスします。

1. 管理ツールパネルの「**[!UICONTROL 画像プリセット]**」をクリックします。

   ![](assets/admin-tools-panel-4.png)

1. 画像プリセットページの「**[!UICONTROL 作成]**」をクリックします。

   ![](assets/image_preset_homepage.png)

1. **[!UICONTROL 画像プリセットを編集]**&#x200B;ページで、「**[!UICONTROL 基本]**」または「**[!UICONTROL 詳細]**」のどちらか該当するタブに、名前などの値を入力します。プリセットは左側のウィンドウに表示され、他のアセットにすぐに使用できます。

   ![](assets/image_preset_create.png)

   >[!NOTE]
   >
   >**[!UICONTROL 画像プリセットを編集]**&#x200B;ページを使用して、既存の画像プリセットのプロパティを編集することもできます。画像プリセットを編集するには、該当する画像プリセットを画像プリセットページから選択し、「**[!UICONTROL 編集]**」をクリックします。

1. 「**[!UICONTROL 保存]**」をクリックします。画像プリセットが作成され、画像プリセットページに表示されます。
1. 画像プリセットを削除するには、画像プリセットページから削除する画像プリセットを選択し、「**[!UICONTROL 削除]**」をクリックします。確認ページで「**[!UICONTROL 削除]**」をクリックして、削除することを確認します。指定した画像プリセットが、画像プリセットページから削除されます。

## 画像をプレビューする際の画像プリセットの適用  {#apply-image-presets-when-previewing-images}

画像とそのレンディションをプレビューするときは、既存のプリセットから選択することで、管理者が設定した仕様で画像を再フォーマットできます。

1. Brand Portal インターフェイスで、画像をクリックして開きます。
1. 左側のオーバーレイアイコンをクリックし、「**[!UICONTROL レンディション]**」を選択します。

   ![](assets/image-preset-previewrenditions.png)

1. **[!UICONTROL レンディション]**&#x200B;リストから、適切な動的レンディション（例：「**[!UICONTROL サムネール]**」）を選択します。プレビューイメージは、選択したレンディションに基づいてレンダリングされます。

   ![](assets/image-preset-previewrenditionthumbnail.png)

## 画像のダウンロード時に画像プリセットを適用する {#apply-image-presets-when-downloading-images}

Brand Portal から画像とそのレンディションをダウンロードするときは、既存の画像プリセットから選択することはできません。ただし、再フォーマットする画像に基づいて、画像プリセットのプロパティをカスタマイズできます。

1. Brand Portal コンソールで、以下のいずれかの手順を実行します。

   * ダウンロードする画像の上にマウスポインターを置きます。使用できるクイックアクションサムネールから、**[!UICONTROL ダウンロード]**&#x200B;アイコンをクリックします。

   ![](assets/downloadsingleasset.png)

   * ダウンロードする画像を選択します。上部のツールバーで「**[!UICONTROL ダウンロード]**」アイコンをクリックします。

   ![](assets/downloadassets.png)

1. **[!UICONTROL ダウンロード]**&#x200B;ダイアログボックスで、アセットとそのレンディションを一緒にダウンロードするかどうかに応じて、必要なオプションを選択します。

   ![](assets/donload-assets-dialog.png)

1. アセットの動的レンディションをダウンロードするには、「**[!UICONTROL 動的レンディション]**」オプションを選択します。
1. ダウンロード中に画像とそのレンディションを動的に再書式設定する対象に基づいて、画像プリセットのプロパティをカスタマイズします。 サイズ、形式、カラースペース、解像度および画像修飾子を指定します。

   ![](assets/dynamicrenditions.png)

1. 「**[!UICONTROL ダウンロード]**」をクリックします。カスタムの動的レンディションが、ダウンロード対象として選択した画像とレンディションと一緒に ZIP ファイルにダウンロードされます。ただし、ダウンロードするアセットが 1 つだけの場合は、迅速なダウンロードを行うために ZIP ファイルは作成されません。
