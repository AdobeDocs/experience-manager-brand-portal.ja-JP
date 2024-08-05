---
title: 壁紙、ヘッダーおよびメールメッセージのカスタマイズ
description: Brand Portal管理者は、ユーザーに表示されるインターフェイスを制限付きでカスタマイズできます。 Brand Portalのログインページ用に特定の背景画像（壁紙）を選択できます。 顧客のブランドに合わせてヘッダー画像を追加したり、アセット共有のメールをカスタマイズしたりできます。
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: administration
role: Admin
exl-id: 9f5c2a6a-8844-4ca4-b0d9-8f50b6164219
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 70%

---

# 壁紙、ヘッダーおよびメールメッセージのカスタマイズ {#customize-wallpaper-header-and-email-message}

Brand Portal管理者は、ユーザーに表示されるインターフェイスを制限付きでカスタマイズできます。 Brand Portalのログインページ用に特定の背景画像（壁紙）を選択できます。 顧客のブランドに合わせてヘッダー画像を追加したり、アセット共有のメールをカスタマイズしたりできます。

## ログイン画面の壁紙のカスタマイズ {#customize-the-login-screen-wallpaper}

カスタムの壁紙画像がない場合、ログインページにはデフォルトの壁紙が表示されます。

1. 上部のツールバーで Experience Manager ロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

1. 管理ツールパネルの「**[!UICONTROL ブランディング]**」をクリックします。

   ![](assets/admin-tools-panel-10.png)

1. **[!UICONTROL ブランディングの設定]**&#x200B;ページの左パネルでは、「**[!UICONTROL 壁紙]**」がデフォルトで選択されています。ログインページに表示されるデフォルトの背景画像が表示されています。

   ![](assets/default_wallpaper.png)

1. 新しい背景画像を追加するには、上部のツールバーの「**[!UICONTROL 画像を選択]**」をクリックします。

   ![](assets/choose_wallpaperimage.png)

   次のいずれかの操作を行います。

   * お使いのコンピューターから画像をアップロードするには、「**[!UICONTROL アップロード]**」をクリックします。必要な画像に移動してアップロードします。
   * Brand Portal の既存の画像を使用するには、「**[!UICONTROL 既存から選択]**」をクリックします。アセットピッカーを使用して画像を選択します。

   ![](assets/asset-picker.png)

1. 背景画像のヘッダーテキストと説明を指定します。変更内容を保存するには、上部のツールバーの「**[!UICONTROL 保存]**」をクリックします。

1. 上部のツールバーの「**[!UICONTROL プレビュー]**」アイコンをクリックして、画像を含む Brand Portal インターフェイスのプレビューを生成します。

   ![](assets/chlimage_1.png)

   ![](assets/custom-wallpaper-preview.png)

1. デフォルトの壁紙をアクティベートまたはアクティベート解除するには、**[!UICONTROL ブランディングを設定／壁紙]**&#x200B;ページで、以下の操作を実行します。

   * Brand Portal ログインページにデフォルトの壁紙画像を表示するには、上部のツールバーの「**[!UICONTROL 壁紙のアクティベートを解除]**」をクリックします。カスタム画像のアクティベート解除を確認するメッセージが表示されます。

   ![](assets/chlimage_1-1.png)

   * Brand Portal ログインページにカスタム画像を再度表示するには、ツールバーの「**[!UICONTROL 壁紙をアクティベート]**」をクリックします。カスタム画像の再度表示を確認するメッセージが表示されます。

   ![](assets/chlimage_1-2.png)

   * 「**[!UICONTROL 保存]**」をクリックして、変更を保存します。

## ヘッダーのカスタマイズ {#customize-the-header}

Brand Portal にログインすると、ヘッダーが様々な Brand Portal ページに表示されます。

1. 上部のツールバーで Experience Manager ロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

1. 管理ツールパネルの「**[!UICONTROL ブランディング]**」をクリックします。

   ![](assets/admin-tools-panel-11.png)

