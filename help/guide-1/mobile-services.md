---
title: Adobe Mobile Services の提供終了に関する FAQ
description: AdobeMobile Services の提供終了のお知らせに関するよくある質問への回答を得ます。
exl-id: c5f44341-7b87-4530-b86e-17e2911a7959
source-git-commit: 343e0a727c570c9eec503d7903d0477134fc6189
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 100%

---

# Adobe Mobile Services の提供終了に関する FAQ

Adobe Mobile Service の提供終了日は、**2022年12月31日（PT）**&#x200B;でした。

## 何が起きているのでしょうか？

Mobile Services は、2022年12月31日（PT）に提供終了となりました。モバイル中心の UI、獲得、ディープリンク、アプリ内メッセージ、プッシュ通知および位置情報をサポートする Mobile Services は、この日以降サポート対象ではなくなりました。

## 対象となるものと、ならないものは何でしょうか？

この提供終了には、[mobilemarketing.adobe.com](https://mobilemarketing.adobe.com) のスタンドアロンプラットフォームである Adobe Mobile Services のみが含まれます。このインターフェイスに依存する Mobile バージョン 4 SDK は、2021年8月31日（PT）に廃止されました。

この提供終了には、Adobe Experience Platform Mobile SDK の一部であるモバイルアプリ用の Adobe Analytics は含まれません。アプリ内動作、ライフサイクル分析、メッセージングインタラクショントラッキング、オーディエンスプロファイルなど、これらの機能は、引き続きアドビからサポートを受けることができます。

## 機能を廃止するのはなぜですか？

アドビがモバイルマーケティング機能を拡張し続けるにつれて、Mobile Services で以前に使用可能だった機能は、Adobe Experience Cloud ソリューションでリリースするか、Adobe Exchange プレミアパートナーを通じて提供する予定です。この移行により、より強力で柔軟なモバイルマーケティング機能を提供します。

## Mobile Services で作成した既存の処理ルールはどうなりますか？

Mobile Services UI で作成または生成した[処理](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=ja)ルールは、Mobile Services の提供終了日よりも前に Adobe Analytics に自動的に移行されます。移行された処理ルールは、Adobe Analytics の他の処理ルールと同様に動作し、自由に表示または編集できます。この移行にユーザーのアクションは必要ありません。

Mobile Services の廃止後、すべての処理ルールロジックは、通常は[コンテキストデータ変数](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/contextdata.html?lang=ja)の使用を含め、Adobe Analytics 内で排他的に処理されます。

## 使用可能な移行オプションは何ですか？

アドビでは、組織のユースケースに応じて 3 つの移行パスを提供します。

1. **アプリ内メッセージおよびプッシュ通知**：アドビは、メッセージングワークフローを Adobe Journey Optimizer に移行できます。この製品は、組織がモバイルメッセージングを含むカスタマージャーニー全体にわたるエクスペリエンスを最適化し、パーソナライズするのに役立ちます。
1. **獲得とディープリンク**：獲得とディープリンクは、Adobe Exchange プレミアパートナープログラムを通じて提供します。アドビのパートナーシップチームは、お客様のニーズに最適なソリューションを確実に見つけられるよう、適切な紹介を行うことができます。
1. **Places Service**：Places Service は、無料の位置情報機能を提供します。[Places Service ドキュメント](https://experienceleague.adobe.com/docs/places/using/home.html?lang=ja)を参照してください。

## 質問がある場合は、どこに問い合わせればよいですか？

詳しくは、[Adobe Mobile Services の提供終了の Spark Page](https://spark.adobe.com/page/C6D30y09zaRpD/) を参照してください。その他のご質問については、アドビ担当者にお問い合わせください。
