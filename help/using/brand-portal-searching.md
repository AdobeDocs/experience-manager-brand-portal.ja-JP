---
title: Brand Portal でのアセットの検索
seo-title: Asset searching and saved search on Experience Manager Assets Brand Portal
description: Brand Portalの検索機能を使用すると、オムニサーチを使用して関連するアセットをすばやく検索でき、検索フィルターを使用すると検索をさらに絞り込むことができます。 検索設定をスマートコレクションとして保存しておき、後で呼び出すことができます。
seo-description: Brand Portal search capability lets you quickly search for relevant assets using omnisearch, and search filters help you further narrow down your search. Save your searches as smart collections for future.
uuid: c2955198-bdc0-4853-a13a-661e6a9ec61f
contentOwner: bdhar
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: SearchandPromote
discoiquuid: dc751cd7-f663-46d2-84c4-5bb12a4fe1ba
exl-id: 7297bbe5-df8c-4d0b-8204-218a9fdc2292
source-git-commit: cbdd943b904882cc9a455bab24c3cf732d5966ca
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 94%

---

# Brand Portal でのアセットの検索 {#search-assets-on-brand-portal}

Brand Portal の検索機能ではオムニチャネルと、検索をさらに絞り込むことができるフィルターを使用したファセット検索を使用して、関連したアセットをすばやく検索することができます。ファイルレベルまたはフォルダーレベルでアセットを検索し、検索結果をスマートコレクションとして保存できます。

