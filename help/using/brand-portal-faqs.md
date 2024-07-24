---
title: よくある質問
description: Adobe Experience Manager Assets Brand Portal でのよくある質問について説明します。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 60104481e8f0b883fbf2cf25c1562e8376882e54
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 24%

---

# よくある質問 {#frequently-asked-questions}

Brand Portalの FAQ では、最新のExperience Manager Assets Brand Portal 6.4.6 リリース以前のバージョンで作業中に発生する可能性のあるエンドユーザーからの問い合わせや問題に重点を置いています。


## Brand Portal 6.4.6 に関する FAQ  {#faqs-bp646}

**質問：既存のレガシー OAuth エンドポイント（`https://legacy-oauth.cloud.adobe.io/login`）が機能していません。 考えられる理由は何でしょうか？**

**回答：** 従来の OAuth 設定は非推奨（廃止予定）になりました。 Experience Manager Assets オーサーインスタンスを最新のサービスパックにアップグレードし、Adobe Developer Consoleを使用して設定します。 詳しくは、[Experience Manager Assets と Brand Portal の連携の設定](configure-aem-assets-with-brand-portal.md)を参照してください。ただし、アップグレードするまでレガシー OAuth 設定が機能するようにするには、レガシー OAuth エンドポイントを `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/` に更新します。

**質問：Adobe Developer Consoleにアップグレードすると、投稿フォルダーのアセットをBrand PortalからExperience Manager Assetsに公開できなくなります。 オーサーインスタンスは Experience Manager Assets 6.5.4 にあります。考えられる理由は何でしょうか？**

**回答：** はい。投稿フォルダーのアセットをAdobe Developer ConsoleでExperience Manager Assets 6.5.4 に公開する際に発生する既知の問題があります。

この問題は Experience Manager Assets 6.5.5 で修正されました。お使いの Experience Manager Assets インスタンスを最新のサービスパック AEM 6.5.5 にアップグレードし、Adobe 開発者コンソールで[設定をアップグレード](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65)してください。


**質問：Experience Manager AssetsでBrand Portalから公開された投稿フォルダーのコンテンツが表示されません。 考えられる理由は何でしょうか？**

**回答：** Experience Manager Assets管理者に設定を問い合わせて、Brand Portal テナントが 1 つのExperience Manager Assets オーサーインスタンスのみで設定されていることを確認してください。

この問題は、複数の Experience Manager Assets オーサーインスタンスに Brand Portal テナントを設定した場合に発生する可能性があります。例えば、管理者が、ステージング環境と実稼動環境のExperience Manager Assets オーサーインスタンスに同じBrand Portal テナントを設定するとします。 この場合、Brand Portalのアセット公開トリガーは、レプリケーションエージェントが要求トークンを受け取らないので、Experience Manager Assets オーサーインスタンスがアセットの読み込みに失敗します。


**質問：Experience Manager AssetsからBrand Portalにアセットを公開できません。 レプリケーションログには、接続がタイムアウトしたことが記録されています。クイックフィックスはありますか？**

**回答：** 通常、レプリケーションキューに複数の保留中の要求がある場合、公開はタイムアウトエラーで失敗します。 この問題を解決するには、タイムアウトを回避するようにレプリケーションエージェントを設定します。

レプリケーションエージェントを設定するには、次の手順を実行します。

1. Experience Manager Assets オーサーインスタンスにログインします。
1. **ツール**&#x200B;パネルで、**[!UICONTROL デプロイメント]**／**[!UICONTROL レプリケーション]**&#x200B;に移動します。
1. 「レプリケーション」ページで、「**[!UICONTROL `Agents on author`]**」をクリックします。 Brand Portal テナントの 4 つのレプリケーションエージェントを表示できます。
1. レプリケーションエージェントの URL をクリックして、エージェントの詳細を開きます。
1. **[!UICONTROL 編集]** をクリックして、レプリケーションエージェントの設定を編集します。
1. エージェント設定で、「**[!UICONTROL 拡張]**」タブをクリックします。
1. 「**[!UICONTROL 接続を閉じる]**」チェックボックスをオンにします。
1. 手順 4～7 を繰り返して、4 つのレプリケーションエージェントをすべて設定します。
1. サーバーを再起動し、接続を確認します。


