# [ブロガー向け勉強会]見本データ

本マニュアル+サイトの見本データは、2015年11月22日に池袋で行うブロガー向け勉強会用の資料です。

見本データはすぐ右にある【**Download ZIP**】ボタンからダウンロードできます。各自、前もって作業するPCにダウンロードしておくと進行がスムーズになります。

なお、見本サイトは下記のサイトを利用しています。

> * [ぱくたそ - フリー写真素材・無料ダウンロード](https://www.pakutaso.com/)

> * [🌟ゆるいフリーイラスト素材屋「ぴよたそ」](http://hiyokoyarou.com/)

> * [カラー配色で迷わない！シーン別配色見本32パターン | Web制作会社スタイル](http://www.hp-stylelink.com/news/2013/07/20130708.php)

> * [HTMLカラーコード](http://html-color-codes.info/japanese/)

> * [Squarespace Logo — Squarespace](http://www.squarespace.com/logo/)

今回の勉強会用で使った特設サイトはこちら。

> * [Study for bloggers!](http://okutani.net/blog-study/)

***

## テキスト編集ツール(エディタ)

HTMLとCSSは、エディタがあると楽に記述することができます。お使いのPCにAtomエディタをインストールしておくと良いでしょう。

> * [初心者でも使いやすい『Atom』エディタ導入方法【Windows・Mac】 | vdeep](http://vdeep.net/install-atom)

Atomで、

```
html
```

と書いたあとに『tab』キーを押すと

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>

  </body>
</html>
```

が一瞬で表示されて、非常に便利です。これだけでサイトの骨組みができてしまいます。

**※ 追記**

ChromeBookお使いの方はAtomが使えないので**Text**というアプリを使いましょう。

> * [Text](https://chrome.google.com/webstore/detail/text/mmfbcljfglbokpmkimbfghdkjmjhdgbg)

iPadをお使いの方は、専用のアプリを使うか、次のようなWeb上でHTMLが書けるサイトを利用しましょう。

> * [Create a new fiddle - JSFiddle](https://jsfiddle.net/)

また、エディタがなくても『メモ帳』なんかでも書くことができますが、見にくいので、なるべくならエディタを使うことをオススメします。

***

## HTMLとCSSについて

### HTML

> サイトの構造を決めるものです。

> 〇〇.htmlという名前でファイルを作成すると、HTMLのファイルになります。

例えば、「**文字**」「**画像**」「**記事の領域、サイドバーの領域...**」「**リスト**」などなど、

文字だったら、

```html
<p>ここが文字だよ</p>
```

画像だったら、

```html
<img src="hiyoko.png">
```

としてあげることで、コンピュータが「**これは文字**」「**これは画像**」と認識することができます。

この『`<p>`』や『`<img>`』を『**pタグ**』『**imgタグ**』など呼ぶことがあるので、覚えておきましょう。

また、HTMLはSEOに非常に強く結びついているため、

```html
<h1>記事の見出し</h1>
<h2>記事の小見出し</h2>
```

のように、『**文字だけど、他の文字とは重要度が違う**』といった形で使い分けしていきます。

ブログでは適切に見出しをつけてあげると、検索されやすくなるので覚えておきましょう。

***

### CSS

> サイトの見た目を決めるものです。

> 〇〇.cssという名前でファイルを作成すると、CSSのファイルになります。

たとえば、

```css
h1 {
  font-size: 50px;
  color: red;
}
```

とCSSファイルにかいてあげると、h1(見出し)が『文字が50pxと大きくなる』かつ『文字色が赤になる』と見た目が変化します。

ちなみに次のHTMLに対して、

```html
<p class="namae">okutani</p>
<p>25歳の男。趣味は吉祥寺巡り。</p>
```

次のCSSを書くと、

```css
.namae {
  font-size: 30px;
}
```

名前のpタグだけ、文字サイズが30pxになります。

このように、『HTMLタグにくっつけたclassの名前を、CSS側で **. + classの名前** の形式で記述』することで、見た目を変更したいHTMLを分けて指定することができます。

ちなみに、

```html
<p class="namae">okutani</p>
<p>25歳の男。趣味は吉祥寺巡り。</p>
<p class="namae">田中</p>
```

に対して以下のCSSを記述すると、

```css
.namae {
  font-size: 30px;
}
```

「okutani」「田中」の**両方の文字**が、文字サイズ30pxに変更されます。

#### 設定しておくと便利なCSSまとめ

覚えなくても大丈夫です。コピー＆ペーストして使いましょう。メモ用に記述しておきます。

講義内では説明しますが、ここでは詳しく解説はしません。気になる方はGoogleにコピペして調べてみてください。

* 余白とかをすごくいじりやすくしてくれるやつ

```css
* {
  box-sizing: border-box;
}
```

* フォントを良い感じにする

```css
body {
  font-family: Arial, Roboto, "Droid Sans", "游ゴシック", YuGothic, "ヒラギノ角ゴ ProN W3", "Hiragino Kaku Gothic ProN", "メイリオ", Meiryo, sans-serif;
  color: #434343;
}
```

* いい感じに影をつけてくれるやつ

```css
header {
  box-shadow: 0 0 10px 1px #aaa;
}
```

***

### 講義の進め方

講義はZIPファイルの中にある『sample.html』を見本にして、『**index.html**』にAtomエディタ(もしくはその他のエディタ)を使って記述していきます。

> index.htmlという名前にしておくと、TOPページが表示されるときに自動で読み込まれるため、この名前にしています。

HTMLとCSSの基礎が分かれば、かんたんなブログのレイアウトはすぐに変更できるようになるかと思います。

かんたんではありますが、以上でブロガー向け勉強会用のマニュアルとさせていただきます。

勉強会当日はどうぞよろしくお願いいたします。

author: okutani [2015/11/19]
