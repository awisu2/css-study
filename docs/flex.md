# flex

行毎を基準に配置をコントロールする

## 親要素に指定

- flexする: `display: flex;`
- 子要素間の幅: `gap: {size};`
- 垂直方向の揃え: `align-items: {stretch|flex-start|flex-end|center|baseline};`
  - flex-direction の設定により 縦横が変化
  - stretch: 行の最大サイズに合わせるて拡張
  - flex-start: 行の上に合わせる
  - flex-end: 行の下に合わせる
  - center: 行の中央に要素で合わせる
  - baseline: 行の中央に文字の土台ラインで合わせる
- 折返しの設定: `flex-wrap: {nowrap|wrap|wrap-reverse}`
  - wrap: 折り返しあり
- 並ぶ方向: `flex-direction: {row|row-reverse|column|column-reverse}`

## 子要素に指定

- `flex-grow: {num};`: どの割合で伸びるか(行に含まれる要素の合算が母数)
- `flex-shrink: {num};`: どの割合で縮むか(行に含まれる要素の合算が母数)
- `flex-basis: {auto|size};`: ベースサイズ
  - size はcssの標準サイズ
- `flex`: flex-grow、flex-shrink, flex-basis を一括指定(default: 0 1 auto)
