---
title: Brand Portal のダウンロードの高速化
seo-title: Speed up the Brand Portal downloads
description: Brand Portal および共有リンクからのダウンロードパフォーマンスを強化します。
seo-description: Enhance download performance from Brand Portal and the shared links.
uuid: 2871137e-6471-49a7-872a-841bd92543d1
contentOwner: Vishabh Gupta
topic-tags: download-install, download assets
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 301f7a0b-5527-4aac-b731-bfc145fed0c0
exl-id: cf28df58-c6dd-4b12-8279-01351892009f
source-git-commit: ce765700aaecba4bfff7b55effb05f981b94bdec
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 99%

---

# Brand Portal のダウンロードの高速化 {#guide-to-accelerate-downloads-from-brand-portal}

<!-- This topic is woefully out of date. It talks at length about using a third party application whose URLs have a variety of problems. Topic should either be deleted or updated entirely to not talk about a specific third party application that Adobe has no control over. It also appears that the third party app is NOT free anymore. -->

Adobe Experience Manager Assets Brand Portal では、インストールオンデマンドアプリケーションである IBM® Aspera Connect との連携により、大きなアセットファイルのダウンロードパフォーマンスを向上させることができます。このアプリケーションは、TCP オーバーヘッドをなくす独自のテクノロジーを使用し、アセットファイルの転送速度を向上させます。この連携により、ダウンロードエクスペリエンスを確実に強化できます。

>[!NOTE]
>
>ダウンロード速度は、ネットワーク帯域幅、サーバーのレイテンシ、クライアントの所在地などの要因によって異なるので、ユーザーごとに異なります。

「**[!UICONTROL 高速ダウンロード]**」設定はデフォルトで有効になっているので、Brand Portal から目的のアセットファイルをダウンロードするのにかかる時間が大幅に短縮されます。

![](assets/download-settings-new.png)

## ファイルのダウンロードを高加速化するための前提条件 {#prerequisites-to-accelerate-file-download}

ファイルのダウンロードを高速化するには、必ず以下を行います。

* **[!UICONTROL ツール]**／**[!UICONTROL ダウンロード]**&#x200B;に移動し、**[!UICONTROL ダウンロード設定]**&#x200B;で、「**[!UICONTROL 高速ダウンロード]**」設定が有効になっていることを確認します。
* ファイアウォールのポート 33001（TCP と UDP の両方）が開いていることを確認します。
* 管理者権限を使用して、ブラウザーの拡張機能に **IBM® Aspera Connect 3.9.9 をインストール**&#x200B;します（[IBM® Asperra Connect のダウンロード](https://www.ibm.com/support/fixcentral/swg/selectFixes?parent=ibm%7EOther%20software&amp;product=ibm/Other+software/IBM+Aspera+Connect&amp;release=3.9.9&amp;platform=All&amp;function=all)）。

>[!NOTE]
>
>IBM® Aspera Connect には既知の問題があります。高速ダウンロードは、IBM® Aspera Connect バージョン 3.10 以降では機能しません。

## ダウンロードドメイン {#download-domains}

様々な地域で利用できるダウンロードドメインを以下に示します。

| 地域コード | ドメイン |
|---|---|
| NA OR1 | downloads-na1.brand-portal.adobe.com |
| NA VA5 | downloads-na2.brand-portal.adobe.com |
| EMEA LON5 | downloads-emea1.brand-portal.adobe.com |
| APAC SIN2 | downloads-apac1.brand-portal.adobe.com |

## ファイルアクセラレーターを使用した場合のダウンロードパフォーマンス例 {#expected-download-performance-using-file-accelerator}

Aspera Connect ファイルダウンロードアクセラレーターを使用した場合の 2 GB ファイルのダウンロードパフォーマンスを次の表に示します。

*Brand Portal サーバーがオレゴン州（米国）にあることを考慮すると、ネットワーク帯域幅、サーバーのレイテンシ、クライアントの所在地などの要因によって測定結果は異なります。*

| クライアントの場所 | クライアントとサーバー間の待ち時間（ミリ秒） | Aspera Connect ファイル転送アクセラレーターを使用した場合の速度（MBps） | Aspera ファイル転送アクセラレーターを使用した場合の 2 GB のファイルのダウンロード所要時間（秒） |
|---------------------------|-----------------------------------|---------------------------------------------|-------------------------------------------------------------------------|
| 米国西部（北カリフォルニア） | 18 | 36 | 57 |
| 米国西部（オレゴン） | 42 | 36 | 57 |
| 米国東部（北バージニア） | 85 | 35 | 58 |
| APAC（東京） | 124 | 36 | 57 |
| ノイダ（インド） | 275 | 13.36 | 153 |
| シドニー | 175 | 29 | 70 |
| ロンドン | 179 | 35 | 58 |
| シンガポール | 196 | 34 | 60 |

## アセットのダウンロード {#download-assets}

Brand Portal より早くアセットをダウンロードするには：

