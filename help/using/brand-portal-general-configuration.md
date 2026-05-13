---
title: 一般的なテナント設定の管理
description: ダウンロードアクセラレーション、公開スマートコレクションの作成、公開コレクションの作成を設定し、管理者ユーザーがテナントのアセットを削除できるようにします。
contentOwner: mgulati
topic-tags: administration
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 5607be8e-0a7f-4692-b71b-5f66eb9ac5ee
TQID: https://experienceleague.adobe.com/W08soCNQvrQy3ZttX4Oa2m-dvmTSxyeTpPmHNLedgPA
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
source-wordcount: 396
ht-degree: 53%

---

# 一般的なテナント設定の管理 {#administer-general-tenant-configurations}

Experience Manager Assets Brand Portal では、各組織が特定のテナントについて以下の機能を設定することができます。

* 管理者によるアセットの削除
* 管理者以外のユーザーによる公開コレクションの作成
* 管理者以外のユーザーによる公開スマートコレクションの作成
* 共有フォルダーの親階層は、管理者以外のユーザーにも表示されます

これらの設定は、管理ツールパネルの&#x200B;**[!UICONTROL 一般設定]**&#x200B;設定として提供されています。

![](assets/general-config.png)

**A** – 管理者がBrand Portalからアセットを削除できるようにする設定。 （デフォルトでは有効になっています）

**B** – 管理者以外のユーザーが公開コレクションを作成できるように設定します。 （デフォルトでは有効になっています）

**C** – 管理者以外のユーザーによる公開スマートコレクションの作成を許可する設定。 （デフォルトでは有効になっています）

**D** – 共有フォルダーのフォルダー階層（ルートから）を管理者以外のユーザー（エディター、ビューアー、ゲストユーザー）に表示するための設定。 （デフォルトでは無効になっています）

## 一般設定を有効または無効にする {#enable-disable-general-configurations}

これらの各設定を有効または無効にするには：

1. 管理者権限でログインします。
1. Experience Manager ロゴを選択して、上部のツールバーから管理ツールにアクセスします。
1. 管理ツールパネルから、**[!UICONTROL 一般]**&#x200B;を選択して&#x200B;**[!UICONTROL 一般設定]**&#x200B;ページを開きます。
1. 各トグルスイッチを使用して、一般設定のいずれかを有効または無効にします。
1. 変更内容を&#x200B;**[!UICONTROL 保存]**&#x200B;します。
1. ログアウトして、変更を有効にします。

## 管理者ユーザーが Brand Portal からアセットを削除することを許可 {#allow-admin-users-to-delete-assets-from-brand-portal}

「**[!UICONTROL ユーザーによる削除を許可]**」設定では、管理者権限を持つユーザーがアセットやフォルダーを Brand Portal から削除することを許可（または禁止）できます。

## 管理者以外による公開コレクションの作成を許可 {#allow-public-collections-creation-by-non-admins}

「[[!UICONTROL 公開コレクションの作成を許可]](../using/brand-portal-share-collection.md#main-pars-text-1915052376)」設定では、管理者以外のユーザーが Brand Portal 上に公開コレクションを作成することを許可するかどうかを制御できます。 この設定はデフォルトで有効です。 設定を無効にすることで、組織はポータルに多数の公開コレクションが存在するのを防ぎ、システムスペースを節約できます。

## 管理者以外による公開スマートコレクションの作成を許可 {#allow-public-smart-collections-creation-by-non-admins}

「[[!UICONTROL 公開スマートコレクションの作成を許可]](../using/brand-portal-searching.md#main-pars-header-500620467)」設定では、管理者以外のユーザーが検索をスマートコレクションとして保存して、そのテナントの公開スマートコレクションにすることを許可するかどうかを制御できます。 この設定はデフォルトで有効です。 この設定を無効にすることで、組織は、管理者以外のユーザーが組織のBrand Portalで作成した膨大な数の公開スマートコレクションを防ぐことができます。

<!-- 
## Allow download acceleration {#allow-download-acceleration}

[[!UICONTROL Allow download acceleration]](../using/accelerated-download.md) configuration lets the organizations to allow accelerated downloads of assets from Brand Portal and shared links, by integrating with IBM Aspera Connect that is an install-on-demand application. The application uses proprietary technology to remove TCP overheads.
-->

## フォルダー階層の有効化 {#enable-folder-hierarchy}

「[[!UICONTROL フォルダー階層を有効化]](../using/brand-portal-sharing-folders.md#non-admin-user-access-to-shared-folders)」設定では、管理者以外のユーザー（エディター、閲覧者、ゲストユーザー）がログイン後に目にする共有フォルダーの表示を管理者が制御できます。
