---
title: Brand Portal でのダイナミックビデオのサポート
description: Brand Portal でのダイナミックビデオのサポート
contentOwner: mgulati
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: download-install
exl-id: 08d6a0fb-061e-4bef-b8e2-bb8522e7482e
source-git-commit: ff51a49a958d43c98443d816a92276faae5e9569
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 97%

---

# Brand Portal でのダイナミックビデオのサポート {#dynamic-video-support-on-brand-portal}

Dynamic Media をサポートしている Brand Portal でビデオをアダプティブにプレビューおよび再生します。また、ポータルおよび共有リンクから動的レンディションをダウンロードします。
Brand Portal を使用すると、次のことが可能になります。

* アセットの詳細ページ、カード表示、リンク共有のプレビューページでビデオをプレビューします。
* アセットの詳細ページでビデオエンコードを再生します。
* アセットの詳細ページの「レンディション」タブで動的レンディションを表示します。
* ビデオを格納したフォルダーとビデオエンコードをダウンロードします。

>[!NOTE]
>
>ビデオを操作したり Brand Portal に公開したりするには、Experience Manager オーサーインスタンスが Dynamic Media ハイブリッドモードか Dynamic Media **[!DNL Scene7]** モードのいずれかに設定されていることを確認してください。

ビデオをプレビュー、再生、ダウンロードするために、Brand Portal では次の 2 つの設定を管理者に公開しています。

