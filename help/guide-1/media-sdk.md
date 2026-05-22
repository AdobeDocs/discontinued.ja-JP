---
title: Adobe Media SDK（バージョン 1.xおよび2.x）の提供終了に関するFAQ
description: Adobe Media SDK バージョン 1.xおよび2.x （旧Video Heartbeat Library）の提供終了に関するよくある質問に対する回答を示します。
source-git-commit: d014c200dd926ccf0116faa50c4bffb1d234e926
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 1%

---


# Adobe Media SDK（バージョン 1.xおよび2.x）の提供終了に関するFAQ

Adobe Media SDK **2.xは2021年8月31日にサポート終了となりました**。 ビデオハートビートライブラリ （VHL） **1.xは非推奨です**。数年間サポートされていません。

## 何が起きているのでしょうか？

オリジナルのビデオハートビートライブラリ（VHL）は、後にMedia SDKに改名され、オーディオとビデオの分析用にクライアントサイドのトラッキングを提供しました。 Adobeは、追跡機能を新しい、より有能な実装に移行しました。

* **Media SDK 3.x （Analyticsのみ）:**&#x200B;現在サポートされています。 Media Collection APIを使用してメディアを追跡します。 Edge Networkに移行できない既存の2.x ユーザーに推奨されます。
* **Edge Network向けStreaming Media （推奨）:**&#x200B;現在おすすめの実装。 Adobe Experience Platform Web SDK、モバイル SDK、Media Edge APIを使用して、Edge Networkを通じてメディアデータを送信し、Adobe Analytics、Customer Journey Analytics、Real-Time CDP、Adobe Journey Optimizerをまたいで使用できるようにします。

## 何が終末期に含まれ、何が含まれていないのか？

**提供終了（サポート終了）:**

* ビデオハートビートライブラリ（VHL） 1.x – すべてのプラットフォーム（Android、iOS、JavaScript、Apple TV、Chromecast、Roku、TVML）
* Media SDK 2.x — Android、iOS、JavaScript

**提供終了ではありません（引き続きサポートされています）:**

* Media SDK 3.x — JavaScript、Chromecast、Roku （Analyticsのみ）
* Edge Network向けStreaming Media — サポートされるすべてのプラットフォーム

## バージョン 1.xと2.xが廃止されたのはなぜですか？

バージョン 3.0以降、Media SDKはMedia Collection APIを直接使用するように再設計され、デリゲート パターンの必要性がなくなり、トラッカーの作成が簡素化されました。 古い1.x SDKと2.x SDKは、それ以降に置き換えられたハートビートサーバーアーキテクチャに依存していました。

Adobeでは、Edge Networkの導入により、従来のハートビート SDKではサポートできなかった、複数のダウンストリームのAdobe アプリケーションをフィードできる単一のデータ収集パイプラインを提供できるようになりました。

## アーカイブされたドキュメントはどこにありますか？

従来のドキュメントはGitHubにアーカイブされており、参照可能です。

| バージョン | ステータス | アーカイブされたドキュメント |
|---|---|---|
| 1.x （ビデオハートビートライブラリ） | 非推奨（廃止予定） | [`video-heartbeat` GitHub リポジトリ &#x200B;](https://github.com/Adobe-Marketing-Cloud/video-heartbeat/tree/master/docs) |
| 2.x （Media SDK） | サポート終了2021年8月31日 | [`media-sdks` GitHub リポジトリ &#x200B;](https://github.com/Adobe-Marketing-Cloud/media-sdks/blob/master/docs/2.x/README.md) |

## 移行オプションは何ですか？

**オプション 1: Media SDK 3.xへの移行（Analyticsのみ）**

2.xを使用しており、Adobe Analyticsのみを使用している場合は、3.xへの移行が最も簡単です。 完全なAPIの比較とコード例については、[2.xから3.xへの移行ガイド &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)を参照してください。

**オプション 2: Edge Network用ストリーミングメディアへの移行（推奨）**

新しい実装の場合や、複数のAdobe アプリケーションでデータを使用する場合は、Adobe Experience Platform Edge Networkを使用します。

* [Media Edge Web SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-web-sdk.html)
* [Media Edge Mobile SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [Media Edge API](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge-api.html)

## FAQ

+++**RokuとChromecast SDKのサポートは影響を受けますか？**

いいえ。 Roku SDKとChromecast SDKは、Media SDK 3.x （Analyticsのみ）の一部として引き続き利用可能であり、サポートされています。 この提供終了は、1.xおよび2.x バージョンのみを対象としています。

+++

+++**Media Analytics JavaScript SDKの実装には影響がありますか？**

いいえ。 JavaScript SDK for Media Analyticsを使用しているお客様は、引き続きスタンドアロンのSDKまたはタグ拡張機能を使用できます。

+++

+++**私はまだMedia SDK 2.xを使用しています。 どうすればよいですか。**

Adobeでは、すべての新規プロジェクトについて、Edge Networkの実装に移行することをお勧めします。 中間ステップが必要な場合は、[JavaScript SDK 2.xから3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)に移行してから、Edge Networkへの移行を計画します。

+++

+++**サポートされている実装に移行する労力のレベルを教えてください。**

移行の労力は、顧客ごとの実装によって異なります。 移行ドキュメントを確認した後、追加のサポートについては、コンサルティングまたはカスタマーケアにお問い合わせください。

* [Mobile Edge SDK（AndroidおよびiOS）を使用したストリーミングメディアの実装](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [JavaScript SDK 2.xから3.xへの移行](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)

+++

+++**Adobe Experience Platform Tagsをタグ管理システムとして使用する必要がありますか？**

モバイルアプリの実装では、Experience Platform Tagsは、webと同様にタグ管理システムとして使用されません。 SDK拡張機能を設定するには、タグ UIが必要です。 これは、Mobile v4 SDKの設定にAdobe Mobile Services UIを使用した場合と同様です。 タグには、選択した拡張機能に基づいてカスタマイズされたインストール手順が表示されます。

+++

+++**このサポート終了は、tvOS向けSDKに影響しますか？**

はい。 tvOS （バージョン 10以降）の場合は、Adobe Experience Platform Mobile SDKを使用してEdge Network用Streaming Mediaに移行することをお勧めします。 詳しくは、[&#x200B; モバイル Edge SDKを使用したストリーミングメディアの実装](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)を参照してください。

+++

+++**このサポート終了は、SDK for Fire TVおよびAndroid TVに影響しますか？**

はい。 Fire TVおよびAndroid TVの場合は、Adobe Experience Platform Mobile SDKを使用してEdge Network用のStreaming Mediaに移行することをお勧めします。 詳しくは、[&#x200B; モバイル Edge SDKを使用したストリーミングメディアの実装](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)を参照してください。

+++

+++**Mobile v4 SDKの提供終了に関する情報はどこで入手できますか？**

[Mobile Servicesの提供終了に関するFAQ](mobile-services.md)を参照してください。 Mobile Services プラットフォームとMobile v4 SDKは、2022年12月31日に提供終了となりました。

+++

+++**質問がある場合はどこに行けばよいですか？**

移行サポートについては、Adobe アカウントチームまたはAdobe カスタマーケアにお問い合わせください。

+++

>[!MORELIKETHIS]
>
>* [&#x200B; ストリーミングメディア実装の概要](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/overview.html?lang=ja)
>* [Edge Network用ストリーミングメディア &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge.html?lang=ja)
>* [Media SDK 3.x — JavaScript設定](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/web-implementation.html?lang=ja)
