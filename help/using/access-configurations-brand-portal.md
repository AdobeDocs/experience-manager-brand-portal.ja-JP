---
title: Brand Portal でのユーザーアクセスの管理
description: Brand Portalでのゲストアクセスと新規ユーザーのアクセスを設定します。
contentOwner: mgulati
topic-tags: administration
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 27a9cd26-9bb3-473b-b1ac-37f77975c912
TQID: https://experienceleague.adobe.com/SGJ5f5BOFd4Yiu2OiR9wyRU3wk-YlnGrX5Zm5JmPHuY
product_v2:
  - id: d09181b5-a36a-43de-ba01-36641440bc43
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: cda65036-5305-4f01-89da-9b3506ae8c50
  - id: da0dfbce-df02-4f8b-b32d-a4e3b1d05085
subfeature_v2:
  - id: e00c7c12-7035-41fe-ad76-1ec82c8c3f01
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e48edcb1ed5d76686794f7a7ed6389c7f4ab1ed3
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 32%

---

# Brand Portal でのユーザーアクセスの管理 {#administer-user-access-on-brand-portal}

Adobe Experience Manager Assets Brand Portal 6.4.2以降では、管理者がゲストアクセスを設定し、ユーザーが組織のBrand Portalでアクセスをリクエストできるようにします。 これらの設定は、管理パネルで&#x200B;**[!UICONTROL アクセス設定]**&#x200B;として提供されています。 これらの設定は両方とも、デフォルトでは無効になっています。

![](assets/access-configs.png)

**A** - Brand Portalようこそ画面の&#x200B;**[!UICONTROL `Guest Access?`]** リンクを使用して、Brand Portalでゲストがアクセスできるようにするための設定。 （デフォルトでは無効になっています）

**B** - Brand Portalようこそ画面の&#x200B;**[!UICONTROL `Need access?`]** リンクを使用して、ユーザーがBrand Portalへのアクセスをリクエストできるようにするための設定。 （デフォルトでは無効になっています）

## ゲストによるアクセスを許可 {#allow-guest-access}

ゲストアクセスを許可することで、Brand Portalにログインしなくてもパブリックアセットにアクセスできます。
ゲストによるアクセスを許可するには、管理者が次の手順を実行する必要があります。

1. AEM ロゴを選択して、上部のツールバーから管理ツールにアクセスします。
1. 管理ツールパネルで「**[!UICONTROL アクセス]**」を選択して、**[!UICONTROL アクセス設定]** ページを開きます。
1. 「**[!UICONTROL ゲストによるアクセスを許可]**」設定を有効にします。
1. 変更内容を&#x200B;**[!UICONTROL 保存]**&#x200B;します。
1. ログアウトして、変更を有効にします。

![](assets/bp-welcome-screen.png)

## ユーザーのアクセス要求を許可 {#allow-users-to-request-access}

管理者は、組織ユーザーに対し、ようこそ画面から Brand Portal へのアクセスを要求することを許可できます。 ただし、管理者は、ようこそ画面にリクエストアクセスリンクが表示されるように、**[!UICONTROL ユーザーにアクセスをリクエスト]**&#x200B;する設定を有効にする必要があります。

組織ユーザーがBrand Portalへのアクセスをリクエストできるようにするには、管理者は次の操作を行う必要があります。

1. AEM ロゴを選択して、上部のツールバーから管理ツールにアクセスします。
1. 管理ツールパネルで「**[!UICONTROL アクセス]**」を選択して、**[!UICONTROL アクセス設定]** ページを開きます。
1. 「**[!UICONTROL ユーザーのアクセス要求を許可]**」設定を有効にします。
1. 変更内容を&#x200B;**[!UICONTROL 保存]**&#x200B;します。
1. ログアウトして、変更を有効にします。