* [Dynamic Media ハイブリッド設定](#configure-dm-hybrid-settings)
Experience Manager オーサーインスタンスが Dynamic Media ハイブリッドモードで動作している場合。
* [Dynamic Media [!DNL Scene7] 設定](#configure-dm-scene7-settings)
Experience Manager オーサーインスタンスが Dynamic Media **[!DNL Scene7]** モードで動作している場合。
Brand Portal テナントの複製先となる Experience Manager オーサーインスタンスに指定した設定に基づいて、これらの設定のいずれかを指定します。

>[!NOTE]
>
>**[!UICONTROL Scene7Connect]** 実行モードで動作している Experience Manager オーサーで設定された Brand Portal テナントでは、ダイナミックビデオはサポートされていません。

## ダイナミックビデオの再生方法 {#how-are-dynamic-videos-played}

![ビデオエンコードはクラウドから取得される](assets/VideoEncodes.png)

Dynamic Media 設定（[ハイブリッド](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings)設定または [[!DNL Scene7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings) 設定）が Brand Portal で指定されている場合、動的レンディションは **[!DNL Scene7]** サーバーから取得されます。したがって、ビデオエンコードは遅延や品質の劣化なしにプレビューおよび再生されます。

ビデオエンコードは Brand Portal リポジトリーに格納されず **[!DNL Scene7]** サーバーから取得されるので、Adobe Experience Manager オーサーインスタンスと Brand Portal の Dynamic Media 設定が同じであることを確認してください。

>[!NOTE]
>
>Brand Portal では、ビデオビューアとビューアプリセットはサポートされません。ビデオは Brand Portal のデフォルトのビューアでプレビューおよび再生されます。

## 前提条件 {#prerequisites}

Brand Portal 上でダイナミックビデオを操作するには、必ず以下を行ってください。

* **Dynamic Media モードで Experience Manager オーサーを起動する**
(Brand Portal の設定に使用した) Experience Manager オーサーインスタンスを [Dynamic Media - [!DNL Scene7] モード](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dms7.html?lang=ja#enabling-dynamic-media-in-scene-mode)または [Dynamic Media - ハイブリッドモード](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dynamic.html?lang=ja)のいずれかで起動します。または、
* **Experience Manager オーサーの Dynamic Media Cloud Services を設定する**
Experience Manager オーサーを実行している Dynamic Media のモード（Scene7 モードまたはハイブリッドモード）に応じて、Experience Manager オーサーの**ツール** | **クラウドサービス** | **Dynamic Media**&#x200B;で [Dynamic Media クラウドサービス（[!DNL Scene7] モード）](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dms7.html?lang=ja#configuring-dynamic-media-cloud-services) または [Dynamic Media クラウドサービス（ハイブリッドモード）](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dynamic.html?lang=ja#configuring-dynamic-media-cloud-services)のいずれかを設定します。
* **Brand Portal の Dynamic Media を設定する**
Experience Manager オーサーの Dynamic Media クラウド設定に応じて、Brand Portal 管理ツールの [Dynamic Media 設定](#configure-dm-hybrid-settings)または [[!DNL Scene7] 設定](#configure-dm-scene7-settings)を行います。
Dynamic Media - **[!UICONTROL Scene7]** モードで設定した Experience Manager オーサーインスタンスと、Dynamic Media - ハイブリッドモードで設定した Experience Manager オーサーインスタンスでは、[別々の Brand Portal テナント](#separate-tenants)を使用してください。特に Dynamic Media **[!UICONTROL S7]** と Dynamic Media ハイブリッドの機能を使用する場合、注意が必要です。
* **Brand Portal に適用したビデオエンコードを含んだフォルダーを公開する**
[ビデオエンコーディング](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/video-profiles.html?lang=ja)を適用し、リッチメディアアセットを含んだフォルダーを Experience Manager オーサーインスタンスから Brand Portal に公開します。
* **セキュアプレビューが有効な場合は、SPS でエグレス IP を許可リストに登録する**
（会社に対して[セキュアプレビューが有効 ](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html?lang=ja)な状態で）Dynamic Media -**[!DNL Scene7]** を使用する場合は、 の **[!DNL Scene7]** 会社管理者が SPS（**[!UICONTROL Scene7]** Publishing System）Flash UI を使用して、それぞれの地域の[公開エグレス IP を許可リストに登録する](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html?lang=ja#testing-the-secure-testing-service)ことをお勧めします。
エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| 該当なし | 130.248.160.68,  20.94.203.130 |
| EMEA | 185.34.189.3,  51.132.146.75 |
| APAC | 63.140.44.54 |

これらのいずれかのエグレス IP を許可リストに登録するには、[セキュアテストサービス用アカウントの準備方法](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html?lang=ja#testing-the-secure-testing-service)を参照してください。

## ベストプラクティス

ダイナミックビデオアセットが Brand Portal（および共有リンク）から正常にプレビュー、再生、ダウンロードされるようにするには、次のベストプラクティスに従います。

### Dynamic Media - Scene7 と Dynamic Media - ハイブリッドモードで別々のテナント {#separate-tenants}

Dynamic Media - **[!DNL Scene7]** モードと Dynamic Media - ハイブリッドモードの両方の機能を使用している場合、Dynamic Media - **[!DNL Scene7]** と Dynamic Media - ハイブリッドモードで設定された Experience Manager オーサーインスタンスには、異なる Brand Portal テナントを使用します。


![オーサーと BP が 1 対 1 で対応](assets/BPDynamicMedia.png)

### Experience Manager オーサーインスタンスと Brand Portal で設定の詳細が同じ

Brand Portal と **[!UICONTROL Experience Manager クラウド設定]**&#x200B;で設定の詳細が同じであることを確認します。設定の詳細が同じものには、以下が含まれます。

* **[!UICONTROL タイトル]**
* **[!UICONTROL 登録 ID]**
* **[!UICONTROL Dynamic Media - ハイブリッドモード]**&#x200B;での&#x200B;**[!UICONTROL ビデオサービス URL]**
* **[!UICONTROL タイトル]**
* 資格情報（**[!UICONTROL メール]**&#x200B;およびパスワード）
* **[!UICONTROL 地域]**
* Dynamic Media - **[!DNL Scene7]** モードでの&#x200B;**[!UICONTROL 会社情報]**

### Dynamic Media Scene7 モードの公開エグレス IP を許可リストに登録する

Dynamic Media **[!UICONTROL Scene7]**（[セキュアプレビューが有効](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html?lang=ja)）を使用して Brand Portal にビデオアセットを配信する場合、**[!UICONTROL Scene7]** はステージング環境または内部アプリケーション用に専用の画像サーバーを設定します。このサーバーへのリクエストはすべて、発信元 IP アドレスをチェックします。受信リクエストが IP アドレスの承認済みリストに含まれていない場合は、失敗のレスポンスが返されます。
そのため、**[!UICONTROL Scene7]** の会社の管理者が、（SPS **[!UICONTROL （Scene7 Publishing System） Flash UI を使用して、自社の]** セキュアテスト ]**環境用の承認済み IP アドレスリストを設定します**[!UICONTROL 。 該当するそれぞれの地域のエグレス IP（以下を参照）を、その承認済みリストに必ず追加してください。
これらのいずれかのエグレス IP を許可リストに登録するには、[セキュアテストサービス用アカウントの準備方法](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public.html?lang=ja#testing-the-secure-testing-service)を参照してください。
エグレス IP は次のとおりです。

| **地域** | **エグレス IP** |
|--- |--- |
| 該当なし | 130.248.160.68, 20.94.203.130 |
| EMEA | 51.132.146.75、130.248.244.202、130.248.244.203、130.248.244.204、130.248.244.210、130.248.244.211,、130.248.244.212 |
| APAC | 63.140.44.54 |

## Dynamic Media ハイブリッドの設定 {#configure-dm-hybrid-settings}

Experience Manager オーサーインスタンスが Dynamic Media ハイブリッドモードで動作している場合は、管理ツールパネルの&#x200B;**[!UICONTROL ビデオ]**&#x200B;タイルを使用して、Dynamic Media ゲートウェイを設定します。

>[!NOTE]
>
>[ビデオエンコーディングプロファイル](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/video-profiles.html?lang=ja)は Brand Portal には公開されず、代わりに **[!UICONTROL Scene7]** サーバーから取得されます。そのため、ビデオエンコードが Brand Portal で正常に再生されるためには、設定の詳細を Experience Manager オーサーインスタンスの [Dynamic Media クラウドサービス（[!DNL Scene7] モード）](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/config-dms7.html?lang=ja#configuring-dynamic-media-cloud-services)と同じにする必要があります。

Brand Portal テナントで Dynamic Media 設定をセットアップするには：

1. Brand Portal で上部のツールバーにある Experience Manager ロゴをクリックして、管理ツールにアクセスします。
1. 管理ツールパネルで&#x200B;**[!UICONTROL ビデオ]**&#x200B;タイルを選択します。

   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/DMHybrid-Video.png)

   **[!UICONTROL Dynamic Media 設定を編集]**&#x200B;ページが開きます。

   ![Brand Portal での Dynamic Media ハイブリッドの設定](assets/edit-dynamic-media-config.png)

1. 「**[!UICONTROL 登録 ID]**」と「**[!UICONTROL ビデオサービスの URL]**」（DM ゲートウェイの URL）を指定します。これらの詳細が、Experience Manager オーサーインスタンスの&#x200B;**[!UICONTROL ツール／クラウドサービス]**&#x200B;で指定した内容と同じであることを確認してください。
1. 「**保存**」をクリックして、設定を保存します。

## Dynamic Media Scene7 の設定 {#configure-dm-scene7-settings}

Experience Manager オーサーインスタンスが Dynamic Media - **[!UICONTROL Scene7]** モードで動作している場合は、管理ツールパネルの **[!UICONTROL Dynamic Media 設定]**&#x200B;タイルを使用して、**[!UICONTROL Scene7]** サーバーを設定します。

Brand Portal テナントで Dynamic Media **[!UICONTROL Scene7]** 設定をセットアップするには：

1. Brand Portal で上部のツールバーにある Experience Manager ロゴをクリックして、管理ツールにアクセスします。

2. 管理ツールパネルで **[!UICONTROL Dynamic Media 設定]**&#x200B;タイルを選択します。

   ![Brand Portal での DM [!UICONTROL Scene7] の設定](assets/DMS7-Tile.png)

   **[!UICONTROL Dynamic Media 設定を編集]**&#x200B;ページが開きます。

   ![Brand Portal での Scene7 の設定](assets/S7Config.png)

3. 以下を指定します。

   * **[!UICONTROL タイトル]**
   * Scene7 サーバーにアクセスするための認証情報（**[!UICONTROL メール ID]** と&#x200B;**[!UICONTROL パスワード]**）
   * **[!UICONTROL 地域]**

   これらの値が、Experience Manager オーサーインスタンスにある値と同じであることを確認してください。

4. 「**[!UICONTROL Dynamic Media に接続]**」をクリックします。

5. **[!UICONTROL 会社名]**&#x200B;を指定し、設定を&#x200B;**[!UICONTROL 保存]**&#x200B;します。
