---
title: Brand Portal でアセットを参照する
description: Brand Portal の様々な表示オプションや UI 要素を使用して、アセットの参照、アセット階層のトラバース、およびアセットの検索を行います。
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: introduction
exl-id: 405d7861-a140-44b1-ae1f-4f0839f05033
source-git-commit: 4d9d7afa2cd45ea68c2e15338c92aa29ecf09f91
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 30%

---

# Brand Portal でアセットを参照する {#browsing-assets-on-brand-portal}

Experience Manager Assets Brand Portalには、様々な機能やユーザーインターフェイス要素が用意されており、様々な表示オプションを使用して、リソースの参照、アセット階層の移動、アセットの検索を簡単に行うことができます。

管理者ユーザーは、上部にあるツールバーのExperience Managerロゴから、管理ツールパネルへアクセスできます。

![](assets/aemlogo.png)

![](assets/admin-tools-panel-2.png)

![](assets/bp_subheader.png)

Brand Portalの左上にあるパネルセレクターのドロップダウンでは、アセット階層への移動、検索の効率化、リソースの表示を行うオプションを表示できます。

![](assets/siderail-1.png)

Brand Portalの表示セレクターで使用可能ないずれかの表示（カード、列、リスト）を使用して、アセットを表示、移動および選択できます。

![](assets/viewselector.png)

## リソースの表示と選択 {#viewing-and-selecting-resources}

概念上、表示、ナビゲーションおよび選択はすべての表示で同じ操作ですが、使用している表示によって処理がわずかに異なります。

使用可能な任意の表示方法で、リソースを表示、ナビゲーションおよび（追加のアクションを行うために）選択できます。

* 列表示
* カード表示
* リスト表示

### カード表示

![](assets/card-view.png)

カード表示では、現在のレベルの各項目の情報カードが表示されます。これらのカードには、次の詳細が表示されます。

* アセット／フォルダーの内容を視覚的に表現したもの。
* 種類
* タイトル
* 名前
* アセットがAEMからBrand Portalに公開された日時
* サイズ
* ディメンション寸法

カードをクリックして階層の下位に移動したり（クイックアクションを回避するために慎重に行う）、ヘッダーの [ パンくずリスト ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/authoring/essentials/basic-handling) を使用して再度上位に移動したりできます。

![](assets/cardquickactions.png)

#### 管理者以外のユーザー向けカード表示

カード表示のフォルダーのカードは、管理者以外のユーザー（編集者、閲覧者、およびゲストユーザー）にフォルダー階層情報を表示します。この機能を使用すると、親階層について、アクセス中のフォルダーの場所をユーザーに知らせることができます。

フォルダー階層情報は、別のフォルダー階層から共有された、他のフォルダーと類似した名前のフォルダーを区別するのに特に役立ちます。 管理者以外のユーザーが、共有されているアセットのフォルダー構造に気付かない場合は、類似した名前を持つアセットやフォルダーは混乱するように見えます。

* それぞれのカードに表示されるパスは、カードのサイズに合わせて切り詰めて表示されます。ただし、ユーザーは、切り詰められたパスにカーソルを合わせると、フルパスをツールチップとして表示できます。

![](assets/folder-hierarchy1.png)

**アセットのプロパティを表示する「概要」オプション**

概要オプションは管理者以外のユーザー（エディター、閲覧者、ゲストユーザー）が使用して、選択したアセットやフォルダーのアセットプロパティを表示できます。 「概要」オプションは、次の場所に表示されます。

* 上部のツールバーでアセット/フォルダーを選択します。
* ドロップダウンで、パネルセレクターを選択します。

アセットやフォルダーを選択した状態で「**[!UICONTROL 概要]**」オプションを選択すると、タイトル、パス、アセット作成時間を確認できます。 一方、アセットの詳細ページで「概要」オプションを選択すると、アセットのメタデータを確認できます。

![](assets/overview-option.png)

![](assets/overview-rail-selector.png)

#### カード表示で設定を表示

**[!UICONTROL ビュー設定]** ダイアログボックスが開きます。そのためには、ビューセレクターから **[!UICONTROL ビュー設定]** を選択します。 これにより、カード表示でアセットのサムネールのサイズを変更できます。 この方法で、ビューをパーソナライズし、表示するサムネールの数を制御することができます。

![](assets/cardviewsettings.png)

### リスト表示

![](assets/list-view.png)

リスト表示では、現在のレベルの各リソースの情報が表示されます。 リスト表示には、次の詳細が表示されます。

* アセットのサムネール画像
* 名前
* タイトル
* ロケール
* 種類
* 寸法
* サイズ
* レーティング
* アセット階層画像を示すフォルダーパス
* Brand Portal 上のアセットの公開日

パス列を使用すると、フォルダー階層内のアセットの場所を簡単に識別できます。 リソース名をクリックして階層を下に移動し、ヘッダーの [ パンくずリスト ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/authoring/essentials/basic-handling) を使用して戻ることができます。

