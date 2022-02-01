# text

- [text\-align](https://developer.mozilla.org/ja/docs/Web/CSS/text-align): テキストの横方向の位置指定
  - `justify`: 両端揃え

## はみ出し

- はみ出し分の調整
  - [overflow－CSSリファレンス](http://www.htmq.com/css/overflow.shtml)
  - はみ出す(default): `overflow: visible;`
  - はみ出し分を非表示: `overflow: hidden;`
  - スクロールバー: `overflow: scroll;`
  - ユーザエージェントに依存: `overflow: auto;`
  - **display: none:** `overflow: no-display;`
  - **visiblity: hidden;** : `overflow: visible;`
- CJK (中国語、台湾語、日本語、韓国語)について：後述

## 改行

### 改行を防止する場合

```css
/* no break line */
white-space: nowrap;
```

### 強制改行する場合

いくつか条件が重なってくるが基本これで良いはず

```css
/* force break line (typical languages) */
word-break: break-all;
word-wrap: break-word;
```

### CJK (中国語、台湾語、日本語、韓国語)

いわゆる漢字を持つ言語(中国語、台湾語、日本語、韓国語)はCJKと言われて改行のルールが異なっているらしい。
[word\-break \- CSS: カスケーディングスタイルシート \| MDN](https://developer.mozilla.org/ja/docs/Web/CSS/word-break)
そのため、urlなどCJK以外で構成される文字については別途考慮が必要

ざっくり感覚でいうと、CJKは文字に関係なく改行が入るっぽい(単語ごとにスペースが入らないからかな)

### links

- [CSS での横幅 \(width\) 、高さ \(height\) の指定にキーワード値を使う \- Qiita](https://qiita.com/qed/items/ef5688118ce78985c9ab)
- [word\-break \- CSS: カスケーディングスタイルシート \| MDN](https://developer.mozilla.org/ja/docs/Web/CSS/word-break)
