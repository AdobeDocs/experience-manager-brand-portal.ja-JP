---
title: よくある質問
description: Adobe Experience Manager Assets Brand Portal でのよくある質問について説明します。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: ht
source-wordcount: '1500'
ht-degree: 100%

---

# よくある質問 {#frequently-asked-questions}

Brand Portal に関する FAQ では、最新の Experience Manager Assets Brand Portal 6.4.6 リリース以前のバージョンでの作業中にエンドユーザーに発生する可能性がある質問や問題に焦点を当てています。


## Brand Portal 6.4.6 に関する FAQ {#faqs-bp646}

**質問：既存のレガシー OAuth エンドポイント（`https://legacy-oauth.cloud.adobe.io/login`）が機能していません。考えられる理由は何でしょうか？**

**回答：**&#x200B;レガシー OAuth 設定は非推奨（廃止予定）です。Experience Manager Assets オーサーインスタンスを最新のサービスパックにアップグレードし、Adobe Developer Console を介して設定します。詳しくは、[Experience Manager Assets と Brand Portal の連携の設定](configure-aem-assets-with-brand-portal.md)を参照してください。ただし、アップグレードするまでレガシー OAuth 設定が機能するようにするには、レガシー OAuth エンドポイントを `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/` に更新します。

**質問：Adobe Developer Console にアップグレードしたら、投稿フォルダーのアセットを Brand Portal から Experience Manager Assets に公開できません。オーサーインスタンスは Experience Manager Assets 6.5.4 にあります。考えられる理由は何でしょうか？**

**回答：**&#x200B;はい、Adobe Developer Console を介して Experience Manager Assets 6.5.4 に投稿フォルダーのアセットを公開する際に既知の問題が発生します。

この問題は Experience Manager Assets 6.5.5 で修正されました。お使いの Experience Manager Assets インスタンスを最新のサービスパック AEM 6.5.5 にアップグレードし、Adobe Developer Console で[設定をアップグレード](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65)してください。


**質問：Brand Portal から公開された投稿フォルダーのコンテンツが Experience Manager Assets に表示されません。考えられる理由は何でしょうか？**

**回答：** Experience Manager Assets 管理者に連絡して設定を確認し、Brand Portal テナントに Experience Manager Assets オーサーインスタンスが 1 つのみ設定されていることを確認してください。

この問題は、複数の Experience Manager Assets オーサーインスタンスに Brand Portal テナントを設定した場合に発生する可能性があります。例えば、管理者が、ステージング環境と実稼動環境の Experience Manager Assets オーサーインスタンスに同じ Brand Portal テナントを設定するとします。この場合、Brand Portal でアセットの公開がトリガーされますが、レプリケーションエージェントがリクエストトークンを受信しないので、Experience Manager Assets オーサーインスタンスはアセットの読み込みに失敗します。


**質問：Experience Manager Assets から Brand Portal にアセットを公開できません。レプリケーションログには、接続がタイムアウトしたことが記録されています。クイックフィックスはありますか？**

**回答：**&#x200B;通常、レプリケーションキューに保留中のリクエストが複数ある場合、公開はタイムアウトエラーで失敗します。この問題を解決するには、タイムアウトを回避するようにレプリケーションエージェントを設定します。

レプリケーションエージェントを設定するには、次の手順を実行します。

1. Experience Manager Assets オーサーインスタンスにログインします。
1. **ツール**&#x200B;パネルで、**[!UICONTROL デプロイメント]**／**[!UICONTROL レプリケーション]**&#x200B;に移動します。
1. レプリケーションページで、「**[!UICONTROL `Agents on author`]**」をクリックします。Brand Portal テナントの 4 つのレプリケーションエージェントを表示できます。
1. レプリケーションエージェントの URL をクリックして、エージェントの詳細を開きます。
1. 「**[!UICONTROL 編集]**」をクリックして、レプリケーションエージェントの設定を編集します。
1. エージェントの設定で、「**[!UICONTROL 拡張]**」タブをクリックします。
1. 「**[!UICONTROL 接続を閉じる]**」チェックボックスをオンにします。
1. 手順 4～7 を繰り返して、4 つのレプリケーションエージェントをすべて設定します。
1. サーバーを再起動し、接続を確認します。