<!--
Comment Type: draft lastmodifiedby="mgulati" lastmodifieddate="2018-08-17T03:12:05.096-0400" type="annotation">Removed:- "Selecting assets in list view To select all items in the list, use the checkbox at the upper left of the list. When all items in the list are selected, this check box appears checked. To deselect all, click the checkbox. When only some items are selected, it appears with a minus sign. To select all, click the checkbox. To deselect all, click the checkbox again. You can change the order of items using the dotted vertical bar at the far right of each item in the list. Click the vertical selection bar and drag the item to a new position in the list."
 -->

### リスト表示の表示設定

リスト表示では、デフォルトでアセット **[!UICONTROL 名前]** が最初の列として表示されます。 アセットの&#x200B;**[!UICONTROL タイトル]**、**[!UICONTROL ロケール]**、**[!UICONTROL タイプ]**、**[!UICONTROL ディメンション]**、**[!UICONTROL サイズ]**、**[!UICONTROL レーティング]**、公開状態などの追加情報も表示されます。ただし、「**[!UICONTROL 表示設定]**」を使用して、表示する列を選択することもできます。

![](assets/list-view-setting.png)

### 列表示

![](assets/column-view.png)

列表示を使用して、一連のカスケード表示された列間をコンテンツツリーで移動します。 この表示は、アセット階層の視覚化とトラバースに役立ちます。

最初（一番左）の列でリソースを選択すると、2 番目の列の右側に子リソースが表示されます。 2 列目でリソースを選択すると、右側の 3 列目に子リソースが表示され、以下同様に表示されます。

ツリー内を上下に移動できます。 リソース名またはリソース名の右側にある山形記号をクリックします。

* リソース名と山形記号は、クリックするとハイライト表示されます。
* サムネールをタップまたはクリックすると、リソースが選択されます。
* 選択すると、チェックマークがサムネールにオーバーレイ表示され、リソース名がハイライト表示されます。
* 選択されたリソースの詳細が最後の列に表示されます。

列表示でアセットを選択すると、アセットが次の詳細と共に最後の列に視覚的に表示されます。

* タイトル
* 名前
* ディメンション寸法
* アセットがAEMからBrand Portalに公開された日時
* サイズ
* 種類
* アセットの詳細ページに表示される「詳細」オプション

<!--
Comment Type: draft

<h3>Selecting Resources</h3>
-->

<!--
Comment Type: draft

<p>Selecting a specific resource depends on a combination of the view and the device:</p>
-->

<!--
Comment Type: draft

<table border="1" cellpadding="1" cellspacing="0" width="100%">
<tbody>
<tr>
<td> </td>
<td>Select</td>
<td>Deselect</td>
</tr>
<tr>
<td>Column View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
<tr>
<td>Card View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap-and-hold the card</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the card</li>
<li>Mobile device:<br /> Tap the card</li>
</ul> </td>
</tr>
<tr>
<td>List View</td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
</tbody>
</table>
-->

<!--
Comment Type: draft

Deselecting All
-->

<!--
Comment Type: draft

<p>In all cases, as you select items the count of the items selected is displayed at the upper right of the toolbar.</p>
<p>You can deselect all items and exit selection mode by clicking the X next to the count.</p>
-->

<!--
Comment Type: draft

<p>In all views, all items can be deselected by clicking escape on the keyboard if you are using a desktop device.</p>
-->

## コンテンツツリー {#content-tree}

これらの表示に加え、3 つのツリー表示を使用して、目的のアセットやフォルダーを表示および選択しながらアセット階層をドリルダウンします。

ツリービューを開くには、左上のパネルセレクターをクリックし、メニューから **[!UICONTROL コンテンツツリー]** を選択します。

![](assets/contenttree.png)

コンテンツ階層から目的のアセットに移動します。

![](assets/content-tree.png)

## アセットの詳細 {#asset-details}

アセットの詳細ページでは、アセットの表示、ダウンロード、アセットのリンクの共有、コレクションへの移動、アセットのプロパティページの表示を行うことができます。 同じフォルダーにある他のアセットの詳細ページを順番に移動することもできます。

![](assets/asset-detail.png)

アセットのメタデータを表示したり、様々なレンディションを表示したりするには、アセットの詳細ページのパネルセレクターを使用します。

![](assets/asset-overview.png)

アセットの詳細ページでアセットの利用可能なレンディションをすべて表示し、「**[!UICONTROL レンディション]** パネルからレンディションを選択してプレビューできます。

![](assets/renditions.png)

<!-- removed as it is fixed in 2022.02.0 release
>[!CAUTION]
>
>(**Experience Manager Assets as a Cloud Service** only) The following known issues will be fixed in the upcoming release:
>
>The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal after December 16, 2021.
>
>The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
-->

アセットのプロパティページを開くには、上部のバーにある **[!UICONTROL プロパティ （p）]** オプションを使用します。

![](assets/asset-properties.png)

また、アセットの関係も AEM から Brand Portal に公開されているので、アセットのプロパティページですべての関連アセット（AEM 上のソースまたは派生アセット）のリストを表示することもできます。