1. Brand Portal テナントにログインします。デフォルトで「**[!UICONTROL ファイル]**」ビューが開き、公開中のアセットとフォルダーがすべて表示されます。

   次のいずれかの操作を行います。

   * ダウンロードするアセットまたはフォルダーを選択します。上部のツールバーで「**[!UICONTROL ダウンロード]**」アイコンをクリックします。

     ![select-multiple-assets](assets/select-assets-new.png)

   * アセットの特定のアセットレンディションをダウンロードするには、該当するアセットにポインターを置き、クイックアクションサムネールに表示される「**[!UICONTROL ダウンロード]**」アイコンをクリックします。

     ![select-asset](assets/select-asset.png)

1. 選択したすべてのアセットが一覧表示される&#x200B;**[!UICONTROL ダウンロード]**&#x200B;ダイアログが開きます。

   アセットをダウンロードする際に Brand Portal のフォルダー階層を保持するには、「**[!UICONTROL アセットごとに別のフォルダーを作成]**」チェックボックスをオンにします。

   ダウンロードボタンは、選択した項目の数を反映しています。ルールの適用が完了したら、「**[!UICONTROL 項目をダウンロード]**」をクリックします。ルールの適用方法について詳しくは、[アセットのダウンロード](../using/brand-portal-download-assets.md#download-assets)を参照してください。

   ![download-dialog](assets/download-dialog-box-new.png)

1. デフォルトでは「**[!UICONTROL ダウンロード設定]**」の「**[!UICONTROL 高速ダウンロード]**」設定が有効になっています。したがって、IBM® Aspera Connect を使用してアセットをダウンロードするための確認ボックスが表示されます。

   初めてアセットをダウンロードするときに、IBM® Aspera Connect がブラウザーにインストールされていない場合や既存のバージョンが古い場合は、Aspera ダウンロードアクセラレーターをインストールするように求めるプロンプトが表示されます（`https://www.ibm.com/docs/en/aspera-connect/3.9.9`）。

   ![](assets/aspera-not-launched.png)

1. **Aspera Connect クライアントをインストールします**。

   IBM® Aspera Connect クライアントセットアップをインストールするには、IBM® Aspera Connect クライアントアプリケーションの .msi ファイルからセットアップを実行し、インストールウィザードに従います。

   ![](assets/aspera-download-1.png)

1. クライアントが正常にインストールされたら、ブラウザーページを更新し、ダウンロード手順を再度開始します。

1. 「**[!UICONTROL 高速ダウンロード]**」を引き続き使用するには、「**[!UICONTROL 許可]**」をクリックします。選択したすべてのレンディションが、IBM® Aspera Connect を使用して zip フォルダーにダウンロードされます。

   ダウンロードが正常に完了すると、ユーザーのシステム上にある、アセットのダウンロード先がダイアログボックスに表示されます。

   ![](assets/aspera-download-2.png)

   IBM® Aspera Connect を使用しない場合は、「**[!UICONTROL 拒否]**」をクリックします。「**[!UICONTROL 高速ダウンロード]**」が拒否された場合や失敗した場合は、エラーメッセージが表示されます。「**[!UICONTROL 通常のダウンロード]**」ボタンをクリックして、アセットのダウンロードを続行します。

>[!NOTE]
>
>管理者が「**[!UICONTROL 高速ダウンロード]**」設定をオフにした場合、選択したレンディションは、IBM® Aspera Connect を使用せずに、zip フォルダーに直接ダウンロードされます。

<!-- 
On successful completion of the download, a dialog box shows the location where assets are downloaded onto the user's system. If there is a failure, it shows error.

   >[!NOTE]
   >
   >There is a known limitation in Aspera Connect client application that no prompt to select download location appears if **[!UICONTROL Always ask me where to save downloaded files]** is enabled under the tab **[!UICONTROL Transfers]** within **[!UICONTROL Preferences]**. Before any download begins, provide the location in the text box **[!UICONTROL Save downloaded files to]**.


1. Log in to Brand Portal using a supported browser.
1. Browse and select the folders or assets you want to download. From the toolbar at the top, click the **[!UICONTROL Download]** icon. the **[!UICONTROL Download]** dialog appears with the **[!UICONTROL Asset(s)]** and **[!UICONTROL Enable download acceleration]** check boxes selected by default. 

   ![](assets/download-assetsbp.png)

   >[!NOTE]
   >
   >The functionality to send email notification with the link to download assets is presently not supported while faster downloads are enabled.

   ![](assets/fast-download-emailchk.png)

1. Click **[!UICONTROL Download]**.

   To speed up the download experience on your Brand Portal tenant account, you need to have Aspera Connect client application installed in your browser's extension.

1. **Download Aspera Connect Client**

   If Aspera Connect client is not installed on your system or the existing Aspera Connect client is out of date, a prompt is displayed on the browser page from where you can download the system-specific Aspera Connect client by selecting **[!UICONTROL Download Latest Version]**.

   ![](assets/aspera-not-launched.png)

   To download the latest version of Aspera Connect from [https://downloads.asperasoft.com/connect2/](https://downloads.asperasoft.com/connect2/), select **[!UICONTROL Download Now]** and follow the instructions.

1. **Install Aspera Connect Client**

   To install IBM Aspera Connect client setup, run the setup from  .msi  file of IBM Aspera Connect client application and follow the installation wizard.

1. Once the client is successfully installed, refresh the browser page and initiate the download steps again.

   When using Aspera Connect for the first time, the browser prompts to open the link using **[!UICONTROL IBM Aspera Connect]**. To skip this dialog in future, enable **[!UICONTROL Remember my choice for FASP links]**.

   >[!NOTE]
   >
   >This message is different on the different browsers.

1. A dialog box confirms whether to proceed the transfer or not. Select **[!UICONTROL Allow]** to begin.
To skip this dialog in future, enable **[!UICONTROL Use my choice for all connections with this host]**.
Download begins. A dialog box shows the progress of the download. Use the dialog box to **[!UICONTROL pause]**, **[!UICONTROL resume]**, or **[!UICONTROL cancel]** the download.
Aspera Connect application provides an Activity Window on the system where user can view and manage all transfer sessions. For more information, refer [Aspera Connect Client documentation](https://downloads.asperasoft.com/en/documentation/8).

![](assets/aspera-activity-window.png)

On successful completion of the download, a dialog box shows the location where assets are downloaded onto the user's system. If there is a failure, it shows error.

   >[!NOTE]
   >
   >There is a known limitation in Aspera Connect client application that no prompt to select download location appears if **[!UICONTROL Always ask me where to save downloaded files]** is enabled under the tab **[!UICONTROL Transfers]** within **[!UICONTROL Preferences]**. Before any download begins, provide the location in the text box **[!UICONTROL Save downloaded files to]**.
-->

## Microsoft® Edge ブラウザーでのファイルアクセラレーターの使用 {#using-file-accelerator-on-microsoft-edge-browser}

Microsoft® Edge は拡張保護モード（EPM）で動作しており、同じプライベートネットワーク上にあるときや信頼済みサイトとの通信時に、Aspera Connect サーバーとの通信を防ぎます。そのため、サーバーとの接続が確立されるたびにポップアップが表示されます。

![](assets/switchapps-msedge.png)

Microsoft® Edge で高速ダウンロード機能を使用するには、信頼済みサイトのリストから Brand Portal サイトを削除します。

1. コントロールパネルを開きます（**[!UICONTROL Windows キー + X]** を押し、「**[!UICONTROL コントロールパネル]**」を選択します）。
1. **[!UICONTROL ネットワークとインターネット]**／**[!UICONTROL インターネットオプション]**&#x200B;に移動します。「**[!UICONTROL セキュリティ]**」タブをクリックします。
1. 「**[!UICONTROL 信頼済みサイトゾーン]**」、「**[!UICONTROL サイト]**」の順にクリックします。
1. リストから Brand Portal サイトを削除します。

## Aspera Connect クライアントの環境設定 {#aspera-connect-client-preferences}

IBM® Aspara Connect クライアント環境設定でアイコンを右クリックし「**[!UICONTROL 環境設定]**」を選択して指定できる、便利な環境設定がいくつかあります。

![](assets/download_assets_frombrandportalimg19.png)

デフォルトのダウンロード場所を設定できます。

![](assets/aspera-preferences.png)

また、接続クライアントを実行してすばやくダウンロードを始められるよう、システム起動時に Aspera Connect クライアントを自動的に開始するようマークすることもできます。

![](assets/aspera-automaticallylaunch.png)

## ダウンロードアクセラレーションに関する問題のトラブルシューティング {#troubleshoot-issues-with-download-acceleration}

ダウンロードアクセラレーションが機能しない場合は、次の提案事項を試してください。

1. そのポートがブロックされていないことを確認します。Google 検索を使用して、使用しているオペレーティングシステムに応じて、ポートがブロックされているかどうかを確認できるオプションを見つけます。<!-- THIS URL IS 404 AND DOES NOT REDIRECT [https://test-connect.asperasoft.com](https://test-connect.asperasoft.com/) from your computer. -->

   ポートに問題がある場合は、ネットワークチームに連絡して、ポート 33001（TCP と UDP の両方）がファイアウォールでブロックされていないことを確認します。

1. ポートに問題がない場合は、[https://www.speedtest.net/](https://www.speedtest.net/) を使用して使用可能な帯域幅を測定し、ネットワークが低速になっていないかどうかを確認します。

   帯域幅が少ない（1～10 Mbps）または Kbps 単位の場合、Aspera の環境設定を使用して、利用可能な帯域幅と同じ帯域幅に制限してみてください。

   <!-- The URL in this step is giving a 404 error. 1. To confirm whether the downloads from Aspera demo server are working, use [https://demo.asperasoft.com/aspera/user](https://demo.asperasoft.com/aspera/user).  
   (login:  asperaweb , password:  demoaspera ) -->

1. 上記のトラブルシューティング手順がいずれも機能しない場合は、「ダウンロードアクセラレーションを有効化」オプションの選択を解除して、通常のダウンロードを使用します。
