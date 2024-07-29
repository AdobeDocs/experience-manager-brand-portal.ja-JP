---
title: Brand Portal でのユーザーアクセスの管理
description: Brand Portalでゲストによるアクセスと新しいユーザーによるアクセスを設定します。
contentOwner: mgulati
topic-tags: administration
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 27a9cd26-9bb3-473b-b1ac-37f77975c912
source-git-commit: 1a3e51922fb658d9d05113b4b1f4d05a0b6555c0
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 31%

---

# Brand Portal でのユーザーアクセスの管理 {#administer-user-access-on-brand-portal}

Adobe Experience Manager Assets Brand Portal 6.4.2 以降では、管理者は、ゲストによるアクセスを設定し、ユーザーが自分の組織のBrand Portalでアクセスをリクエストできるようにすることが許可されています。 これらの設定は、管理パネルで&#x200B;**[!UICONTROL アクセス設定]**&#x200B;として提供されています。これらの設定は両方とも、デフォルトでは無効になっています。

![](assets/access-configs.png)

**A** - Brand Portalのようこそ画面の **[!UICONTROL `Guest Access?`]** リンクを使用して、ゲストがBrand Portalにアクセスできるようにする設定。 （デフォルトでは無効になっています）

**B** - Brand Portalのようこそ画面の **[!UICONTROL `Need access?`]** リンクを使用してBrand Portalへのアクセスをリクエストするユーザーを許可する設定。 （デフォルトでは無効になっています）

## ゲストによるアクセスを許可 {#allow-guest-access}

ゲストによるアクセスを許可すると、ユーザーはBrand Portalにログインしなくても公開アセットにアクセスできます。
ゲストによるアクセスを許可するには、管理者が次の手順を実行する必要があります。

1. AEM ロゴを選択して、上部のツールバーにある管理ツールにアクセスします。
1. 管理ツールパネルで **[!UICONTROL Access]** を選択して **[!UICONTROL Access 設定]** ページを開きます。
1. 「**[!UICONTROL ゲストによるアクセスを許可]**」設定を有効にします。
1. 変更内容を&#x200B;**[!UICONTROL 保存]**&#x200B;します。
1. ログアウトして、変更を有効にします。

![](assets/bp-welcome-screen.png)

## ユーザーのアクセス要求を許可 {#allow-users-to-request-access}

管理者は、組織ユーザーに対し、ようこそ画面から Brand Portal へのアクセスを要求することを許可できます。ただし、管理者は、「アクセスを要求」リンクがスタートアップスクリーンに表示されるように、「**[!UICONTROL ユーザーがアクセスを要求することを許可]** 設定を有効にする必要があります。

組織ユーザーがBrand Portalへのアクセスをリクエストできるようにするには、管理者は次の操作を行う必要があります。

1. AEM ロゴを選択して、上部のツールバーにある管理ツールにアクセスします。
1. 管理ツールパネルで **[!UICONTROL Access]** を選択して **[!UICONTROL Access 設定]** ページを開きます。
1. 「**[!UICONTROL ユーザーのアクセス要求を許可]**」設定を有効にします。
1. 変更内容を&#x200B;**[!UICONTROL 保存]**&#x200B;します。
1. ログアウトして、変更を有効にします。
