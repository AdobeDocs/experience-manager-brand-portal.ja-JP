---
title: Experience Manager Assets と Brand Portal の連携の設定
description: Experience Manager Assets と Brand Portal の連携の設定について説明します。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: f4add370fd3242f5506e5cc4d921362e2b14141a
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 60%

---

# Experience Manager Assets と Brand Portal の連携の設定 {#configure-integration}

Adobe Experience Manager Assets と Brand Portal の連携を設定すると、Brand Portal ユーザー向けにアセットの公開、アセットの配布、アセットの投稿機能が可能になります。Experience Manager Assets ユーザーは、Brand Portal ユーザーとアセットを公開および配布できます。 Brand Portal ユーザーは、共有アセットにアクセスしたり、アセットを投稿したりできます。アセットを投稿するには、アセット投稿フォルダーに新しいアセットをアップロードし、その投稿フォルダーを Experience Manager Assets に公開します。

Experience Manager Assets と Brand Portal の連携の設定は、次のバージョンでサポートされています。

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets（オンプレミス版および Managed Services 版）6.5 以降

Cloud Manager から Brand Portal をアクティベートすると、Experience Manager Assets as a Cloud Service と Brand Portal の連携が自動的に設定されます。アクティベーションワークフローにより、バックエンドで必要な設定が作成され、Experience Manager Assets as a Cloud Service インスタンスと同じ IMS 組織に Brand Portal がアクティベートされます。

一方、Experience Manager Assets（オンプレミス版および Managed Service 版）とBrand Portalの連携は、Adobe Developer Consoleを使用して手動で設定されます。これにより、Brand Portal テナントの認証に使用するAdobe Identity Management Services （IMS）トークンが調達されます。

>[!NOTE]
>
>***Experience Manager Assets, 6.5 以降***
>
>以前は、クラシックインターフェイスは、レガシー OAuth ゲートウェイを使用してBrand Portalを設定していました。このゲートウェイでは、JSON web トークン（JWT）交換を使用して認証用の IMS トークンを取得します。
>
>従来の OAuth を使用した設定は、2020 年 4 月 6 日（PT）以降はサポートされなくなり、Adobe Developer Consoleを使用した設定に変更されました。


>[!TIP]
>
>***既存のお客様のみ（オンプレミス版および Managed Services 版）***
>
>既存のお客様は、レガシー OAuth ゲートウェイ設定が引き続き機能します。
>
>従来の OAuth Gateway 設定で問題が発生した場合は、Adobe Developer Consoleから既存の設定を削除して新しい設定を作成します。

AEM Assets と Brand Portal の連携を設定する手順は、AEM のバージョンと、初めて設定するか既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Brand Portal のライセンス認証](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal) | [設定のアップグレード](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) |
