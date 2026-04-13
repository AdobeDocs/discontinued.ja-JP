---
title: 非表示のテスト
description: これは隠れたテストです
hide: true
landing-page-breadcrumb-title: Test AEM 6.5
landing-page-name: experience-manager-65
feature: Annotations
exl-id: e6e5ba1c-98a5-4d7d-9913-426df31bc7a3
source-git-commit: c12654fbc3d13ff53fd5daf3ba5ba2978c3922ca
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 7%

---

# 非表示のテスト

2026年3月17日 – `hold: true`はオフです。

2026年4月13日 – マットがテスト中

新しいキーのテスト

これは隠れたテストです。 この`[`を追加して、v2 レンダリングで正常に動作することを確認します。

## 新しいタブで開く {#section_92882928}

`[See What's new](auditor.md){target="_blank"} `

[同じタブで開く](auditor.md)

[引用符で囲んだスペースを含む新しいタブ &#x200B;](auditor.md){target="_blank"} 

[&#x200B; アンカー付きの新しいタブ &#x200B;](auditor.md){target=_blank}

[引用符で囲まれた新しいタブ](auditor.md){target="_blank"}

[引用符のないスペースを含む新しいタブ &#x200B;](auditor.md){target=_blank} 

[引用符のない新しいタブ](auditor.md){target=_blank}

[ディープリンク付きの新しいタブ](commerce-channels.md#channel-manager-extension){target="_blank"}

[ディープリンク付きの新しいタブの固定](https://experienceleague.adobe.com/ja/docs/analytics/analyze/home#key-analytics-resources){target="_blank"}

[外部リンク付きの新しいタブ](https://www.adobe.com/jp){target="_blank"}

[新しいタブルートリンク](/help/guide-1/auditor.md){target="_blank"}


<table>
  <tr>
    <th>引用符で囲む</a></th>
    <th>引用符なし</th>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com/jp" target="_blank">Adobeの「新規」タブ</a></td>
    <td><a href="https://www.adobe.com/jp" target="_blank">Adobeの「新規」タブ</td>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com/jp">Adobeの「新しいタブなし」</a></td>
    <td><a href="https://www.adobe.com/jp">Adobeの「新しいタブなし」</td>
  </tr>
</table>

## コメントテスト

2025年11月18日（PT）

<!-- 
## Comment with basic text

This is a new line.

Second new line. 
-->


以下にコメントしてください。 この記事で最後に見られるのは、コメント構文によるものです。

1. 「**[!UICONTROL 作成]**」をクリックします。

<!-- 
## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. 
-->

この行はコメントの後にあります。

## ビデオテスト

### 平易な動画が文字起こしなし – metadata.mdがトリクルダウンするので、文字起こしを表示する必要があります

>[!VIDEO](https://video.tv.adobe.com/v/3409660?captions=jpn&hidetitle=true)

### 文字起こしをtrueに設定

>[!VIDEO](https://video.tv.adobe.com/v/3409660?captions=jpn&hidetitle=true){transcript=true}

### 文字起こしをfalseに設定すると、ビデオの文字起こしが表示されない

>[!VIDEO](https://video.tv.adobe.com/v/3409660?captions=jpn&hidetitle=true){transcript=false}

## 相対リンク

* [概要](overview.md)
* [検索して宣伝](search-promote.md)
* [Social](social.md)

## 明示的なディープリンク

[概要追加（ルート）](/help/guide-1/overview.md#additional-products)

[概要その他](overview.md#additional-products)

## テキストのホバーテスト {#this-is-a-heading-anchor}

テキストにカーソルを合わせる

```
![alt text](assets/maui-flip.jpg)
```

![alt text](assets/maui-flip.jpg)


はいテキストにカーソルを合わせる

```
![alt text](assets/maui-flip.jpg "Hover text")
```

![代替テキスト &#x200B;](assets/maui-flip.jpg " テキストにカーソルを合わせる")

## スライド

構文：

```
>[!SLIDE](analyze-project)
https://experienceleague-stage.adobe.com/en/slides/analyze-project
```

レンダリングされました：

<!--
>[!SLIDE](analyze-project)
-->

Bob: トピックのロックをテストしたら、スライドコメントを削除します。
