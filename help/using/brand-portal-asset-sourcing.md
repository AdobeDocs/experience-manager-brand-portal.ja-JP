---
title: Brand Portal でのアセットソーシング
description: Adobe Experience Manager Assets Brand Portal でリリースされたアセットソーシング機能について説明します。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
sub-product: assets
topics: collaboration, content-velocity, sharing
doc-type: feature-video
activity: use
audience: author, marketer
version: Experience Manager 6.5
kt: 3838
exl-id: 2c132a7a-ed10-4856-8378-67939167ea60
source-git-commit: aea8becdf9493b1d465f1b1cb818c85f8943bedb
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 58%

---

# アセットソーシングの概要 {#overview-asset-sourcing-in-bp}

**アセットソーシング**&#x200B;を使用すると、追加の&#x200B;**アセット投稿**&#x200B;プロパティを持つ新しいフォルダーを Experience Manager Assets ユーザー（管理者／管理者以外のユーザー）が作成できるので、この新規作成フォルダーを Brand Portal ユーザーによるアセット送信に利用することができます。これにより、新しく作成された **投稿** フォルダー内に **SHARED** および **NEW** という 2 つのサブフォルダーが自動的にトリガーされます。 管理者は、投稿フォルダーに追加する必要があるアセットのタイプの概要をアップロードすることで、要件を定義します。 一連のベースラインアセットを **SHARED** フォルダーにアップロードして、Brand Portal ユーザーに必要な参照情報を提供します。 その後、管理者は、アクティブな Brand Portal ユーザーに投稿フォルダーへのアクセスを許可してから、新しく作成した&#x200B;**投稿**&#x200B;フォルダーを Brand Portal に公開することができます。**NEW** フォルダーへのコンテンツの追加を完了したら、投稿フォルダーをExperience Manager オーサー環境に公開できます。 なお、読み込みが完了し、新しく公開したコンテンツが Experience Manager Assets 内に反映されるまでに数分かかる場合があります。

また、既存の機能はすべてそのままで変わりません。Brand Portal ユーザーは、投稿フォルダーおよび許可された他のフォルダーからアセットを表示、検索およびダウンロードできます。さらに、管理者は投稿フォルダーの共有、プロパティの変更、コレクションへのアセットの追加を行うことができます。

![Brand Portal アセットソーシング](assets/asset-sourcing.png)

