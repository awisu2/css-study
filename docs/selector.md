# selector

## selector

- `+`: 同じ親を持つタグ群で、隣接しているタグを選択(`a + p`とした場合pが選択される)
  - `{parent} > * + *`: 特定の子群の先頭以外

## Pseudo classes: 擬似クラス

[擬似クラス \- CSS: カスケーディングスタイルシート \| MDN](https://developer.mozilla.org/ja/docs/Web/CSS/Pseudo-classes)

- `{element?}:nth-child(An+B)`: match nth item in children(1~)
  - `*:nth-child(1)`, `:first-child`: match first
  - `*:nth-child(5)`: 5th
  - `*:nth-child(3n)`: matches a multiple of 3
  - `*:nth-child(odd)`: 奇数
  - `*:nth-child(even)`: 偶数
  - `*:nth-child(-n+3)`: first three
  - `p:nth-child(n+3)`: p and the third and subsequent child elements
  - [:nth\-child\(\) \- CSS: カスケーディングスタイルシート \| MDN](https://developer.mozilla.org/ja/docs/Web/CSS/:nth-child)