1. Brand Portal インターフェイスのページヘッダーをカスタマイズするには、**[!UICONTROL ブランディングを設定]**&#x200B;ページの左パネルから「**[!UICONTROL ヘッダーの画像]**」を選択します。デフォルトのヘッダー画像が表示されています。

   ![](assets/default-header.png)

1. ヘッダー画像をアップロードするには、「**[!UICONTROL 画像を選択]**」アイコンをクリックし、「**[!UICONTROL アップロード]**」を選択します。

   既存のBrand Portal画像を使用するには、「**[!UICONTROL 既存を選択]**」を選択します。

   ![](assets/choose_wallpaperimage-1.png)

   アセットピッカーを使用して画像を選択します。

   ![](assets/asset-picker-header.png)

1. ヘッダー画像に URL を含めるには、「**[!UICONTROL 画像 URL]**」ボックスで URL を指定します。 外部または内部 URL を指定できます。内部リンクの場合は、
   [!UICONTROL `/mediaportal.html/content/dam/mac/tenant_id/tags`] などの相対リンクにすることも可能です。
このリンクをクリックすると、tags フォルダーに移動します。
変更内容を保存するには、上部のツールバーの「**[!UICONTROL 保存]**」をクリックします。

   ![](assets/configure_brandingheaderimageurl.png)

1. 上部のツールバーで「**[!UICONTROL プレビュー]**」アイコンをクリックして、ヘッダー画像を含むBrand Portal インターフェイスのプレビューを生成します。

   ![](assets/chlimage_1-3.png)
   ![](assets/custom_header_preview.png)

1. ヘッダー画像をアクティベートまたはアクティベート解除するには、**[!UICONTROL ブランディングを設定／ヘッダーの画像]**&#x200B;ページで、以下の操作を実行します。

   * ヘッダー画像がBrand Portalページに表示されないようにするには、上部のツールバーの **[!UICONTROL ヘッダーをアクティベートを解除]** をクリックします。 ヘッダー画像のアクティベート解除を確認するメッセージが表示されます。

   ![](assets/chlimage_1-4.png)

   * ヘッダー画像をBrand Portal ページに再び表示するには、上部のツールバーの **[!UICONTROL ヘッダーをアクティベート]** をクリックします。 ヘッダー画像のアクティベートを確認するメッセージが表示されます。

   ![](assets/chlimage_1-5.png)

   * 「**[!UICONTROL 保存]**」をクリックして、変更を保存します。

## メールメッセージのカスタマイズ {#customize-the-email-messaging}

アセットをリンクとして共有すると、そのリンクを含むメールがユーザーに届きます。 管理者は、これらのメールのメッセージ、つまりロゴ、説明およびフッターをカスタマイズできます。

1. 上部のツールバーで Experience Manager ロゴをクリックして、管理ツールにアクセスします。

   ![](assets/aemlogo.png)

1. 管理ツールパネルの「**[!UICONTROL ブランディング]**」をクリックします。

   ![](assets/admin-tools-panel-12.png)

1. アセットをリンクとして共有したりメールを介してダウンロードしたりする場合や **[!UICONTROL コレクション]** を共有する場合は、ユーザーにメール通知が送信されます。 メールメッセージをカスタマイズするには、**[!UICONTROL ブランディングを設定]**&#x200B;ページの左パネルから「**[!UICONTROL メールメッセージ]**」を選択します。

   ![](assets/configure-branding-page-email.png)

1. 送信するメールにロゴを追加するには、上部のツールバーの「**[!UICONTROL アップロード]**」をクリックします。

1. 「**[!UICONTROL 説明]**」セクションで、メールのヘッダーとフッターのテキストを指定します。変更内容を保存するには、上部のツールバーの「**[!UICONTROL 保存]**」をクリックします。

   >[!NOTE]
   >
   >ロゴを推奨サイズで使用していない場合や、ヘッダーやフッターのテキストが推奨単語数を超えている場合は、メールメッセージのコンテンツが判読できなくなる場合があります。
