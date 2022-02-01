# grid

縦横の統一を気にして配置の設定を行う

- ざっくりと連続要素(repeat)の配置と、areaでの名前指定の2種類がある
- `display: grid;` により直下のタグがgird配置対象になる
- 縦と横が方眼用紙のように設定され複数行/複数列になっても幅/高さが揃えられる
  - flexはそれぞれの行、列ごとに計算するためずれる
- minmax: 単体でセットすると、なるべく小さく収まるように動作する
- repeat: 指定の繰り返しを設定する
  - [repeat\(\) \- CSS: カスケーディングスタイルシート \| MDN](https://developer.mozilla.org/ja/docs/Web/CSS/repeat())
  - auto-fill / auto-fit: なるべく1行(列)に収まるように各要素を最大で取ろうとする。(minmaxなど最大幅を持つ設定がされている場合)
    - auto-fit は内部要素が空の時0サイズとして扱う(折りたたまれる)
- 並びを逆順にする: `direction: ltr;` or `direction: rtl;` (本来言葉の書き方向を設定するもののため使い方が違うかもしれない)

## 連続要素(repeat)

この例では、内部要素が 100px~200px 幅で配置される、合計幅が親の幅を超える場合は改行される

```css
    #grid-repeat {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(100px, 200px));
    }
```

以下のように、固定で記載することも可能で、repeaatを混ぜても良い

```css
    #grid-repeat {
        display: grid;
        grid-template-columns: 100px 100px;
    }
```

## area指定

行列を区切って各要素に名前(area)を割り当てる。同名をセットすると合体する
note: 以下の例ではdが設定されていないため、どこかに行く(連続要素として扱われる？)

```css
    #grid-area {
        display: grid;
        grid-template:
            "a b" 100px
            "c c" 200px
            / 100px 200px;
    }
    #grid-area .a {
        grid-area: a;
    }
    #grid-area .b {
        grid-area: b;
    }
    #grid-area .c {
        grid-area: c;
    }
    #grid-area .d {
        grid-area: d;
    }
```
