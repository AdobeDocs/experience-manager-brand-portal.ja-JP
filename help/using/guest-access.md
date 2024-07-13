---
title: Brand Portal へのゲストによるアクセス
seo-title: Guest Access to Brand Portal
description: ゲストによるアクセスを許可し、認証が不要な多数のユーザーのオンボーディングにかかる労力を省きます。
seo-description: Allow guest access and save the effort to onboard numerous users without authentication.
uuid: edb4378d-1710-44a2-97a6-594d99f62fff
contentOwner: VG
topic-tags: introduction
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: b9e9fe7b-0373-42d1-851b-7c76b47657c2
exl-id: ecce0a45-abae-41c4-9ea7-5dfdcf19e5ea
source-git-commit: 0670b8d372fd2dc5bdb1d0a928601e3e09a6dcf9
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 98%

---

# Brand Portal へのゲストによるアクセス {#guest-access-to-brand-portal}

Experience Manager Assets Brand Portal では、ゲストによるポータルへのアクセスを許可します。ゲストユーザーは資格情報がなくてもポータルに入ることができ、ポータルの公開アセット（およびコレクション）にアクセスできます。ゲストセッション中のユーザーは Lightbox（非公開コレクション）にアセットを追加でき、セッションが終了するまで、またはゲストユーザーが[[!UICONTROL セッションの終了]](#exit-guest-session)を選択した場合を除いて、同様にダウンロードすることができます。ゲストユーザーセッションは 15 分間アクティブのままになります。

ゲストによるアクセス機能を使用すれば、組織は対象オーディエンスのオンボーディングを行わなくても、[承認済みアセットをすばやく共有](../using/brand-portal-sharing-folders.md#how-to-share-folders)することができます。Brand Portal 6.4.2 以降には、複数の同時ゲストユーザー（組織あたりの合計ユーザークォータの 10%）に対応する機能が搭載されています。ゲストによるアクセスを許可することで、Brand Portal の限られた機能を使用するユーザーのスコアの管理やオンボーディングにかかる時間を節約できます。\
管理ツールパネルの「**[!UICONTROL アクセス]**」設定の「**[!UICONTROL ゲストによるアクセスを許可]**」オプションを使用して、組織の Brand Portal アカウントでのゲストによるアクセスを有効化（または無効化）できます。

<!--
Comment Type: annotation
Last Modified By: mgulati
Last Modified Date: 2018-08-17T10:42:59.879-0400
Removed the first para: "AEM Assets Brand Portal allows public users to enter the portal anonymously and have restricted access to the allowed public resources as guests. Organization users with guest role need not seek access and authentication from administrators."
-->

![](assets/enable-guest-access.png)

## ゲストセッションの開始 {#begin-guest-session}

匿名でBrand Portalに入るには、「ゲストとしてアクセスしますか？」に対応する **[!UICONTROL ここをクリック]** を選択します **[!UICONTROL 。Brand Portalのようこそ画面で]** きます。 CAPTCHA セキュリティチェックを入力して、Brand Portal へのアクセスを許可します。

![](assets/bp-login-screen.png)

## ゲストセッションの期間 {#guest-session-duration}

ゲストユーザーセッションが 15 分間アクティブのままになります。
つまり、**[!UICONTROL Lightbox]** の状態はセッションの開始時刻から 15 分間保持され、その後は現在のゲストセッションが再起動するので、Lightbox の状態が失われます。

例えば、ゲストユーザーが 15 時 00 分に Brand Portal にログインし、15 時 05 分にダウンロード対象のアセットを **[!UICONTROL Lightbox]** に追加するとします。ユーザーが 15 時 15 分より前（ログインから 15 分以内）に **[!UICONTROL Lightbox]** コレクション（またはそのアセット）をダウンロードしない場合、ユーザーはセッションを再起動する必要があります。その場合、**[!UICONTROL Lightbox]** は空になります。つまり、セッションが失われた場合、アップロードしたアセットは使用できなくなります。

## 許可されている同時ゲストセッション {#concurrent-guest-sessions-allowed}

同時ゲストセッションの数は、組織あたりの合計ユーザークォータの 10% に制限されます。つまり、ユーザークォータが 200 の組織の場合、最大 20 人のゲストユーザーが同時に作業をすることができます。21 番目のゲストユーザーはアクセスを拒否され、20 人のアクティブなゲストユーザーのいずれかがセッションを終了した場合にのみゲストとしてアクセスできるようになります。

>[!NOTE]
>
>ライセンスを取得したユーザーの数が契約値（クォータ）を超えても、Brand Portal は通知を送信しません。また、ライセンスを取得したユーザーのアクティビティは制限されません。

## ゲストユーザーの Brand Portal の操作 {#guest-user-interaction-with-brand-portal}

### ゲスト UI ナビゲーション

ゲストとして Brand Portal に入ると、すべてのユーザーまたはゲストユーザーのみと[共有されているアセットおよびフォルダー](../using/brand-portal-sharing-folders.md#sharefolders)をすべて表示できます。これはコンテンツのみの表示であり、アセットがカード、リストまたは列レイアウトで表示されます。

![](assets/disabled-folder-hierarchy1.png)

ただし、管理者が「[フォルダー階層を有効化](../using/brand-portal-general-configuration.md#main-pars-header-1621071021)」設定を有効にしていた場合は、ゲストユーザーが Brand Portal にログインしたときに、ルートフォルダーから始まるフォルダーツリーと、それぞれの親フォルダー内に含まれる共有フォルダーが表示されます。

これらの親フォルダーは仮想フォルダーであり、これらに対してアクションを実行することはできません。これらの仮想フォルダーには、鍵のアイコンが付きます。

**[!UICONTROL カード表示]**&#x200B;でこれらをカーソルで指したり選択したりしても、共有フォルダーとは異なり、アクションタスクは表示されません。**[!UICONTROL 列表示]**&#x200B;や&#x200B;**[!UICONTROL リスト表示]**&#x200B;で仮想フォルダーを選択すると「**[!UICONTROL 概要]**」ボタンが表示されます。

>[!NOTE]
>
>最初の共有フォルダーのサムネール画像が仮想フォルダーのデフォルトのサムネールになります。

![](assets/enabled-hierarchy1.png) ![](assets/hierarchy1-nonadmin.png) ![](assets/hierarchy-nonadmin.png) ![](assets/hierarchy2-nonadmin.png)

「**[!UICONTROL 表示設定]**」オプションでは、ゲストユーザーは、**[!UICONTROL カード表示]**&#x200B;のカードサイズや、**[!UICONTROL リスト表示]**&#x200B;に表示する列を調整することができます。

![](assets/nav-guest-user.png)

**[!UICONTROL コンテンツツリー]**&#x200B;では、アセット階層内を移動することができます。

![](assets/guest-login-ui.png)

Brand Portal には、選択したアセット／フォルダーの&#x200B;**[!UICONTROL アセットプロパティ]**&#x200B;をゲストユーザーが表示できる「**[!UICONTROL 概要]**」オプションがあります。「**[!UICONTROL 概要]**」オプションは、次の場所に表示されます。

* アセットやフォルダーを選択する際に上部に表示されるツールバー。
* パネルセレクターを選択する際のドロップダウン。

アセットやフォルダーを選択した状態で「**[!UICONTROL 概要]**」オプションを選択すると、タイトル、パス、アセット作成時間を確認できます。一方、アセットの詳細ページで「**[!UICONTROL 概要]**」オプションを選択すると、アセットのメタデータを確認できます。

![](assets/overview-option-1.png)

![](assets/overview-rail-selector-1.png)

左パネルの「**[!UICONTROL ナビゲーション]**」オプションでは、ファイルからコレクションに移動したり、ユーザーがファイルやコレクションのアセットから参照できるよう、ゲストセッションに戻ったりすることができます。

「**[!UICONTROL フィルター]**」オプションを使用すると、ゲストユーザーは管理者が設定した検索用述語を使用して、アセットファイルやフォルダーにフィルターを適用することができます。

### ゲストユーザーの機能

ゲストユーザーは Brand Portal の公開アセットにアクセスできますが、制約もいくつかあります（これについては後で説明します）。

**ゲストユーザーが実行できる操作**：

* すべての Brand Portal ユーザー向けのすべての公開フォルダーと公開コレクションにアクセスする。
* メンバーや詳細ページを参照し、すべての公開フォルダーおよび公開コレクションのメンバーの完全なアセット表示を行う。
* 公開フォルダーおよび公開コレクション全体でアセットを検索する。
* Lightbox コレクションにアセットを追加する。コレクションに対するこれらの変更は、セッションの間保持されます。
* アセットを直接、または Lightbox コレクションからダウンロードする。

**ゲストユーザーが実行できない操作**：

* コレクションや保存済みの検索結果を作成、またはそれらを共有する。
* フォルダーやコレクションの設定にアクセスする。
* アセットをリンクとして共有する。

### ゲストセッションでのアセットのダウンロード

ゲストユーザーは、公開アセット、またはゲストユーザーのみと共有されたアセットを Brand Portal で直接ダウンロードできます。また、ゲストユーザーは **[!UICONTROL Lightbox]**（公開コレクション）にアセットを追加したり、セッションが期限切れになる前に **[!UICONTROL Lightbox]** コレクションをダウンロードしたりできます。

アセットやコレクションをダウンロードするには、次の場所のダウンロードアイコンを使用します。

* アセットまたはコレクションにカーソルを合わせると表示されるクイックアクションサムネール
* アセットまたはコレクションを選択すると表示される上部のツールバー

![](assets/download-on-guest.png)

[!UICONTROL ダウンロード]ダイアログで「**[!UICONTROL ダウンロードアクセラレーションを有効化]**」を選択すると、[ダウンロードパフォーマンスを強化](../using/accelerated-download.md)することができます。

## ゲストセッションの終了 {#exit-guest-session}

ゲストセッションを終了するには、ヘッダーにあるオプションから「**[!UICONTROL セッションを終了]**」を使用します。ただし、ゲストセッションに使用されるブラウザータブが非アクティブになっている場合、アクティビティが行われなくなってから 2 時間が経過するとセッションは自動的に期限切れとなります。

![](assets/end-guest-session.png)

## ゲストユーザーアクティビティの監視 {#monitoring-guest-user-activities}

管理者は、Brand Portal でのゲストユーザーの操作を監視できます。Brand Portal で生成されたレポートは、ゲストユーザーアクティビティに関する重要なインサイトを提供できます。例えば、**[!UICONTROL ダウンロード]**&#x200B;レポートを使用すると、ゲストユーザーによってダウンロードされたアセットの数を追跡できます。**[!UICONTROL ユーザーログイン]**&#x200B;レポートでは、ゲストユーザーがポータルに最後にログインした時刻、および指定期間内のログイン頻度を確認ができます。