>[!NOTE]
>
>Brand Portal は、オムニサーチを使用したコレクション検索をサポートしていません。
>
>ただし、[検索フィルターを使用して、関連するコレクションのリストを取得する](#search-collection)ことができます。

## オムニサーチを使用したアセット検索 {#search-assets-using-omnisearch}

Brand Portal 上でアセットを検索するには、次のようにします。

1. ツールバーの&#x200B;**[!UICONTROL 検索]**&#x200B;アイコンをクリックするか、**[!UICONTROL /]** キーを押してオムニサーチを起動します。

   ![](assets/omnisearchicon-1.png)

1. 検索ボックスに、検索するアセットのキーワードを入力します。

   ![](assets/omnisearch.png)

   >[!NOTE]
   >
   >* オムニサーチで検索候補が表示されるには、3 文字以上入力する必要があります。
   >* `mountain biking` を検索すると、オムニサーチでは、検索結果に、メタデータフィールドで使用できる `mountain` と `biking` の両方を含むすべてのアセットを返します。例： `Title`フィールド内の`mountain`と`Description`フィールド内の`biking` 検索結果に表示するには、両方の単語がメタデータフィールドで使用可能である必要があります。 ただし、スマートタグのメタデータフィールドで使用できる単語が 2 つのうち 1 つだけの場合でも、オムニサーチでは、検索結果でそのアセットを返します。例えば、あるアセットのスマートタグのいずれかとして `mountain` が含まれ、他のメタデータフィールドに `biking` が含まれていない場合、`mountain biking` を検索すると、オムニサーチでは、検索結果でそのアセットを返します。

1. ドロップダウンリストに表示される関連候補の中から選択すれば、関連するアセットにすばやくアクセスできます。

   ![](assets/assets-search-result.png)

   *オムニサーチを使用したアセット検索*

スマートタグ付きアセットでの検索動作については、[AEM でのアセットの検索](https://experienceleague.adobe.com/docs/experience-manager-65/assets/using/search-assets.html?lang=ja)を参照してください。

## フィルターパネルでのファセットを使用した検索 {#search-using-facets-in-filters-panel}

フィルターパネルの検索ファセットを使用すると、詳細な検索条件を指定して、検索効率を高めることができます。検索ファセットでは、複数のディメンション（述語）を使用して、より複雑な検索を実行できます。検索の焦点をさらに絞り込むために、必要な詳細レベルまで簡単にドリルダウンできます。

例えば、画像を検索する場合、ビットマップ画像とベクトル画像のどちらを検索するかを選択できます。ファイルタイプ検索ファセットで画像の MIME タイプを指定することで、検索範囲をさらに絞り込むことができます。 同様に、ドキュメントを検索する場合は、PDF や MS® Word などの形式を指定できます。

![Brand Portal のフィルターパネル](assets/file-type-search.png "Brand Portal のフィルターパネル")

**[!UICONTROL フィルター]**&#x200B;パネルには、**[!UICONTROL パスブラウザー]**、**[!UICONTROL ファイルタイプ]**、**[!UICONTROL ファイルサイズ]**、**[!UICONTROL ステータス]**、**[!UICONTROL 回転角度]**&#x200B;などの、いくつかの標準的なファセットが用意されています。ただし、**[!UICONTROL フィルター]**&#x200B;パネルに[カスタム検索ファセットを追加](../using/brand-portal-search-facets.md)したり、特定の検索ファセットを削除したりすることも可能です。そのためには、基礎となる検索フォームで述語を追加または削除します。詳しくは、[Brand Portal で利用可能な検索用述語の一覧](../using/brand-portal-search-facets.md#list-of-search-predicates)を参照してください。

利用可能な[検索ファセット](../using/brand-portal-search-facets.md)を使用して検索にフィルターを適用するには、次のようにします。

1. オーバーレイアイコンをクリックし、「**[!UICONTROL フィルター]**」を選択します。

   ![](assets/selectorrail.png)

1. 左側の **[!UICONTROL フィルター]** パネルから、適切なオプションを選択して、関連するフィルターを適用します。
例えば、以下の標準のフィルターを使用します。

   * **[!UICONTROL パスブラウザー]**：特定のディレクトリ内のアセットを検索します。パスブラウザーの述語のデフォルト検索パスは `/content/dam/mac/<tenant-id>/` です。これはデフォルトの検索フォームを編集することで設定できます。

   >[!NOTE]
   >
   >管理者以外のユーザーの場合、[!UICONTROL フィルター]パネルの[!UICONTROL パスブラウザー]には、そのユーザーに共有されているフォルダー（とその上位層）のコンテンツ構造のみが表示されます。\
   >管理者ユーザーは、パスブラウザーを使用して、Brand Portal の任意のフォルダーに移動できます。

   * **[!UICONTROL ファイルタイプ]**：検索するアセットファイルのタイプ（画像、ドキュメント、マルチメディア、アーカイブ）を指定します。さらに、例えば画像の MIME タイプ（Tiff、ビットマップ、GIMP 画像）やドキュメントの形式（PDF、MS® Word）を指定して、検索の範囲を絞り込むことができます。
   * **[!UICONTROL ファイルサイズ]**：ファイルサイズに基づいてアセットを検索します。サイズ範囲の下限と上限を指定して検索を絞り込むことができます。また、検索の単位を指定できます。
   * **[!UICONTROL ステータス]**：承認のステータス（承認済み、リクエストされた変更、却下、保留）や有効期限などのアセットのステータスに基づいてアセットを検索します。
   * **[!UICONTROL 平均評価]**：アセットの評価に基づいてアセットを検索します。
   * **[!UICONTROL 回転角度]**：アセットの回転角度（水平方向、垂直方向、四角形）に基づいてアセットを検索します。
   * **[!UICONTROL スタイル]**：アセットのスタイル（カラー、モノクロ）に基づいてアセットを検索します。
   * **[!UICONTROL ビデオ形式]**：形式（DVI、Flash、MPEG4、MPEG、OGG Theora、QuickTime、Windows Media、WebM）に基づいてビデオアセットを検索します。

   フィルターパネルで[カスタム検索ファセット](../using/brand-portal-search-facets.md)を使用できるようにするには、基礎となる検索フォームを編集します。

   * **[!UICONTROL プロパティの述語]**：検索フォームで使用すると、述語のマッピング先のメタデータプロパティに一致するアセットを検索できます。\
     例えば、プロパティの述語が [!UICONTROL `jcr:content /metadata/dc:title`] にマッピングされている場合は、タイトルに基づいてアセットを検索できます。\
     [!UICONTROL プロパティの述語]では、以下の場合のテキスト検索をサポートしています。

     **部分的な語句**
プロパティの述語で部分的な語句を使用したアセット検索を許可するには、検索フォームの「**[!UICONTROL 部分検索]**」チェックボックスを有効にします。これにより、アセットメタデータで使用する語句を指定しなくても、目的のアセットを検索できます。

     >[!NOTE]
     >
     > Brand Portal では、部分検索用に次のフィールドをサポートしています。
     >* jcr:content/metadata/dc:title
     >* jcr:content/jcr:title
     >* jcr:content/metadata/dam:search_promote
     >* jcr:content/metadata/dc:format

     以下の操作を実行できます。
      * フィルターパネルのファセットで、検索しようとするフレーズに出てくる単語を指定します。例えば、「**climb**」という単語を検索する（およびプロパティの述語が [!UICONTROL `dc:title`] プロパティにマッピングされている）と、タイトルに「**climb**」という単語を含むアセットがすべて返されます。
      * 検索する語句に含まれている単語の一部を指定し、不明な箇所をワイルドカード文字（&#42;）で補完します。
例えば、次のようになります。
         * **climb&#42;** を検索すると、「climb」という文字列で始まる単語がタイトルフレーズで使用されているアセットがすべて返されます。
         * **&#42;climb** を検索すると、「climb」という文字列で終わる単語がタイトルフレーズで使用されているアセットがすべて返されます。
         * **&#42;climb&#42;** を検索すると、「climb」という部分文字列を含んだ単語がタイトルフレーズで使用されているアセットがすべて返されます。

     **大文字と小文字を区別しないテキスト**
プロパティの述語で大文字と小文字を区別せずに検索するには、検索フォームの「**[!UICONTROL 大文字と小文字を区別しない]**」チェックボックスをオンにします。プロパティの述語のテキスト検索では、デフォルトで大文字と小文字が区別されます。

   >[!NOTE]
   >
   >「**[!UICONTROL 部分検索]**」チェックボックスを選択すると、デフォルトで「**[!UICONTROL 大文字と小文字を区別しない]**」がオンになります。

   ![](assets/wildcard-prop-1.png)

   適用したフィルターに従って検索結果が表示され、同時に検索結果数も表示されます。

   ![](assets/omnisearch-with-filters.png)

   検索結果数を使用したアセット検索結果。

1. 検索結果から特定の項目に移動した後、ブラウザーの戻るボタンを使用して元の検索結果に簡単に戻ることができます。検索クエリを再実行する必要はありません。

## 検索設定をスマートコレクションとして保存 {#save-your-searches-as-smart-collection}

検索設定をスマートコレクションとして保存しておくと、同じ検索をすぐに再実行することができ、後で同じ設定をし直す必要がなくなります。ただし、コレクションに検索フィルターを適用することはできません。

検索設定をスマートコレクションとして保存するには：

1. 「**[!UICONTROL スマートコレクションを保存]**」をタップまたはクリックし、スマートコレクションの名前を指定します。

   すべてのユーザーがアクセスできるスマートコレクションにするには、「**[!UICONTROL 公開]**」を選択します。スマートコレクションが作成され、保存済みの検索の一覧に追加されたことを示すメッセージが表示されます。

   >[!NOTE]
   >
   >管理者以外のユーザーによるスマートコレクションの公開を制限できます。これにより、管理者以外のユーザーが組織の Brand Portal 上に多数の公開スマートコレクションを作成することを防止できます。管理ツールパネルの&#x200B;**[!UICONTROL 一般]**&#x200B;設定で、「**[!UICONTROL 公開スマートコレクションの作成を許可]**」設定を無効化できます。

   ![](assets/save_smartcollectionui.png)

1. スマートコレクションを別の名前で保存したり、「**[!UICONTROL 公開]**」チェックボックスをオンまたはオフにするには、「**[!UICONTROL スマートコレクションを編集]**」をクリックします。

   ![](assets/edit_smartcollection.png)

1. **[!UICONTROL スマートコレクションを編集]**&#x200B;ダイアログボックスで、「**[!UICONTROL 名前を付けて保存]**」を選択し、スマートコレクションの名前を入力します。「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/saveas_smartsearch.png)


## コレクションを検索 {#search-collection}

コレクションでは、オムニサーチはサポートされていません。 ただし、検索フィルターを適用して、[!UICONTROL コレクション]インターフェイス内で関連するコレクションを一覧表示することができます。

[!UICONTROL コレクション]インターフェイスで、オーバーレイアイコンをクリックし、左側のパネルでフィルターパネルを開きます。使用可能なフィルターから 1 つまたは複数の検索フィルターを適用します（`modified date`、`access type`、および `tags`）。適用されたフィルターに基づいて、最も関連性の高いコレクションのセットが一覧表示されます。

![](assets/collection-search.png)
