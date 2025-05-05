---
title: Brand Portal へのタグの公開
description: Experience Manager Assets から Brand Portal にタグを公開する方法について説明します。
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
exl-id: 842656a6-1a2b-4b64-954d-1e663923a1a1
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 38%

---

# Brand Portal へのタグの公開 {#publish-tags-to-brand-portal}

Experience Manager Assets から Brand Portal にタグを公開する方法について説明します。

タグは、アセットを整理したり、アセットが関連付けられているアセットの検索性を高めたりするのに役立ちます。 タグは、アセットに添付されるキーワードまたはラベル（メタデータ）と考えることができ、検索結果としてアセットをすばやく見つけることができます。 Experience Manager Assets でアセットにタグを割り当てる方法については、[タグを使用したアセットの構成](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/managing/organize-assets)を参照してください。

関連タグの付いたアセット（およびコレクション）が Brand Portal に公開されると、（AEM でアセットやコレクションに関連付けられた）タグが Brand Portal に自動公開されます。公開されたタグは、そのタグに関連付けられているアセットを検索で探す際に役立ちます。

>[!NOTE]
>
>Adobeでは、タグが関連付けられているアセット（およびコレクション）を公開する前に、タグをBrand Portalにのみ公開することをお勧めします。 このアプローチにより、アセット（およびコレクション）をBrand Portalにすばやく公開できます。

## タグを管理 {#manage-tags}

既存のタグを使用してアセットに添付したり、AEM タグコンソール（**[!UICONTROL ツール | タグ付け | AEM タグ]**）。 どちらのシナリオでも、まずタグをBrand Portalに公開し、次に適切なアセットに関連付ける必要があります。

AEMでタグを作成し、Brand Portalでタグを公開し、適切なアセット（またはコレクション）にタグを関連付けるには、次の手順に従います。

1. **タグを作成**
管理者権限でAEM オーサーインスタンスにログインし、グローバルナビゲーションから **[!UICONTROL AEM タグ]** コンソールにアクセスします。

   1. 「**[!UICONTROL ツール]**」を選択します

   1. 「**[!UICONTROL 一般]**」を選択します

   1. 「**[!UICONTROL タグ付け]**」を選択します

1. **[!UICONTROL 作成]** を選択してから、「**[!UICONTROL タグを作成]**」オプションを選択します。
1. 以下を指定します。

   * **[!UICONTROL タイトル]**

     *（必須）*&#x200B;タグの表示タイトル。
   * **[!UICONTROL 名前]**

     *（必須）*&#x200B;タグの名前。指定しない場合、有効なノード名が「タイトル」から作成されます。[タグ ID](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/implementing/developing/platform/tagging/framework) を参照してください。
   * **説明**

     *（オプション）*&#x200B;タグの説明。
   * **タグのパス** タグの JCR パス。

1. 「**[!UICONTROL 送信]**」を選択すると、タグが作成されます。

   AEM インスタンスでタグを作成すると、そのタグをアセットに添付できるようになります（そのアセットの「プロパティ」セクションまたは「タグを管理」セクションを使用）。

1. **タグを Brand Portal に公開します**。

   **[!UICONTROL AEM タグ]** コンソール（[!UICONTROL &#x200B; ツール | タグ付け | AEM Tags]）で目的のタグを選択し、Brand PortalにPublishします。

1. **タグをアセット（またはコレクション）に関連付けます**。

   アセット（またはコレクション）を選択し、そのアセットの「プロパティ」セクションまたは「タグを管理」セクションを使用して目的のタグを添付します。 AEM Assetsでアセットにタグを割り当てる方法について詳しくは、[ タグを使用したアセットの整理 ](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/managing/organize-assets) を参照してください。

1. **アセット（またはコレクション）を Brand Portal に公開します**。\
   アセット（またはコレクション）を Brand Portal に公開すると、関連付けられているタグも Brand Portal 上で利用できるようになります。

   Brand Portalの各アセット（またはコレクション）に添付されたタグを表示するには、Brand Portalにログインしてからアセットを選択します。 「プロパティ」セクションで、添付されたタグが表示されます。

## 昇格を検索 {#search-promote}

AEM Assets Brand Portalを使用すると、特定のアセットをキーワードのタグに基づく検索の上位の結果として取り込むことができます。

アセットを昇格させる検索キーワードを設定するには、次のようにします。

1. AEM オーサーインスタンスでアセットの&#x200B;**[!UICONTROL プロパティ]**&#x200B;ページを開きます。
1. 「**[!UICONTROL 詳細]**」タブに移動します。
1. 「**[!UICONTROL 検索キーワード用に昇格]**」セクションの **[!UICONTROL 検索の昇格]** で、**[!UICONTROL 追加]** を選択して検索キーワードまたはタグを追加します。

   ![](assets/search-promote.png)

1. 変更内容を保存します。
1. アセットをBrand PortalにPublishします。
1. Brand Portalにログインします。 アセットの **[!UICONTROL プロパティ]** セクションの **[!UICONTROL 詳細]** タブを表示します。
なお、アセットのプロパティには「**[!UICONTROL 昇格を検索]**」のキーワードも表示されます。
