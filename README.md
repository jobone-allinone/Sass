# Sassとは

cssを効率的に書く記法。
下記のようにcssをネストして記述することが可能で、コード量をPureなcssよりも減らすことができます。

ただしSassはそのままhtmlで読み込こんで使用することはできない。Sassをcssに変換（コンパイル）して使用する必要があります。

```css
/* css */
ul {
    padding: 0;
}
ul li{
　　margin: auto;
}
ul li a{
　　color: #fff;
}
```

```scss
/* scss Sassにはsass記法とscss記法の2つがあり、scss記法が一般的に使われる */
ul {
    padding: 0;
    li {
        margin: auto;
        a {
            color: #fff;
        }
    }
}
```

## 使い方
Windowsの場合、RubyInstallerからRubyをインストールする（OS Xの場合は不要です）。

https://rubyinstaller.org/

Rubyインストール後にgemをアップデートする。

```bash
gem install rubygems-update --source http://rubygems.org/
update_rubygems
```

gemアップデート後にSassをインストールする。

```bash
gem install sass
```

## Sassを使ってみる

Bracketsの場合「Brackets Open Terminal」をインストールする。

ファイルツリーを右クリックし、ターミナル（cmd or powershell）を起動し、以下のコマンドを入力する。

![terminal](https://user-images.githubusercontent.com/35711528/36238340-493a15ee-1245-11e8-888e-3ca5ae9d5917.png)

*input.scss を用意すること。

```bash
sass input.scss output.css
```

成功すると
output.cssが作成される。

自動でコンパイルするためには以下のように実行する

```bash
sass --watch input.scss:output.css
```

## 課題
Sassのインストールから自動コンパイル実行までを実施してください。