## Brand Portal 6.4.5 に関する FAQ  {#faqs-bp645}

**質問：Brand Portal 6.4.5 リリースの主な変更点は何ですか？**

**回答：** Experience Manager Assets Brand Portal 6.4.5 では、管理者権限を必要とせずに、Brand Portal から直接、コンテンツをアップロードし、投稿フォルダーを Experience Manager Assets に公開できます。詳しくは、[Brand Portal でのアセットソーシング](brand-portal-asset-sourcing.md)を参照してください。



**質問：作成した既存のアセット、機能または設定へのアクセス権は失われましたか？**

**回答：**&#x200B;既存の機能と設定はすべてそのまま残ります。エンドユーザーに影響はなく、コンテンツはそのまま残ります。



**質問：新しいバージョンの Brand Portal にはいつ移行しますか？**

**回答：**Brand Portal 6.4.5 は、2019年10月に実稼動環境へリリースされました。また、次の Brand Portal バージョンは、2020年3月にリリースされる予定です。
アップデートとバージョンの変更について詳しくは、アドビでは、[リリースノート](brand-portal-release-notes.md)と [Brand Portal の新機能](whats-new.md)を参照することをお勧めします。



**質問：ユーザーに影響はありますか？**

**回答：** Brand Portal 6.4.5 リリースは Brand Portal 内でのみ行われるので、エンドユーザーに影響はありません。



**質問：Brand Portal ユーザーとして必要なアクションはありますか？**

**回答：** Brand Portal 6.4.5 リリースには、アセットソーシングという新機能が付属しています。管理者は、Experience Manager Assets でアセットソーシング機能を設定し、Brand Portal ユーザーに対してこの機能を有効にする必要があります。詳しくは、[アセットソーシングの有効化](brand-portal-asset-sourcing.md)を参照してください。



**質問：投稿フォルダーを作成できるのは誰ですか？**

**回答：** Experience Manager Assets でフォルダーを作成する権限を持つ Experience Manager Assets ユーザーであれば、誰でも&#x200B;**投稿**&#x200B;フォルダーを作成できます。**投稿**&#x200B;フォルダーを作成するには、**アセット投稿**タイプのフォルダーを作成します。
このフォルダーは、投稿用として、アクティブな Brand Portal ユーザーと共有されます。



**質問：投稿フォルダーには何が含まれますか？**

**回答：** **投稿**&#x200B;フォルダーには、**NEW** と **SHARED** の 2 つのサブフォルダーが含まれます。始めは、NEW フォルダーは空で、SHARED フォルダーには Brand Portal ユーザーの参照コンテンツ（再利用可能なアセット）が含まれます。
Brand Portal ユーザーは**投稿**&#x200B;フォルダーにアクセスし、**NEW** フォルダーにコンテンツをアップロードします。



**質問：既存の投稿フォルダーの名前を変更できますか？**

**回答：****いいえ**、既存の&#x200B;**投稿**&#x200B;フォルダーの名前は変更できません。



**質問：投稿に関するアセット要件とは何ですか？**

**回答**：**投稿**&#x200B;フォルダー内の&#x200B;**概要**&#x200B;ドキュメントと **SHARED** フォルダー内の参照コンテンツは、Brand Portal ユーザーが投稿のニーズと期待を理解するのに役立ちます。これらはまとめてアセット要件と呼ばれます。

**質問：許可されたフォルダーにアセットをアップロードできますか？**

**回答：**&#x200B;許可されたフォルダーすべてにアップロードできるわけではありません。Brand Portal ユーザーは、Experience Manager Assets または Brand Portal 管理者が共有する&#x200B;**投稿**&#x200B;フォルダーにのみコンテンツをアップロードできます。



**質問：投稿フォルダーにアクセスするにはどうすればよいですか？**

