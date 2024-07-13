---
title: Experience Manager Assets と Brand Portal の連携の設定
seo-title: Configure Experience Manager Assets with Brand Portal
description: Experience Manager Assets と Brand Portal の連携の設定について説明します。
seo-description: Get an insight into configuring Experience Manager Assets with Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: 454b05c05359a2068cc29124f826d5bd25a1bad1
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 100%

---

# Experience Manager Assets と Brand Portal の連携の設定 {#configure-integration}

Adobe Experience Manager Assets と Brand Portal の連携を設定すると、Brand Portal ユーザー向けにアセットの公開、アセットの配布、アセットの投稿機能が可能になります。これにより、Experience Manager Assets ユーザーは、Brand Portal ユーザーにアセットを公開および配布できます。Brand Portal ユーザーは、共有アセットにアクセスしたり、アセットを投稿したりできます。アセットを投稿するには、アセット投稿フォルダーに新しいアセットをアップロードし、その投稿フォルダーを Experience Manager Assets に公開します。

Experience Manager Assets と Brand Portal の連携の設定は、次のバージョンでサポートされています。

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets（オンプレミス版および Managed Services 版）6.5 以降

Cloud Manager から Brand Portal をアクティベートすると、Experience Manager Assets as a Cloud Service と Brand Portal の連携が自動的に設定されます。アクティベーションワークフローにより、バックエンドで必要な設定が作成され、Experience Manager Assets as a Cloud Service インスタンスと同じ IMS 組織に Brand Portal がアクティベートされます。

一方、Experience Manager Assets（オンプレミス版および Managed Services 版）と Brand Portal の連携は、Adobe Developer Console を使用して手動で設定されます。このコンソールでは、Brand Portal テナントの認証に使用する Adobe Identity Management サービス（IMS）トークンを調達します。

>[!NOTE]
>
>***Experience Manager Assets 6.5 以降の場合***
>
>これまで、Brand Portal は、旧来の OAuth ゲートウェイを通じてクラシックインターフェイスで設定されていました。このゲートウェイは、JSON Web トークン（JWT）交換を使用して認証用の IMS トークンを取得します。
>
>旧来の OAuth を使用した設定は、2020 年 4 月 6 日以降はサポートされなくなり、Adobe Developer Console を使用した設定に変更されました。


>[!TIP]
>
>***既存のお客様のみ（オンプレミス版および Managed Services 版）***
>
>旧来の OAuth ゲートウェイを通じた設定は、既存のお客様には引き続きご利用いただけます。
>
>旧来の OAuth ゲートウェイを通じた設定で問題が発生した場合は、Adobe Developer Console で既存の設定を削除して新しい設定を作成します。

AEM Assets と Brand Portal の連携を設定する手順は、AEM のバージョンと、初めて設定するか既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Brand Portal のライセンス認証](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html?lang=ja) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html?lang=ja) | [設定のアップグレード](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html?lang=ja#upgrade-integration-65) |
