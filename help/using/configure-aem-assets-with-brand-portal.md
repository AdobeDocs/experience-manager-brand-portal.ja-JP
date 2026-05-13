---
title: Experience Manager Assets と Brand Portal の連携の設定
description: Experience Manager Assets と Brand Portal の連携の設定について説明します。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
TQID: https://experienceleague.adobe.com/-FF6IXLHoYo485vkZVBaYMrVlZZYys0shOr9OChBlao
product_v2:
  - id: d09181b5-a36a-43de-ba01-36641440bc43
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: da0dfbce-df02-4f8b-b32d-a4e3b1d05085
subfeature_v2:
  - id: e00c7c12-7035-41fe-ad76-1ec82c8c3f01
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: e48edcb1ed5d76686794f7a7ed6389c7f4ab1ed3
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 65%

---

# Experience Manager Assets と Brand Portal の連携の設定 {#configure-integration}

Adobe Experience Manager Assets と Brand Portal の連携を設定すると、Brand Portal ユーザー向けにアセットの公開、アセットの配布、アセットの投稿機能が可能になります。 Experience Manager Assets ユーザーは、Brand Portal ユーザーと共にアセットを公開および配布できます。 Brand Portal ユーザーは、共有アセットにアクセスしたり、アセットを投稿したりできます。アセットを投稿するには、アセット投稿フォルダーに新しいアセットをアップロードし、その投稿フォルダーを Experience Manager Assets に公開します。

Experience Manager Assets と Brand Portal の連携の設定は、次のバージョンでサポートされています。

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets（オンプレミス版および Managed Services 版）6.5 以降

Cloud Manager から Brand Portal をアクティベートすると、Experience Manager Assets as a Cloud Service と Brand Portal の連携が自動的に設定されます。 アクティベーションワークフローにより、バックエンドで必要な設定が作成され、Experience Manager Assets as a Cloud Service インスタンスと同じ IMS 組織に Brand Portal がアクティベートされます。

一方、Experience Manager Assets（オンプレミスおよびマネージドサービス）は、Adobe Developer Consoleを使用してBrand Portalを使用して手動で設定され、Brand Portal テナントの認証のためにAdobe Identity Management サービス（IMS）トークンを取得します。

>[!NOTE]
>
>***Experience Manager Assets、6.5以降***&#x200B;の場合
>
>以前は、従来のインターフェイスでは従来のOAuth Gatewayを使用してBrand Portalを設定していました。このゲートウェイでは、JSON Web Token （JWT）交換を使用してIMS トークンを取得し、認証を取得していました。
>
>従来のOAuthによる設定は、2020年4月6日からサポートされなくなり、Adobe Developer Consoleによる設定に変更されました。


>[!TIP]
>
>***既存のお客様のみ（オンプレミス版および Managed Services 版）***
>
>従来のOAuth ゲートウェイ設定は、引き続き既存の顧客に対して機能します。
>
>従来のOAuth Gateway設定で問題が発生した場合は、既存の設定を削除し、Adobe Developer Consoleを介して新しい設定を作成します。

AEM Assets と Brand Portal の連携を設定する手順は、AEM のバージョンと、初めて設定するか既存の設定をアップグレードするかによって異なります。

| **AEM のバージョン** | **新しい設定** | **設定のアップグレード** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Brand Portal のライセンス認証](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal) | - |
| **AEM 6.5（6.5.4.0 以降）** | [設定の作成](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal) | [設定のアップグレード](https://experienceleague.adobe.com/ja/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) |