## Brand Portal 6.4.5 に関する FAQ  {#faqs-bp645}

**質問：Brand Portal 6.4.5 リリースの主な変更点は何ですか？**

**回答：** Experience Manager Assets Brand Portal 6.4.5 では、管理者権限を必要とせずに、コンテンツをアップロードし、投稿フォルダーをBrand Portalから直接Experience Manager Assetsに公開することができます。 詳しくは、[Brand Portal でのアセットソーシング](brand-portal-asset-sourcing.md)を参照してください。



**質問：作成した既存のアセット、機能、設定へのアクセス権を失いましたか？**

**回答：** 既存の機能と設定はすべてそのまま残ります。 エンドユーザーに影響はなく、コンテンツはそのまま残ります。



**質問：Brand Portalの新しいバージョンに移行するのはいつですか？**

**回答：** Brand Portal 6.4.5 は、2019 年 10 月に実稼動環境にリリースされました。 また、次回のBrand Portal版は 2020 年 3 月（PT）の予定です。
Adobe アップデートとバージョン変更については、[ リリースノート ](brand-portal-release-notes.md) と [Brand Portalの新機能 ](whats-new.md) をトラッキングすることをお勧めします。



**質問：ユーザーは影響を受けますか？**

**回答：** Brand Portal 6.4.5 リリースはBrand Portal内でのみ使用されるので、エンドユーザーに影響はありません。



**質問：Brand Portal ユーザーとして必要なアクションはありますか？**

**回答：** Brand Portal 6.4.5 リリースには、アセットソーシングという名前の新機能が付属しています。 管理者は、Experience Manager Assetsでアセットソーシング機能を設定し、Brand Portal ユーザーに対して有効にする必要があります。 詳しくは、「[アセットソーシングの有効化](brand-portal-asset-sourcing.md)」を参照してください。



**質問：投稿フォルダーを作成できるのは誰ですか？**

**回答：** Experience Manager Assetsでフォルダーを作成する権限を持つExperience Manager Assets ユーザーであれば、誰でも **投稿** フォルダーを作成できます。 **投稿** フォルダーを作成するには、**アセット投稿** タイプのフォルダーを作成します。
このフォルダーは、投稿用として、アクティブな Brand Portal ユーザーと共有されます。



**質問：投稿フォルダーには何が含まれていますか？**

**回答：** **投稿** フォルダーには、2 つのサブフォルダー **NEW** と **SHARED** が含まれています。 始めは、NEW フォルダーは空で、SHARED フォルダーには Brand Portal ユーザーの参照コンテンツ（再利用可能なアセット）が含まれます。
Brand Portal ユーザーは**投稿**&#x200B;フォルダーにアクセスし、**NEW** フォルダーにコンテンツをアップロードします。



**質問：既存の投稿フォルダーの名前を変更できますか？**

**回答：****いいえ**、既存の **投稿** フォルダーの名前を変更することはできません。



**質問：貢献度に関するアセットの要件は何ですか？**

**回答：** **投稿** フォルダーの **概要** ドキュメントと **SHARED** フォルダーの参照コンテンツは、Brand Portal ユーザーが投稿のニーズと期待を理解するのに役立ちます。 これらを合わせて、アセット要件と呼びます。

**質問：許可された任意のフォルダーにアセットをアップロードできますか？**

**回答：** 許可されていないフォルダーがあります。 Brand Portal ユーザーは、Experience Manager AssetsまたはBrand Portal管理者が共有する **投稿** フォルダーにのみコンテンツをアップロードできます。



**質問：投稿フォルダーにアクセスするにはどうすればよいですか？**

