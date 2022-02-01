# scroller

親要素の高さに合わせ内部要素が超えた場合にscrollするようにする
タグを2重に用意する必要あり

```css
.scroller {
  @apply relative h-full min-h-full;

  > *:first-child {
    @apply absolute top-0 left-0 w-full h-full overflow-scroll;
  }
}
```

```html
<div class="scroller" style="width: 100px;">
    <div>
        any content
    </div>
</div>
```
