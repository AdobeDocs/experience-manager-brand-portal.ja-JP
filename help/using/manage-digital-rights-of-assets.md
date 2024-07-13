---
title: アセットのデジタル著作権の管理
seo-title: Manage digital rights of assets
description: アセットのライセンスを供与したり、アセットや共有リンクの有効期限を設定したりすることで、アセットの使用を制御し、アセットを保護できます。
seo-description: Licensing assets and setting expiration for assets and shared links ensure controlled usage of these assets and safeguard them.
uuid: ce30e398-0109-41bf-a4d2-2fcca476f499
contentOwner: bdhar
topic-tags: download-install
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: f77003ba-31fe-4a9e-96c8-dbc4c2eba79e
role: Admin
exl-id: 86c31891-0627-41ca-b571-8dac3a074d55
source-git-commit: d1487434b10b01eaf55f34672267490fd8fd907e
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 81%

---

# アセットのデジタル著作権の管理 {#manage-digital-rights-of-assets}

ブランドを守るには、クリエイティブアセットやブランドマテリアルの配布および使用を適切に保護することが不可欠です。これを組織の内外にわたって確実に適用するには、AEM から Brand Portal に公開される承認済みアセットに有効期限の日時を設定したり、アセットの条件付き使用を認めるライセンスを供与したりします。また、Brand Portalでは、Brand Portalから共有されるアセットへのリンクの有効期限を指定できます。

Brand Portalでのアセットの保護方法と、関連する使用権限について説明します。

## アセットの有効期限 {#asset-expiration}

アセットの有効期限は、Brand Portal 上の承認済みアセットの使用を組織全体にわたって制御する有効な方法です。AEM Assets から Brand Portal に公開されるアセットには必ず有効期限日が設定されており、この設定によって、様々なユーザーの役割によるアセットの使用が制限されています。

### 期限切れアセットに関連する使用権限 {#usage-permissions-expired-assets}

Brand Portalでは、管理者は、期限切れのアセットの表示、ダウンロードおよびコレクションへの追加を行うことができます。 一方、編集者と閲覧者にできるのは、期限切れアセットの表示とコレクションへの追加だけです。

管理者は期限切れアセットを AEM Assets から Brand Portal に公開できます。しかし、期限切れアセットを Brand Portal からリンクを介して共有することはできません。期限切れアセットと期限切れでないアセットの両方を含むフォルダーから期限切れアセットを選択している場合は、「**[!UICONTROL リンクを共有]**」アクションは使用できません。しかし、期限切れアセットと期限切れでないアセットを含んだフォルダーそのものを選択している場合は、「[!UICONTROL 共有]」アクションと「**[!UICONTROL リンクを共有]**」アクションを使用できます。

>[!NOTE]
>
>フォルダーは、その中に期限切れアセットが含まれている場合でも、リンクとして共有できます。その場合、共有されたリンクは期限切れアセットをリストせず、期限切れでないアセットのみが共有されます。

以下の表に、期限切れアセットの使用権限を示します。

|   | **[!UICONTROL リンク共有]** | **[!UICONTROL ダウンロード]** | **[!UICONTROL プロパティ]** | **[!UICONTROL コレクションに追加]** | **[!UICONTROL 削除]** |
|---|---|---|---|---|---|
| **[!UICONTROL 管理者]** | 使用不可 | 使用可 | 使用可 | 使用可 | 使用可 |
| **[!UICONTROL 編集者]** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |
| **[!UICONTROL 閲覧者]** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |
| **[!UICONTROL ゲストユーザー]** | 使用不可 | 使用不可 | 使用可 | 使用可 | 使用不可 |

>[!NOTE]
>
>閲覧者およびエディターが期限切れアセットと期限切れでないアセットを含むフォルダーをダウンロードした場合は、期限切れでないアセットのみがダウンロードされます。フォルダーに期限切れのアセットのみが含まれている場合は、空のフォルダーがダウンロードされます。

### アセットの有効期限切れステータス {#expiration-status-of-assets}

アセットの有効期限ステータスは&#x200B;**[!UICONTROL カード表示]**&#x200B;で確認できます。カードの赤いフラグは、アセットの有効期限が切れたことを示します。

![](assets/expired_assets_cardview.png)

>[!NOTE]
>
>リスト表示と列表示には、アセットの有効期限ステータスは表示されません。

