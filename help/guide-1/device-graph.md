---
keywords: Device-graph;end-of-life
title: デバイスグラフ
description: デバイスグラフの提供終了プランについて説明します。
source-git-commit: d014c200dd926ccf0116faa50c4bffb1d234e926
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 4%

---

# デバイスグラフの提供終了

>[!WARNING]
>
>クロスデバイス分析内のデバイスグラフは、**2025年12月31日**&#x200B;をもって使用できなくなりました。 現在のデバイスグラフで有効になっている仮想レポートスイートを[ フィールドベースのメソッド ](https://experienceleague.adobe.com/en/docs/analytics/components/cda/field-based-stitching)に切り替えてください。

クロスデバイス分析では、プライベートグラフを使ってデータをつなぎ合わせました。 プライベートグラフは、組織に固有のハッシュ化されたデバイス IDのリポジトリです。 CDAは、デバイスグラフと定期的に通信してデバイスをリンクさせます。

## デバイスグラフに固有の前提条件

デバイスグラフ方式を使用してクロスデバイス分析を実装する場合は、以下が必要でした。

>[!WARNING]
>
>すべての前提条件を満たせない場合、クロスデバイス分析を有効にできないか、データを結合する際に結果が悪くなる可能性があります。

* お客様の組織では、[Adobe Experience Platform Identity Service Private Graph](https://business.adobe.com/products/experience-platform/identity-service.html)を使用する必要があります。 Identity Service ユーザーガイドの[ ホームページ ](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html)も参照してください。
* 実装では、最新バージョンのID サービス（ECID）を使用する必要があります。 ID サービスユーザーガイドの[ ホームページ ](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)を参照してください。 Adobe Experience Platformで[ タグ ](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja)を使用しているほとんどの実装では、既にID サービスがデプロイされている可能性があります。
* ユーザーがログインしたり、メールを開いたときなど、個人を識別できる場合は、実装で`setCustomerIDs`関数（またはSDK相当）を呼び出す必要があります。 この要件は、使用される場合、モバイルアプリを含むすべてのプラットフォームに適用されます。 ID サービスユーザーガイドの[`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html)を参照してください。

## デバイスグラフに固有の制限

* 従来のAnalytics IDはサポートされていません。 ECIDを持つ訪問者のみがステッチされます。
* 組織でプライベートグラフを使用している場合、新しいデバイスのステッチに最大24時間かかります。
* 3rd パーティのデバイスグラフはサポートされていません。