>[!VIDEO](https://video.tv.adobe.com/v/29365/?quality=12)

## 前提条件 {#prerequisites}

* Experience Manager Assets as a Cloud Service インスタンス、Experience Manager Assets 6.5.2 以降。
* Experience Manager Assets インスタンスと Brand Portal の連携が設定されていることを確認します。詳しくは、[Experience Manager Assets と Brand Portal の連携の設定](../using/configure-aem-assets-with-brand-portal.md)を参照してください。

<!--
* Ensure that your Brand Portal tenant is configured with one AEM Assets author instance.
-->

>[!NOTE]
>
>アセットソーシング機能は、Experience Manager Assets as a Cloud Service（Experience Manager Assets 6.5.9 以降）では、アセットソーシング機能がデフォルトで有効になっています。
>
>既存の設定は、以前のバージョンで引き続き機能します。

>[!NOTE]
>
>Experience Manager Assets 6.5.4 には既知の問題があります。Brand Portal ユーザーが、Adobe Developer Consoleにアップグレードすると、投稿フォルダーのアセットをExperience Manager Assetsに公開できなくなります。
>
>この問題は Experience Manager Assets 6.5.5 で修正されました。お使いの Experience Manager Assets インスタンスを最新のサービスパック AEM 6.5.5 にアップグレードし、Adobe 開発者コンソールで[設定をアップグレード](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65)してください。

<!--

>For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your author instance.
-->

<!--
## Configure Asset Sourcing {#configure-asset-sourcing}

**Asset Sourcing** is configured from within the AEM Assets author instance. The administrators can enable the Asset Sourcing feature flag configuration from the **AEM Web Console Configuration** and upload the active Brand Portal users list in **AEM Assets**.

>[!NOTE]
>
>Asset Sourcing is by default enabled on AEM Assets as a Cloud Service. The AEM administrator can directly upload the active Brand Portal users to allow them access to the Asset Sourcing feature.

>[!NOTE]
>
>Before you begin with the configuration, ensure that your AEM Assets instance is configured with Brand Portal. See, [Configure AEM Assets with Brand Portal](../using/configure-aem-assets-with-brand-portal.md). 

The following video demonstrates, how to configure Asset Sourcing on your AEM Assets author instance:

>[!VIDEO](https://video.tv.adobe.com/v/29771)
-->

<!--
### Enable Asset Sourcing {#enable-asset-sourcing}

AEM administrators can enable the Asset Sourcing feature flag from within the AEM Web Console Configuration (a.k.a Configuration Manager).

>[!NOTE]
>
>This step is not applicable for AEM Assets as a Cloud Service.


**To enable Asset Sourcing:**
1. Log in to your AEM Assets author instance and open Configuration Manager. 
Default URL: http:// localhost:4502/system/console/configMgr.
1. Search using the keyword **Asset Sourcing** to locate **[!UICONTROL Asset Sourcing Feature Flag Config]**.
1. Click **[!UICONTROL Asset Sourcing Feature Flag Config]** to open the configuration window.
1. Select the **[!UICONTROL feature.flag.active.status]** check box.
1. Click **[!UICONTROL Save]**.

![](assets/enable-asset-sourcing.png)
-->


### Brand Portal ユーザーリストのアップロード {#upload-bp-user-list}

Experience Manager Assets 管理者は、アクティブな Brand Portal ユーザーリストを含む Brand Portal ユーザー設定（.csv）ファイルを Experience Manager Assets にアップロードして、アセットソーシング機能へのアクセスを許可できます。

投稿フォルダーは、ユーザーリストで定義されたアクティブな Brand Portal ユーザーのみ共有できます。また、管理者は、設定ファイルに新規ユーザーを追加して、変更したユーザーリストをアップロードできます。

>[!NOTE]
>
>Experience Manager Assets インスタンスと Brand Portal の連携が設定されていることを確認します。詳しくは、[Experience Manager Assets と Brand Portal の連携の設定](../using/configure-aem-assets-with-brand-portal.md)を参照してください。

>[!NOTE]
>
>CSV ファイルの形式は、Admin Consoleでの一括ユーザー読み込みでサポートされている形式と同じです。 メールと氏名は必須です。

管理者は、Admin Consoleに新しいユーザーを追加できます。 詳しくは、[ ユーザーの管理 ](brand-portal-adding-users.md) を参照してください。 Admin Consoleでユーザーを追加したら、これらのユーザーをBrand Portal ユーザー設定ファイルに追加し、投稿フォルダーにアクセスする権限を割り当てることができます。

**Brand Portal ユーザーリストをアップロードするには：**

1. Experience Manager Assets インスタンスにログインします。
1. [!UICONTROL  ツール ] パネルから、**[!UICONTROL Assets]**/**[!UICONTROL Brand Portal ユーザー]** に移動します。

1. Brand Portal 投稿者をアップロードウィンドウが開きます。
ローカルマシンから参照し、アクティブなBrand Portal ユーザーリストを含む **設定（.csv** ファイルをアップロードします。
1. 「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/upload-user-list2.png)

管理者は、投稿フォルダーを設定する際に、このユーザーリスト内の特定のユーザーにアクセス権を付与できます。投稿フォルダーにアクセスしBrand PortalからExperience Manager Assetsにアセットを公開できるのは、投稿フォルダーに割り当てられたユーザーのみです。

## 関連トピック {#reference-articles}

* [Brand Portalへの投稿フォルダーの設定と公開](brand-portal-publish-contribution-folder-to-brand-portal.md)

* [Experience Manager Assets への投稿フォルダーの公開](brand-portal-publish-contribution-folder-to-aem-assets.md)
