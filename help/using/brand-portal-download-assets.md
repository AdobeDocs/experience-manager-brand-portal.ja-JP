---
title: アセットをダウンロード
description: すべてのユーザーがアクセス可能なアセットとフォルダーを同時にダウンロードできるので、承認済みのブランドアセットをオフラインで使用するために安全に配布できます。
content-type: reference
contentOwner: Vishabh Gupta
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: download, download-install, download assets
exl-id: be264b1c-38d9-4075-b56a-113f34a2c6bf
source-git-commit: f483ac280a5e89ca25305eae09380d70ad661752
workflow-type: tm+mt
source-wordcount: '1909'
ht-degree: 64%

---

# アセットをダウンロード {#download-assets-from-bp}

Adobe Experience Manager Assets Brand Portalでは、Brand Portalからアクセス可能なアセットやフォルダーをユーザーが同時にダウンロードできるので、ダウンロードエクスペリエンスが強化されます。 つまり、承認されたブランドアセットを安全に配布して、オフラインで使用できます。 以下では、Brand Portal からアセット（承認済みアセット）をダウンロードする方法や、期待される[ダウンロードパフォーマンス](#expected-download-performance)などについて説明します。


>[!NOTE]
>
>Brand Portal 2020.10.0 （およびそれ以降）では、「**[!UICONTROL 高速ダウンロード]**」設定がデフォルトで有効になっており、IBM® Aspera Connect を使用してアセットのダウンロードが高速化されます。 Brand Portalからアセットをダウンロードする前に、ブラウザーの拡張機能にIBM® Aspera Connect 3.9.9 （`https://www.ibm.com/docs/en/aspera-connect/3.9.9`）をインストールしてください。 [Brand Portalからのダウンロードを高速化するためのガイド ](../using/accelerated-download.md) を参照してください。
>
>IBM® Aspera Connect を使用せずに通常のダウンロードプロセスを続行する場合は、Brand Portal管理者に連絡して **[!UICONTROL 高速ダウンロード]** 設定をオフにしてもらってください。

## アセットのダウンロード設定 {#configure-download}

Brand Portal管理者は、Brand Portal ユーザーのアセットのダウンロードとユーザーグループの設定を行うことができます。 この機能を使用すると、Brand Portal インターフェイスからアセットレンディションにアクセスしてダウンロードできます。

>[!NOTE]
>
>ユーザーインターフェイスのダウンロード設定を使用すると、Brand Portal ユーザーはセルフサービスエクスペリエンスを利用して、アセットレンディションを簡単に設定およびダウンロードできます。 アプリケーションレイヤーでのアセットのダウンロードは制限されません。例えば、完全な URL パスを使用してアセットレンディションにアクセスしたり、アセットレンディションをダウンロードしたりすることが引き続き可能です。

次の設定は、Brand Portal インターフェイスからアセットレンディションにアクセスしてダウンロードする方法を定義するものです。

* ダウンロード設定の有効化
* ユーザーグループ設定の指定

### ダウンロード設定の有効化 {#enable-download-settings}

管理者は、**[!UICONTROL ダウンロード設定]** を有効にして、Brand Portal ユーザーがダウンロードにアクセスできるレンディションのセットを定義できます。

使用可能な設定は次のとおりです。

* **[!UICONTROL 高速ダウンロード]**

  IBM® Aspera Connect を使用してアセットのダウンロードを高速化します。 デフォルトでは、「**[!UICONTROL ダウンロード設定]**」の「**[!UICONTROL 高速ダウンロード]**」設定が有効になっています。

* **[!UICONTROL カスタムレンディション]**

  アセットのカスタムレンディションおよび（または）動的レンディションのダウンロードを有効にします。

  元のアセットとシステム生成レンディション以外のすべてのアセットレンディションは、カスタムレンディションと呼ばれます。これには、アセットに使用できる静的レンディションと動的レンディションが含まれます。すべてのユーザーがExperience Manager Assetsでカスタムの静的レンディションを作成できますが、カスタムの動的レンディションを作成できるのは管理者のみです。 [ 画像プリセットまたは動的レンディションを適用する方法 ](../using/brand-portal-image-presets.md) を参照してください。

* **[!UICONTROL システムレンディション]**

  アセットのシステム生成レンディションのダウンロードを有効にします。

  これらのアセットは、「DAM アセットの更新」ワークフローに基づいて、Experience Manager Assetsで自動的に生成されるサムネールです。

* **[!UICONTROL アセットのダウンロード]**

  レンディションは、アセットごとに別個のフォルダーにダウンロードされます。 この設定は、20 個を超えるアセットのフォルダー、コレクション、一括ダウンロードに適用されます。


Brand Portal テナントに管理者としてログインし、**[!UICONTROL ツール]**／**[!UICONTROL ダウンロード]**&#x200B;に移動します。

管理者は、Brand Portal ユーザーがレンディションにアクセスしてダウンロードするための設定を任意に組み合わせることができます。

![](assets/download-settings-new.png)


>[!NOTE]
>
>管理者のみが、期限切れのアセットをダウンロードできます。有効期限が切れたアセットについて詳しくは、[アセットのデジタル著作権の管理](../using/manage-digital-rights-of-assets.md)を参照してください。

### ユーザーグループ設定の指定 {#configure-user-group-settings}

**[!UICONTROL ダウンロード設定]**&#x200B;に加えて、Brand Portal 管理者は、様々なユーザーグループが元のアセットとそのレンディションを表示および（または）ダウンロードするための設定をさらに指定できます。

Brand Portal テナントに管理者としてログインし、**[!UICONTROL ツール]**／**[!UICONTROL ユーザー]**&#x200B;に移動します。**[!UICONTROL ユーザーの役割]**&#x200B;ページで、「**[!UICONTROL グループ]**」タブに移動して、ユーザーグループの表示および（または）ダウンロード設定を指定します。

![view-download-permission](assets/download-permissions.png)

>[!NOTE]
>
>ユーザーが複数のグループに追加されていて、そのいずれかのグループが制約を受ける場合、そのユーザーにも制約が適用されます。

設定に基づいて、スタンドアロンのアセット、複数のアセット、アセットを含むフォルダー、ライセンス済みまたは未ライセンスのアセット、共有リンクを使用したアセットのダウンロードでは、ダウンロードワークフローは一定になります。

次の表は、ユーザーがレンディションにアクセスできるかどうかを[ダウンロード設定](#configure-download)に応じて定義したものです。

| **ダウンロード設定：カスタムレンディション** | **ダウンロード設定：システムレンディション** | **ユーザーグループ設定：オリジナルをダウンロード** | **ユーザーグループ設定：レンディションをダウンロード** | **結果** |
|---|---|---|---|---|
| オン | オン | オン | オン | すべてのレンディションを表示およびダウンロード |
| オン | オン | オフ | オフ | 元のアセットを表示 |
| オフ | オフ | オン | オン | 元のアセットの表示とダウンロード |
| オン | オフ | オン | オン | 元のアセットとカスタムレンディションを表示およびダウンロード |
| オフ | オン | オン | オン | 元のアセットとシステムレンディションを表示およびダウンロード |
| オン | オフ | オフ | オフ | 元のアセットを表示 |
| オフ | オン | オフ | オフ | 元のアセットを表示 |
| オフ | オフ | オフ | オン | 元のアセットを表示 |
| オフ | オフ | オン | オフ | 元のアセットの表示とダウンロード |
| オフ | オフ | オフ | オフ | 元のアセットを表示 |



## アセットのダウンロード {#download-assets}

Brand Portal ユーザーは、Brand Portal インターフェイスから複数のアセット、アセットを含んだフォルダー、コレクションをダウンロードできます。

>[!NOTE]
>
>アセットレンディションにアクセスまたはアセットレンディションをダウンロードする権限がない場合は、Brand Portal 管理者に問い合わせてください。

ユーザーがレンディションにアクセスできる場合は、次の機能を備えた強化版&#x200B;**[!UICONTROL ダウンロード]**&#x200B;ダイアログが提供されます。

* ダウンロードリストで任意のアセットの使用可能なすべてのレンディションを表示する。
* ダウンロードの必要がないアセットのレンディションを除外します。
* 1 回のクリックで、同じレンディションセットをすべての類似アセットタイプに適用する。
* アセットタイプごとに異なるレンディションセットを適用する。
* アセットごとに別個のフォルダーを作成する。
* 選択したアセットとレンディションをダウンロードする。

![download-dialog](assets/download-dialog-box.png)

>[!NOTE]
>
>**[!UICONTROL ダウンロード]**&#x200B;ダイアログが表示されるのは、**[!UICONTROL ダウンロード設定]**&#x200B;で「**[!UICONTROL カスタムレンディション]**」および（または）「**[!UICONTROL システムレンディション]**」が有効になっている場合のみです。


### アセットのダウンロード手順 {#bulk-download}

Brand Portal インターフェイスからアセットまたはアセットを含んだフォルダーをダウンロードする手順は次のとおりです。

1. Brand Portal テナントにログインします。デフォルトで「**[!UICONTROL ファイル]**」ビューが開き、公開中のアセットとフォルダーがすべて表示されます。

   次のいずれかの操作を行います。

   * ダウンロードするアセットまたはフォルダーを選択します。上部のツールバーで「**[!UICONTROL ダウンロード]**」アイコンをクリックします。

     ![select-multiple-assets](assets/select-assets-new.png)

   * アセットの特定のアセットレンディションをダウンロードするには、該当するアセットにポインターを置き、クイックアクションサムネールに表示される「**[!UICONTROL ダウンロード]**」アイコンをクリックします。

     ![select-asset](assets/select-asset.png)


     >[!NOTE]
     >
     >初めてアセットをダウンロードするときに、ブラウザーにIBM® Aspera Connect がインストールされていない場合は、Aspera ダウンロードアクセラレーター（`https://www.ibm.com/docs/en/aspera-connect/3.9.9`）をインストールするように求めるプロンプトが表示されます。


     >[!NOTE]
     >
     >ダウンロードしたアセットにライセンス済みアセットも含まれている場合は、**[!UICONTROL 著作権管理]** ページにリダイレクトされます。 このページで、アセットを選択し、「**[!UICONTROL 同意する]**」をクリックし、「**[!UICONTROL ダウンロード]**」をクリックします。「同意しない」を選択した場合は、ライセンスが必要なアセットはダウンロードされません。
     > 
     >ライセンスで保護されているアセットには、[ 使用許諾契約が添付 ](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/administer/drm) されています。この処理は、Experience Manager Assetsでアセットの [ メタデータプロパティ ](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/administer/drm) を設定することで行われます。


     ![licensed-asset](assets/licensed-asset-new.png)

1. 選択したすべてのアセットが一覧表示される&#x200B;**[!UICONTROL ダウンロード]**&#x200B;ダイアログが開きます。

   任意のアセットをクリックして使用可能なレンディションを表示し、ダウンロードするレンディションに対応するチェックボックスをオンにします。

   個々のアセットのレンディションを手動で選択または除外することができます。または、**適用** アイコンをクリックして、類似のアセットタイプ用にダウンロードするのと同じレンディションのセットを選択します（この例では、すべての画像ファイル）。 **[!UICONTROL すべてを適用]**&#x200B;ダイアログで、「**[!UICONTROL 完了]**」をクリックして、類似するすべてのアセットにルールを適用します。

   ![apply-all](assets/apply.png)

   また、**削除**&#x200B;アイコンをクリックして、（必要に応じて）ダウンロードリストからアセットを削除することもできます。

   ![remove](assets/remove.png)

   アセットのダウンロード時にBrand Portalのフォルダー構造を維持するには、「**[!UICONTROL `Create separate folder for each asset`]**」チェックボックスをオンにします。

   ダウンロードボタンは、選択した項目の数を反映しています。ルールの適用が完了したら、「**[!UICONTROL 項目をダウンロード]**」をクリックします。

   ![download-dialog](assets/download-dialog-box-new.png)

1. デフォルトでは「**[!UICONTROL ダウンロード設定]**」の「**[!UICONTROL 高速ダウンロード]**」設定が有効になっています。そのため、確認ボックスが表示され、IBM® Aspera Connect を使用してダウンロードを高速化できます。

   「**[!UICONTROL 高速ダウンロード]**」を引き続き使用するには、「**[!UICONTROL 許可]**」をクリックします。選択したすべてのレンディションが、IBM® Aspera Connect を使用して zip フォルダーにダウンロードされます。

   IBM® Aspera Connect を使用しない場合は、「**[!UICONTROL 拒否]**」をクリックします。「**[!UICONTROL 高速ダウンロード]**」が拒否された場合や失敗した場合は、エラーメッセージが表示されます。「**[!UICONTROL 通常のダウンロード]**」ボタンをクリックして、アセットのダウンロードを続行します。

<!-- removed the known issue from step 2 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issue will be fixed in the upcoming release:
   >
   >The download dialog lists the smart crop renditions of the selected asset, however, the user cannot download the smart crop renditions.
-->

>[!NOTE]
>
>管理者が「**[!UICONTROL 高速ダウンロード]**」設定をオフにした場合、選択したレンディションは、IBM® Aspera Connect を使用せずに、zip フォルダーに直接ダウンロードされます。

>[!NOTE]
>
>**[!UICONTROL ダウンロード設定]**&#x200B;で「**[!UICONTROL アセットのダウンロード]**」設定が有効になっている場合、アセットレンディションは、zip フォルダー内でアセットごとに別個のフォルダーにダウンロードされます。
>  
>共有リンクからアセットをダウンロードした場合、アセットレンディションは、zip フォルダー内でアセットごとに別個のフォルダーにダウンロードされます。
>
>ダウンロード対象としてフォルダー、コレクション、20 個を超えるアセットのいずれかを選択した場合、「**[!UICONTROL ダウンロード]**」ダイアログボックスは表示されません。 代わりに、アクセス可能なすべてのアセットレンディション（動的レンディションを除く）が zip フォルダーにダウンロードされます。

>[!NOTE]
>
>Brand Portalでは、Dynamic Mediaを – ハイブリッドモードとScene7 モードの両方で設定できます。
>
>（*Experience Manager Assets オーサーインスタンスが&#x200B;**Dynamic Media ハイブリッドモードで動作している場合***）
>
>動的レンディションをプレビューまたはダウンロードするには、Dynamic Media を有効化します。 アセットのピラミッド TIFF レンディションが、アセットの公開先のExperience Manager Assets オーサーインスタンスに存在することを確認します。 Experience Manager Assets から Brand Portal にアセットを公開すると、そのビラミッド TIFF レンディションも公開されます。

[ 管理者が元のレンディションへのアクセスを許可していない ](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) 場合、選択したアセットの元のレンディションをダウンロードすることはできません。

![no-access-message](assets/no-access-message.png)

<!-- This issue has been resolved, check with engineering.
>[!NOTE]
>
>Once you have downloaded the asset renditions, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.
-->

### アセットの詳細ページからのアセットのダウンロード {#download-assets-from-asset-details-page}

ダウンロードワークフローに加えて、個々のアセットのレンディションをアセットの詳細ページから直接ダウンロードする方法もあります。

ユーザーは、**[!UICONTROL ダウンロード]**&#x200B;ダイアログを開かなくても、アセットの詳細ページの&#x200B;**[!UICONTROL レンディション]**&#x200B;パネルから様々なアセットレンディションをプレビューし、特定のレンディションを選択して、アセットレンディションを直接ダウンロードすることができます。


アセットの詳細ページからアセットレンディションをダウンロードする手順は、次のとおりです。

1. Brand Portal テナントにログインし、アセットをクリックしてアセットの詳細ページを開きます。
1. 左側のオーバーレイアイコンをクリックし、「**[!UICONTROL レンディション]**」をクリックします。

   ![rendition-navigation](assets/rendition-navigation.png)

1. **[!UICONTROL レンディション]**&#x200B;パネルには、アセットの[ダウンロード設定](#configure-download)に基づいて、アクセス可能なアセットレンディションがすべて一覧表示されます。

   ダウンロードする特定のレンディションを選択し、「**[!UICONTROL 項目をダウンロード]**」をクリックします。

   ![レンディションパネル](assets/renditions-panel.png)


1. デフォルトでは「**[!UICONTROL ダウンロード設定]**」の「**[!UICONTROL 高速ダウンロード]**」設定が有効になっています。そのため、確認ボックスが表示され、IBM® Aspera Connect を使用してダウンロードを高速化できます。

   「**[!UICONTROL 高速ダウンロード]**」を引き続き使用するには、「**[!UICONTROL 許可]**」をクリックします。選択したすべてのレンディションが、IBM® Aspera Connect を使用して zip フォルダーにダウンロードされます。

   「**[!UICONTROL 高速ダウンロード]**」の使用を拒否すると、エラーメッセージが表示されます。「**[!UICONTROL 通常のダウンロード]**」ボタンをクリックして、アセットのダウンロードを続行します。

<!-- removed the known issue from step 3 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issues will be fixed in the upcoming release:
   >
   >The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal after December 16, 2021.
   >
   >The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
-->

>[!NOTE]
>
>管理者が「**[!UICONTROL 高速ダウンロード]**」設定をオフにした場合、選択したレンディションは、IBM® Aspera Connect を使用せずに、zip フォルダーに直接ダウンロードされます。


>[!NOTE]
>
>個別にダウンロードしたアセットは、アセットダウンロードレポートに表示されます。ただし、アセットを含んだフォルダーをダウンロードした場合は、そのフォルダーもアセットも、アセットダウンロードレポートに表示されません。

<!--
>[!NOTE]
>
>Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

<!-- Backup of content before updating the new feature docs.
## Configure asset download {#configure-download}

The download configuration allows the Brand Portal administrators to define the set of renditions available to the Brand Portal users for downloading the assets. The administrator can configure the asset **[!UICONTROL Download]** settings from the Brand Portal interface. 

The available configurations are:

* **[!UICONTROL Fast Download]** 

  Enables high-speed download of the assets. To know more, see [guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).

* **[!UICONTROL Custom Renditions]** 
  
  Download custom and (or) dynamic renditions of the assets. 
  All the asset renditions other than the original asset and system-generated renditions are called as custom renditions. It includes static as well as dynamic renditions available for the asset. Any user can create a custom static rendition in AEM Assets, whereas, only the AEM administrator can create custom dynamic renditions. To know more, see [how to apply image presets or dynamic renditions](../using/brand-portal-image-presets.md)

* **[!UICONTROL System Renditions]** 

  Download system-generated renditions of the assets. These are the thumbnails which are automatically generated in AEM Assets based on the "DAM update asset" workflow. 

Log in to your Brand Portal tenant as an administrator and navigate to **[!UICONTROL Tools]** > **[!UICONTROL Download]**. By default, the **[!UICONTROL Fast Download]** configuration is enabled in the **[!UICONTROL Download Settings]**. 

The administrators can enable any combination to configure the asset download process.

![](assets/download-configuration.png)


Based on the configuration, the download workflow remains constant for stand-alone assets, multiple assets, folders containing assets, licensed or unlicensed assets, and downloading assets using share link. 


* If both **[!UICONTROL Custom Renditions]** and **[!UICONTROL System Renditions]** configurations are turned-off, the original renditions of the assets are downloaded without any additional dialog being presented to the users.    


* If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled, an additional **[!UICONTROL Download]** dialog box appears wherein you can choose whether to download the original asset along with its renditions, or download only specific renditions. 

>[!NOTE]
>
>Only the administrators can download the expired assets. For more information about expired assets, see [manage digital rights of assets](../using/manage-digital-rights-of-assets.md).

## Steps to download assets {#steps-to-download-assets}

Following are the steps to download assets or folders containing assets from Brand Portal:

1. From the Brand Portal interface, do one of the following:

   * Select the folders or assets you want to download. From the toolbar at the top, click the **[!UICONTROL Download]** icon.

     ![](assets/downloadassets-1.png)

   * To download a specific asset or folder, hover the pointer over the asset or folder and click the **[!UICONTROL Download]** icon available in the quick action thumbnails.

     ![](assets/downloadsingleasset-1.png)


     >[!NOTE]
     >
     >If you are downloading the assets for the first time and do not have IBM Aspera Connect installed in your browser, it will prompt you to install the Aspera download accelerator. 


     >[!NOTE]
     >
     >If the assets you are downloading also include licensed assets, you are redirected to the **[!UICONTROL Copyright Management]** page. In this page, select the assets, click **[!UICONTROL Agree]**, and then click **[!UICONTROL Download]**. If you choose to disagree, licensed assets are not downloaded. 
     > 
     >License-protected assets have [license agreement attached]() to them, which is done by setting asset's [metadata property]() in Experience Manager Assets.


     ![](assets/licensed-asset-download-1.png)

     
     >[!NOTE]
     >
     >Ensure to select all the required asset renditions while downloading them from the asset details page, and click **[!UICONTROL Download]**. The selected renditions are downloaded to your local machine.
     > 
     >Once you download, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the downloaded renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.

     If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled in the **[!UICONTROL Download Settings]**, the **[!UICONTROL Download]** dialog appears with the **[!UICONTROL Asset(s)]** check box selected by default. If the **[!UICONTROL Fast Download]** configuration is enabled, the **[!UICONTROL Enable download acceleration]** check box is selected by default.

     ![](assets/download-dialog.png)

     >[!NOTE]
     >
     >If the downloading assets are image files, and you select only the **[!UICONTROL Asset(s)]** check box in the **[!UICONTROL Download]** dialog but are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) then no image files are downloaded and a notification appears, stating that you have been restricted by the administrator to access original renditions.

     ![](assets/restrictaccess-note.png)

1. To download the renditions in addition to the original assets, select the **[!UICONTROL Rendition(s)]** check box. However, if you want to download the system-generated renditions along with the custom renditions, clear the **[!UICONTROL Exclude System Renditions]** check box.

   ![](assets/download-system-rendition.png)

   * To download only the renditions, clear the **[!UICONTROL Asset(s)]** check box.

     >[!NOTE]
     >
     >By default, only the assets are downloaded. However, original renditions of image files are not downloaded if you are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708).

    * To share the selected assets with other users through a link, select the **[!UICONTROL Email]** check box. An email notification is sent to the users with the download link. To know how to download assets from shared links, see [downloading assets from shared links](../using/brand-portal-link-share.md#main-pars-header-1703469193).  

      ![](assets/download-link.png)

      >[!NOTE]
      >
      >The download link on email notification expires after 45 days.
      >
      >The administrators can customize email messages, that is, logo, description, and footer, using the [Branding](../using/brand-portal-branding.md) feature.


    * You can select a predefined image preset or create a custom dynamic rendition from the **[!UICONTROL Download]** dialog box. 

      To apply a [custom image preset to the asset and its renditions](../using/brand-portal-image-presets.md#applyimagepresetswhendownloadingimages), select the **[!UICONTROL Dynamic Rendition(s)]** check box. Specify the image preset properties (such as size, format, color space, resolution, and image modifier) to apply the custom image preset while downloading the asset and its renditions. To download only the dynamic renditions, clear the **[!UICONTROL Asset(s)]** check box.

      ![](assets/dynamic-rendition.png)

      >[!NOTE]
      >
      >Brand Portal supports configuring Dynamic Media in both - Hybird and Scene 7 mode. 
      >
      >(*If AEM author instance is running on **Dynamic Media Hybrid mode***)
      >
      >To preview or download dynamic renditions of an asset, ensure that the dynamic media is enabled and the asset's Pyramid tiff rendition exists at the AEM Assets author instance from where the assets have been published. When an asset is published to Brand Portal, its Pyramid tiff rendition is also published.
      
  
    * To preserve the Brand Portal folder hierarchy while downloading assets, select the **[!UICONTROL Create separate folder for each asset]** check box. By default, the Brand Portal folder hierarchy is ignored and all the assets are downloaded in one folder in your local system.

1. Click **[!UICONTROL Download]**.

   The assets (and renditions if selected) are downloaded as a zip file to your local folder. However, no zip file is created if a single asset is downloaded without any of the renditions. 

   If you are not [authorized by the administrator to have access to the original renditions](../using/brand-portal-adding-users.md#main-pars-procedure-202029708), the original renditions of the selected assets are not downloaded. 

   >[!NOTE]
   >
   >Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

## 期待されるダウンロードパフォーマンス {#expected-download-performance}

ユーザーのクライアントが様々な場所にある場合、ファイルのダウンロードエクスペリエンスは、ローカルのインターネット接続やサーバーのレイテンシなどの要因によって異なります。様々なクライアントの場所で観測された 2 GB ファイルの予想されるダウンロードパフォーマンスは次のとおりです。米国オレゴンにあるBrand Portal サーバーの場合は、次のようになります。

| クライアントの場所 | クライアントとサーバーの間のレイテンシ | 予想されるダウンロード速度 | 2 GB ファイルのダウンロード所要時間 |
|-------------------------|-----------------------------------|-------------------------|------------------------------------|
| 米国西部 (北カリフォルニア) | 18 ミリ秒 | 7.68 MB/秒 | 4 分 |
| 米国西部 (オレゴン) | 42 ミリ秒 | 3.84 MB/秒 | 9 分 |
| 米国東部 (北バージニア) | 85 ミリ秒 | 1.61 MB/秒 | 21 分 |
| APAC（東京） | 124 ミリ秒 | 1.13 MB/秒 | 30 分 |
| ノイダ | 275 ミリ秒 | 0.5 MB/秒 | 68 分 |
| シドニー | 175 ミリ秒 | 0.49 MB/秒 | 69 分 |
| ロンドン | 179 ミリ秒 | 0.32 MB/秒 | 106 分 |
| シンガポール | 196 ミリ秒 | 0.5 MB/秒 | 68 分 |


>[!NOTE]
>
>引用したデータは、テスト条件下において確認されたものであり、レイテンシや帯域幅の異なる場所にいるユーザーの場合は結果が異なる可能性があります。