## アセットリンクの有効期限 {#asset-link-expiration}

管理者およびエディターは、リンクを通じてアセットを共有する一方で、**[!UICONTROL リンク共有]**&#x200B;ダイアログボックスの「**[!UICONTROL 有効期限]**」フィールドを使用して有効期限の日時を設定できます。リンクのデフォルトの有効期限は、リンクが共有された日から 7 日間です。

![](assets/asset-link-sharing.png)

これにより、リンクとして共有されたアセットは Brand Portal の管理者およびエディターが設定した日時に期限切れになり、その後は表示もダウンロードもできなくなります。リンクを通じて共有されたアセットは、組織の一員でない外部ユーザーからも見られるので、有効期限を指定することで、承認済みアセットを保護し、指定の日時以降は未知の人物に見られないようにすることができます。

リンク共有について詳しくは、[アセットをリンクとして共有](../using/brand-portal-link-share.md)を参照してください。

## ライセンスで保護されたアセット {#licensed-assets}

ライセンスで保護されたアセットを Brand Portal からダウンロードするときは、事前に使用許諾契約への同意が求められます。ライセンス取得済みアセットに関するこの契約書は、Brand Portalから直接アセットをダウンロードする場合、または共有リンクを使用してダウンロードする場合に交付されます。 ライセンスで保護されたアセットは、有効期限が切れているかどうかにかかわらず、すべてのユーザーが表示できます。 ただし、期限切れのライセンス済みアセットのダウンロードと使用は制限されています。 期限切れのライセンス済みアセットの動作と、ユーザーの役割に基づいて許可されるアクティビティについて詳しくは、[ 期限切れアセットの使用権限 ](../using/manage-digital-rights-of-assets.md#usage-permissions-expired-assets) を参照してください。

ライセンスで保護されているアセットには、[使用許諾契約が添付](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/drm.html?lang=ja)されています。この処理は、[!DNL Experience Manager Assets] のメタデータプロパティを設定することで行われます。

アセットに次のいずれかまたは両方のメタデータプロパティが含まれている場合、アセットは保護されていると見なされます。

* `xmpRights:WebStatement`：このプロパティが、そのアセットの使用許諾契約書を含むページのパスを指している。`xmpRights:WebStatement` は、リポジトリ内の有効なパスである必要があります。
* `adobe_dam:restrictions`：このプロパティの値が、使用許諾契約書を指定する変換前の HTML である。


ライセンスで保護されたアセットをダウンロードする場合は、メタデータプロパティに応じて&#x200B;**[!UICONTROL 著作権管理]**&#x200B;ページを指定できます。

| `adobe_dam:restrictions` | `xmpRights:WebStatement` | 著作権管理 |
| --- | --- | --- |
| はい | - | このインターフェイスは、Assets と Brand Portal の両方に表示されます |
| - | はい（無効なパス） | インターフェイスなし |
| はい | はい（無効なパス） | インターフェイスなし |
| はい | はい（有効なパス） | このインターフェイスは、パスが Assets と Brand Portal のどちらに対して有効か（または両方に有効か）に応じて Assets または Brand Portal </br> に表示されます。 |

![](assets/asset-copyright-mgmt.png)

ここでダウンロードするアセットを選択し、関連付けられた使用許諾契約に同意する必要があります。使用許諾契約に同意しない場合、「**[!UICONTROL ダウンロード]**」ボタンは無効になります。

![](assets/licensed-asset-download-2.png)

選択した項目に保護されたアセットが複数含まれている場合、一度に 1 つずつアセットを選択し、使用許諾契約書に同意し、アセットのダウンロードに進みます。

## 期限切れアセットに関するレポートの生成 {#generate-report-about-expired-assets}

管理者は、特定の期間内に期限切れになったすべてのアセットをリストするレポートを生成してダウンロードできます。このレポートには、期限切れアセットについての詳細情報（サイズ、種類、アセット階層内のアセットの場所を示すパス、アセットが期限切れになった日時、アセットが公開された日時など）が含まれます。このレポートの列はカスタマイズ可能であり、表示するデータを要件に応じて増やすことができます。

![](assets/assets-expired.png)

レポートの機能について詳しくは、[レポートの操作](../using/brand-portal-reports.md#work-with-reports)を参照してください。
