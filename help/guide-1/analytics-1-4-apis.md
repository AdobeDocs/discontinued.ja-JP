---
title: Adobe Analytics 1.4 APIの提供終了
description: Adobe Analytics 1.4 APIおよびWSSE認証は、2026年8月31日に提供終了となりました。 影響を受ける内容と、Analytics 2.0 APIに移行する方法について説明します。
source-git-commit: 4056ba0953e81a279d25b15449c7b41a4a5eb7f9
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%
---
# Adobe Analytics 1.4 APIの提供終了

2026年8月31日（PT）より、AdobeはAdobe Analytics 1.4 APIおよびWSSE認証を廃止しました。 **&#x200B;**&#x200B;このバージョンのAPIを使用するすべてのエンドポイントにアクセスできなくなり、その上に構築された統合が機能しなくなります。

Adobe Analytics 1.4 APIは、レポート、分類、データフィード、セグメント、計算指標、データソース、レポートスイート設定など、幅広いアクションを提供します。 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0)に置き換えられました。これにより、セグメントや計算指標などのコンポーネントのレポートと管理など、Adobe Analytics ユーザーインターフェイスで使用できるほとんどのアクションを実行できます。 まだアップグレードが必要な統合環境がある場合は、[Adobe Analytics 2.0 APIへの移行](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration)のガイドに従ってください。

## サポート終了

この提供終了は、次の1.4 API機能に直接影響します。 影響を受ける各ワークフローを[Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0)に移行します。

* レポート（Data Warehouse、リアルタイムレポート、パスレポート、概要レポートを含む）
* レポートスイートの設定と管理
* 分類
* セグメント
* 計算指標
* データソース
* データフィード
* ブックマークと会社（エンドポイント）メソッド

また、**Adobe Analytics WSSE認証**&#x200B;も廃止されます（以下の[WSSE認証](#wsse-authentication)を参照）。

>[!IMPORTANT]
>
>この提供終了は、データ収集に&#x200B;*影響しません*。 タグ（旧Adobe Launch）、Web SDK、AppMeasurementなどのタグ付けソリューションは影響を受けません。 [&#x200B; データ挿入API](#data-insertion-api)も&#x200B;*ではなく*&#x200B;廃止されました。 ただし、1.4 データソースまたは分類APIを使用してデータを強化する場合は、これらのワークフローをAdobe Analytics 2.0 APIに移行する必要があります。

## WSSE認証

WSSE認証は、Analytics 1.4 APIでサポートされていたレガシー認証プロトコルです。 [Adobe Developer Console](https://developer.adobe.com/console/home)で提供されているOAuth ベースの認証オプションに置き換えられました。 WSSE認証を使用するプロジェクトは、Adobe Developer Consoleでプロビジョニングされたプロジェクトに資格情報を更新する必要があります。

移行するには、[Adobe Developer Console](https://developer.adobe.com/console/home)にログインし、Analytics 2.0 API統合用のプロジェクトを作成します。 **OAuth ユーザー**&#x200B;または&#x200B;**OAuth サーバー間**&#x200B;認証方法のいずれかを選択します。

## Data Insertion API

Data Insertion APIは、この提供終了の&#x200B;**not**&#x200B;部分です。 ドキュメントは[Adobe Analytics Data Collection API](https://developer.adobe.com/analytics-collection-apis/) サイトに移動し、他のサーバーサイドのコレクションメソッドと一緒に移動しました。

* [Data Insertion API](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/): イベントデータを、クエリ文字列（イメージリクエスト）またはXML `POST`として、一度に1回ずつ送信します。
* [Bulk Data Insertion API](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/): サーバー呼び出しデータのバッチをファイルとしてアップロードします。 Adobeでは、新しいサーバーサイド実装にBulk Data Insertion APIを使用することをお勧めします。

## よくある質問

+++これは、Analytics API用の既存のAdobe Developer プロジェクトに影響しますか？

Analytics 1.4 APIを使用する既存のプロジェクトはすべて影響を受けます。 これらの統合は、[Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)に移行する必要があります。

+++

+++Adobeの資格情報を、Analytics APIを使用する別の製品またはアプリケーションと共有しました。 影響は受けていますか？

その製品またはアプリケーションがWSSE資格情報を使用しているか、Analytics 1.4 APIを呼び出す場合、影響を受け、移行する必要があります。 移行プランとタイムラインについて詳しくは、製品またはアプリケーションのプロバイダーにお問い合わせください。

+++

+++プロジェクトで使用するAPIを判断するにはどうすればよいですか？

プロジェクトが呼び出すベース URLによって、使用するAPI バージョンが決まります。 Adobe Analytics 1.4 APIでは、次のベース URLを使用しました。

* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

[Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)では、次のベース URLが使用されています。

* `https://analytics.adobe.io`

いずれかのAPI プロジェクトが`api*.omniture.com`を呼び出す場合、廃止されたAdobe Analytics 1.4 APIを使用し、2.0 APIに移行する必要があります。

+++

+++サポート終了はデータ収集に影響を与えますか？

いいえ。 この提供終了は、タグ、Web SDK、AppMeasurement、Data Insertion APIなどの直接的なデータ収集に&#x200B;**が影響を与えることはありません**。 ただし、1.4 データソースまたは分類APIを使用してデータを強化する場合は、これらのワークフローをAdobe Analytics 2.0 APIに移行する必要があります。

+++

このページで回答されていない、この提供終了に関するさらなる質問がある場合は、Adobe アカウントチームにお問い合わせください。
