---
keywords: デバイスグラフ；提供終了
title: デバイスグラフ
description: デバイスグラフの提供終了プランについて説明します。
source-git-commit: b090d9f4f4040143b0d2847464785c7ad35de545
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 4%

---

# デバイスグラフの提供終了

>[!WARNING]
>
>クロスデバイス分析内のデバイスグラフは、**2025 年 12 月 31 日** をもって使用できなくなりました。 現在のデバイスグラフが有効な仮想レポートスイートを、[&#x200B; フィールドベースの方法 &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/cda/field-based-stitching) に切り替えてください。

クロスデバイス分析では、プライベートグラフを使用してデータをつなぎ合わせました。 プライベートグラフは、組織に固有の、ハッシュ化されたデバイス ID のリポジトリです。 CDA は、デバイスグラフと定期的に通信し、デバイスをリンクします。

## デバイスグラフに固有の前提条件

デバイスグラフ方式を使用してクロスデバイス分析を実装する場合は、次が必要でした。

>[!WARNING]
>
>すべての前提条件を満たさないと、データをステッチする際に、クロスデバイス分析を有効にできず、結果が悪くなる場合があります。

* 組織は、[Adobe Experience Platform ID サービスのプライベートグラフ &#x200B;](https://business.adobe.com/products/experience-platform/identity-service.html) を使用する必要があります。 『 ID サービスユーザガイド』の [&#x200B; ホームページ &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html) も参照してください。
* 実装では、最新バージョンのExperience Cloud ID サービス（ECID）を使用する必要があります。 ID サービスユーザーガイドの [&#x200B; ホームページ &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja) を参照してください。 Adobe Experience Platformの [&#x200B; タグ &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ja) を使用するほとんどの実装では、既に ID サービスがデプロイされている可能性があります。
* ユーザーがログインしたりメールを開いたりする場合など、個人を識別できる場合は、常に `setCustomerIDs` 関数（またはSDKと同等の関数）を呼び出す必要があります。 この要件は、すべてのプラットフォーム（使用する場合はモバイルアプリを含む）に適用されます。 ID サービスユーザーガイドの「[`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html)」を参照してください。

## デバイスグラフに固有の制限

* 従来の Analytics ID はサポートされていません。 Experience Cloud ID のを持つ訪問者のみをステッチします。
* 組織がプライベートグラフを使用している場合、新しいデバイスをステッチするには最大 24 時間かかります。
* サードパーティのデバイスグラフはサポートされていません。

