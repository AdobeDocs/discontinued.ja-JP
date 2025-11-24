---
title: 非表示のテスト
description: これは隠されたテストです
hide: true
hidefromtoc: true
landing-page-breadcrumb-title: Test AEM 6.5
landing-page-name: experience-manager-65
feature: Annotations
exl-id: e6e5ba1c-98a5-4d7d-9913-426df31bc7a3
source-git-commit: 32a5873bea2428daa2d432234fc005641523d35c
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# 非表示のテスト

これは隠されたテストです。 v2 レンダリングで正常に動作することを確認するために、この `[` を追加します。

## 新しいタブで開く

`[See What's new](auditor.md) {target="_blank"}`

[同じタブで開く](auditor.md)

[ 引用符で囲まれたスペースを含む新しいタブ ](auditor.md) {target="_blank"}

[アンカー付きの新しいタブ](auditor.md#_blank)

[ 引用符で囲まれたスペースのない新しいタブ ](auditor.md){target="_blank"}

[ 引用符のないスペースを含む新しいタブ ](auditor.md) {target=_blank}

[ 引用符なしの新しいタブ ](auditor.md){target=_blank}

[ ディープリンクを含む新しいタブ ](commerce-channels.md#channel-manager-extension){target="_blank"}

[ ディープリンクを使用した新しいタブのアンカー ](https://experienceleague.adobe.com/en/docs/analytics/analyze/home#key-analytics-resources#_blank)

[ 外部リンクを含む新しいタブ ](https://www.adobe.com){target="_blank"}

[ 新しいタブのルートリンク ](/help/guide-1/auditor.md){target="_blank"}


<table>
  <tr>
    <th>引用符付き</a></th>
    <th>引用符なし</th>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com" target="_blank">Adobeの新しいタブ</a></td>
    <td><a href="https://www.adobe.com" target="_blank">Adobeの新しいタブ</td>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com">Adobe：新しいタブなし</a></td>
    <td><a href="https://www.adobe.com">Adobe：新しいタブなし</td>
  </tr>
</table>

## テストをコメント

2025 年 11 月 18 日（Pt）

<!-- ## Comment with basic text

This is a new line.

Second new line. -->


以下にコメントします。 この記事で最後に表示される場合は、コメント構文が原因です。

1. **[!UICONTROL 作成]** をクリックします。

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

この行はコメントの後にあります。

## ビデオテスト

### プレーンビデオ トランスクリプトなし – metadata.md が流れ落ちるので、トランスクリプトを表示します。

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true)

### トランスクリプトを true に設定した場合

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true){transcript=true}

### トランスクリプトが false に設定されている場合 – ビデオトランスクリプトは表示されません

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true){transcript=false}

## 相対リンク

* [概要](overview.md)
* [検索と昇格](search-promote.md)
* [Social](social.md)

## 明示的なディープリンク

[概要の追加（ルート）](/help/guide-1/overview.md#additional-products)

[概要の追加](overview.md#additional-products)

## ホバーテキスト テスト {#this-is-a-heading-anchor}

ホバーテキストなし

```
![alt text](assets/maui-flip.jpg)
```

![ 代替テキスト ](assets/maui-flip.jpg)


はいホバーテキスト

```
![alt text](assets/maui-flip.jpg "Hover text")
```

![ 代替テキスト ](assets/maui-flip.jpg " ホバーテキスト ")

## スライド

構文：

```
>[!SLIDE](analyze-project)
https://experienceleague-stage.adobe.com/en/slides/analyze-project
```

レンダリング：

<!--
>[!SLIDE](analyze-project)
-->

Bob：トピックが見つかったら、スライドのコメントを削除します。