**回答：** **投稿** フォルダーにアクセスできるのは、共有されている場合のみです。 投稿フォルダーが共有されるたびに、メール/パルス通知が届きます。 メールで共有されたリンクから投稿フォルダーにアクセスできます。 または、Brand Portal インスタンスにログインし、ベルのアイコンに移動して通知を受け取り、投稿フォルダーにアクセスすることもできます。

>[!NOTE]
>
>Brand Portal ユーザーでない場合は、Experience Manager Assets管理者に依頼して、Admin Consoleにユーザーを作成してください。 次に、Brand Portal ユーザーリストのユーザー設定ファイルにプロファイルを追加します。


**質問：ユーザー読み込みの CSV ファイルの形式は何ですか？**

**回答：** この形式は、ユーザーの一括読み込みでサポートされるAdmin Consoleと一致します。 メールと氏名は必須です。



**質問：アセット投稿ユーザーのドロップダウンにユーザーのリスト（Brand Portal投稿者）が表示されるのは何ですか？**

**回答：** ドロップダウンのユーザーは、Experience Manager AssetsにアップロードされたBrand Portal ユーザー設定（.csv）ファイルから入力されます。



**質問：インポートジョブと公開ジョブのステータスはどこで確認できますか？**

**回答：** Experience Manager Assetsでは、読み込みのステータスを **async** ジョブページで確認できます。 Brand Portal では、**[!UICONTROL ツール／アセット投稿のステータス]**&#x200B;で公開ジョブのステータスを確認できます。



**質問：Experience Managerで定期的に実行されるインポートジョブの頻度はどれくらいですか？**

**回答：** Experience Manager Assetsでは、ポーリングは 5 分ごとに実行されます。



**質問：Brand PortalからExperience Manager Assetsにフォルダーを公開できる回数にしきい値はありますか？**

**回答：** いいえ。**NEW** フォルダー内のすべてのアセットは、以前に公開されたかどうかとは関係なく、Experience Manager Assetsに公開されます。 **投稿** フォルダーがBrand PortalからExperience Manager Assetsに公開されるたびに、その **NEW** フォルダーのコンテンツが置き換えられます。



**質問：投稿フォルダーに新しいアセットをアップロードするにはどうすればよいですか？**

**回答：** 投稿フォルダーへのアセットのアップロード [ に関する詳細なドキュメントを参照してください ](brand-portal-publish-contribution-folder-to-brand-portal.md)。



**質問：NEW フォルダーにアップロードされたアセットのサムネールやプレビューが表示されません。**

**回答：** Brand Portal側でワークフローが実行されないので、設計どおりです。



**質問：不安定なExperience Manager AssetsからBrand Portalにフォルダーが公開されるとどうなりますか？**

**回答：** Experience Manager Assetsでは、フォルダーがBrand Portalに公開されるたびにログが保持されます。 公開時に、Brand Portalに公開されていないすべてのアセットがレプリケーションキューに追加されます。 公開ジョブがトリガーされた後にフォルダーに追加されたアセットは、Brand Portal に公開されません。Experience Manager Assets ユーザーがフォルダーを再度公開すると、以前に公開されなかった（レプリケーションキューに存在する）アセットのみがBrand Portalに公開されます。 このプロセスは、Experience Manager AssetsからBrand Portalに公開されたフォルダー、および投稿フォルダー内の SHARED フォルダーに対しても当てはまります。

**質問：質問に連絡するのは誰ですか？**

**回答：** Adobe担当営業またはカスタマーサポートにお問い合わせください。

>[!NOTE]
>
>リリーススケジュールは暫定的で、変更される可能性があります。 更新されたリリーススケジュールを取得するには、Adobe担当営業またはカスタマーサポートにお問い合わせください。


## 製品のアクセスとサポート（制限付きサイト） {#product-access-and-support-restricted-sites}

以下のサイトは既存ユーザーのみが参照できます。アクセス権を必要とするお客様は、Adobe担当営業または販売店にお問い合わせください。

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
