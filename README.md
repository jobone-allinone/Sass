# Sassの書き方

## scssは子要素は入れ子で書ける

```scss
// scssでの入れ子の書き方
#content {
    background-color: #e1e1e1;
    .second-title {
        font-size: 0.8em;
        text-decoration: underline #90c23a;
    }
}
```

```css
/* 上記のscssはこのcssのようにコンパイルされる */
#content {
    background-color: #e1e1e1;
}
#content .second-title {
    font-size: 0.8em;
    text-decoration: underline #90c23a;
}
```

```scss
// scssでの入れ子の書き方
ul.nav li a {
    padding-left: 20px;
    padding-right: 20px;
    &:hover { // &は親要素を表す
        color: #fff;
        text-underline-position: left;
        text-decoration: none;
    }
}
```

```css
/* 上記のscssはこのcssのようにコンパイルされる */
ul.nav li a {
    padding-left: 20px;
    padding-right: 20px;
}
ul.nav li a:hover {
    color: #fff;
    text-underline-position: left;
    text-decoration: none;
}
```

## 変数を使う

```scss
// scssは$で変数を使える
$whitecolor: #fff;
main {
    background-color: $whitecolor;
}
```

```css
/* 上記のscssはこのcssのようにコンパイルされる */
main {
    background-color: #fff;
}
```

## 継承を使う

```scss
.under-line-extend {
    content: "";
    position: absolute;
    left: 50%;
    margin-left: -16px;
    height: 10px;
    width: 32px;
    border-bottom: 2px solid $blackcolor;
}

.info-content {
    @extend .under-line-extend;
    top: 67%;
}
```

```css
/* 上記のscssはこのcssのようにコンパイルされる */
.info-content {
  content: "";
  position: absolute;
  left: 50%;
  margin-left: -16px;
  height: 10px;
  width: 32px;
  border-bottom: 2px solid #000;
}
.info-content {
    top: 67%;
}
```

## 課題

上記の入れ子・変数・継承等を利用して課題サイトを作成してください。

## 参考

「ドットインストール Sass入門」をざっくり一周した

http://373.hatenadiary.jp/entry/2017/05/31/143301

公式ドキュメント

http://sass-lang.com/documentation/