**回答：****投稿**&#x200B;フォルダーには、自分と共有されている場合にのみアクセスできます。投稿フォルダーが自分と共有されるたびに、メール／パルス通知が届きます。メールで共有されたリンクを介して投稿フォルダーにアクセスできます。または、Brand Portal インスタンスにログインし、通知のベルアイコンに移動して、投稿フォルダーにアクセスすることもできます。

>[!NOTE]
>
>Brand Portal ユーザーでない場合は、Experience Manager Assets 管理者に、Admin Console でユーザーを作成するようにリクエストしてください。次に、Brand Portal ユーザーリストのユーザー設定ファイルにプロファイルを追加します。


**質問：ユーザー読み込み用の CSV ファイルの形式は何ですか？**

**回答：**&#x200B;形式は、Admin Console が一括ユーザー読み込みをサポートしているものと一致します。メールと氏名は必須です。



**質問：アセット投稿ユーザードロップダウンのユーザー（Brand Portal 投稿者）のリストには何が入力されますか？**

**回答：**&#x200B;ドロップダウンのユーザーは、Experience Manager Assets にアップロードされた Brand Portal ユーザー設定（.csv）ファイルから入力されます。



**質問：読み込みジョブと公開ジョブのステータスはどこで確認できますか？**

**回答：** Experience Manager Assets では、**非同期**&#x200B;ジョブページで読み込みのステータスを確認できます。Brand Portal では、**[!UICONTROL ツール／アセット投稿のステータス]**&#x200B;で公開ジョブのステータスを確認できます。



**質問：Experience Manager で定期的に実行される読み込みジョブの頻度はどれくらいですか？**

**回答：** Experience Manager Assets では、ポーリングは 5 分ごとに実行されます。



**質問：Brand Portal から Experience Manager Assets にフォルダーを公開できる回数にしきい値はありますか？**

**回答：**&#x200B;いいえ、以前に公開されたかどうかに関係なく、**NEW** フォルダー内のすべてのアセットが Experience Manager Assets に公開されます。**投稿**&#x200B;フォルダーが Brand Portal から Experience Manager Assets に公開されるたびに、**NEW** フォルダーのコンテンツが置き換えられます。



**質問：投稿フォルダーに新しいアセットをアップロードするにはどうすればよいですか？**

**回答：**&#x200B;詳しくは、[投稿フォルダーへのアセットのアップロード](brand-portal-publish-contribution-folder-to-brand-portal.md)のドキュメントを参照してください。



**質問：NEW フォルダーにアップロードされたアセットのサムネールやプレビューが表示されません。**

**回答**：Brand Portal 側でワークフローが実行されないので、設計されたとおりに表示されません。



**質問：Experience Manager Assets から流動的な Brand Portal にフォルダーが公開されるとどうなりますか？**

**回答：** Experience Manager Assets では、フォルダーが Brand Portal に公開されるたびにログが保持されます。公開時に、Brand Portal に公開されていないすべてのアセットがレプリケーションキューに追加されます。公開ジョブがトリガーされた後にフォルダーに追加されたアセットは、Brand Portal に公開されません。Experience Manager Assets ユーザーがフォルダーを再度公開すると、以前に公開されなかったアセット（レプリケーションキューに存在するもの）のみが Brand Portal に公開されます。このプロセスは、Experience Manager Assets から Brand Portal に公開されたすべてのフォルダーおよび投稿フォルダー内の SHARED フォルダーに当てはまります。

**質問：質問がある場合は誰に問い合わせればよいですか？**

**回答：**&#x200B;アドビアカウントマネージャーまたはカスタマーサポートにお問い合わせください。

>[!NOTE]
>
>リリーススケジュールは暫定的で、変更される可能性があります。更新されたリリーススケジュールを取得するには、アドビアカウントマネージャーまたはカスタマーサポートにお問い合わせください。


## 製品のアクセスとサポート（制限付きサイト） {#product-access-and-support-restricted-sites}

これらのサイトはお客様のみが参照できます。お客様がアクセス権を必要とする場合は、アドビアカウントマネージャーにお問い合わせください。

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
