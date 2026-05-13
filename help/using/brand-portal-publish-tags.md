---
title: Brand Portal へのタグの公開
description: Experience Manager Assets から Brand Portal にタグを公開する方法について説明します。
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
exl-id: 842656a6-1a2b-4b64-954d-1e663923a1a1
TQID: https://experienceleague.adobe.com/5U3958LUe-Pw2LMcX9fEDKIYHU6IVQ-J4CeKlmBFuKo
product_v2:
  - id: d09181b5-a36a-43de-ba01-36641440bc43
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: e48edcb1ed5d76686794f7a7ed6389c7f4ab1ed3
workflow-type: tm+mt
source-wordcount: 639
ht-degree: 34%

---

# Brand Portal へのタグの公開 {#publish-tags-to-brand-portal}

Experience Manager Assets から Brand Portal にタグを公開する方法について説明します。

タグは、アセットを整理し、関連するアセットの検索性を向上させるのに役立ちます。 タグは、アセットに添付されたキーワードやラベル（メタデータ）と考えることができ、検索の結果としてアセットをすぐに見つけることができます。 Experience Manager Assets でアセットにタグを割り当てる方法については、[タグを使用したアセットの構成](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/organize-assets)を参照してください。

関連タグの付いたアセット（およびコレクション）が Brand Portal に公開されると、（AEM でアセットやコレクションに関連付けられた）タグが Brand Portal に自動公開されます。 公開されたタグは、そのタグに関連付けられているアセットを検索で探す際に役立ちます。

>[!NOTE]
>
>Adobeでは、タグが関連付けられているアセット（およびコレクション）を公開する前に、Brand Portalにタグを公開することをお勧めします。 このアプローチにより、アセット（およびコレクション）をBrand Portalにすばやく公開できます。

## タグの管理 {#manage-tags}

既存のタグを使用して、アセットにアタッチしたり、AEM タグコンソール（**[!UICONTROL ツール | タグ付け| AEM タグ]**）から新しいタグを作成したりできます。 どちらの場合も、最初にタグをBrand Portalに公開してから、適切なアセットに関連付ける必要があります。

AEMでタグを作成し、Brand Portalでタグを公開し、タグを適切なアセット（またはコレクション）に関連付けるには、次の手順に従います。

1. **タグを作成**
管理者権限でAEM オーサーインスタンスにログインし、グローバルナビゲーションから&#x200B;**[!UICONTROL AEM Tags]** コンソールにアクセスします。

   1. 「**[!UICONTROL ツール]**」を選択します

   1. 「**[!UICONTROL 一般]**」を選択します

   1. 「**[!UICONTROL タグ付け]**」を選択します

1. 「**[!UICONTROL Create]**」を選択し、「**[!UICONTROL タグを作成]**」オプションを選択します。
1. 以下を指定します。

   * **[!UICONTROL タイトル]**
     *（必須）*&#x200B;タグの表示タイトル。
   * **[!UICONTROL 名]**
     *（必須）*&#x200B;タグの名前。 指定しない場合、有効なノード名が「タイトル」から作成されます。 [タグ ID](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/tagging/framework) を参照してください。
   * **説明**
     *（オプション）*&#x200B;タグの説明。
   * **タグパス**
タグのJCR パス。

1. 「**[!UICONTROL 送信]**」を選択すると、タグが作成されます。

   AEM インスタンスでタグを作成した後、そのタグをアセットに添付できます（「プロパティ」セクションまたは「タグを管理」セクションを使用）。

1. **タグを Brand Portal に公開します**。

   **[!UICONTROL AEM Tags]** コンソール （[!UICONTROL &#x200B; ツール | タグ付け| AEM Tags]）に移動し、目的のタグを選択してBrand Portalに公開します。

1. **タグをアセット（またはコレクション）に関連付けます**。

   アセット（またはコレクション）を選択し、そのアセットの「プロパティ」セクションまたは「タグを管理」セクションを使用して、目的のタグを添付します。 AEM Assetsでアセットにタグを割り当てる方法について詳しくは、[&#x200B; タグを使用したアセットの整理](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/organize-assets)を参照してください。

1. **アセット（またはコレクション）を Brand Portal に公開します**。\
   アセット（またはコレクション）を Brand Portal に公開すると、関連付けられているタグも Brand Portal 上で利用できるようになります。

   Brand Portalの各アセット（またはコレクション）に添付されたタグを表示するには、Brand Portalにログインして、アセットを選択します。 「プロパティ」セクションで、添付されたタグを確認できます。

## 昇格を検索 {#search-promote}

AEM Assets Brand Portalでは、特定のアセットをキーワードタグにもとづいた検索結果の上位に表示することができます。

アセットを昇格させる検索キーワードを設定するには、次のようにします。

1. AEM オーサーインスタンスでアセットの&#x200B;**[!UICONTROL プロパティ]**&#x200B;ページを開きます。
1. 「**[!UICONTROL 詳細]**」タブに移動します。
1. **[!UICONTROL 検索キーワードの昇格]** セクション内の&#x200B;**[!UICONTROL 検索プロモーション]**&#x200B;で、**[!UICONTROL 追加]**&#x200B;を選択して検索キーワードまたはタグを追加します。

   ![](assets/search-promote.png)

1. 変更内容を保存します。
1. Brand Portalにアセットを公開します。
1. Brand Portalにログインします。 アセットの「**[!UICONTROL プロパティ]**」セクションの「**[!UICONTROL 詳細]**」タブを表示します。
なお、アセットのプロパティには「**[!UICONTROL 昇格を検索]**」のキーワードも表示されます。
