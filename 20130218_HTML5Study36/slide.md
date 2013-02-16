
現実解を探してみよう。





# HTML5じゃないサイトからHTML5を考える。<span class="yellow">It is not HTML5. but ...</span>

### HTML5とか勉強会 2013/02/18

　<a href="http://sadah.github.com" target="_blank">ひらい さだあき</a> <a href="http://twitter.com/sada_h">@sada_h</a>


## ひらい さだあき

* html5j.org / HTML5とか勉強会 スタッフ
* <a href="http://sadah.github.com" target="_blank">sadah.github.com</a> / <a href="http://twitter.com/sada_h" target="_blank">@sada_h</a> / <a href="http://d.hatena.ne.jp/j7400157" target="_blank">techlog</a>
* Kamakura, Born in 1981.
* Ruby / Rails / HTML5 / JavaScript / Java
    * 最近の悩み => ruby で console.log() しちゃう。
* Kakaku.com, Inc. Engineer 2012/08〜
    * <a href="http://tabelog.com/" target="_blank">グルメ・レストランガイド [食べログ]</a>
    * <a href="http://yoyaku.tabelog.com/" target="_blank">レストラン予約サイト [cena(チェーナ)]</a>

 <a href="http://twitter.com/sada_h" target="_blank"><img src="images/profile.jpg" alt="ひらい さだあき" style="max-width:100px;vertical-align:middle;" /></a>
<a href="http://tabelog.com" target="_blank"><img src="images/tabelog.gif" alt="食べログ" style="vertical-align:middle;" /></a>
<a href="http://yoyaku.tabelog.com" target="_blank"><img src="images/cena.png" alt="レストラン予約サイト cena(チェーナ)" style="vertical-align:middle;background-color:#fff;" /></a>


**この資料の内容は私の個人的な見解であり、所属する会社の公式見解ではありません。**

**<span class="blue">仕事をしながら、考えること</span>**

**<span class="red">tabelog & cena are not HTML5!</span>**

**<span class="yellow">HTML5、どこから使う？</span>**

**<span class="yellow">HTML5</span> は 2012/12/17 に W3C勧告候補**


## ウェブの進化
<a href="http://evolutionofweb.appspot.com/" target="_blank">![ウェブの進化](images/evoweb.png)</a>

<aside class="notes">
<a href="http://www.dotcominfoway.com/blog/dot-com-infoway-releases-html5-infographic" target="_blank">Dot Com Infoway Releases HTML5 Infographic</a>
<a href="http://www.wix.com/flash/infographic/the-history-of-html5.html" target="_blank">The History of HTML5</a>
</aside>


**たくさんある**


## <span class="yellow">HTML5</span>、どこから使う？

* キャンペーンサイト
* 新しく立ち上げるサイト
* スマートフォン向けサイト


**<span class="green">勧告候補になったし、そろそろ普通に使っていきたい</span>**

**すでに<span class="yellow">HTML5</span>を使っているサイトを <del>ぱくって</del> 参考に<span class="yellow">HTML5</span> を取り入れて行きたい。**

**<span class="blue">いろいろ調べて、考えてみた。</span><br>↑これから話すこと**


**身近な、普通のサイトで使われている <span class="yellow">HTML5</span>**

## <span class="yellow">HTML5</span> Markup
HTML5なマークアップはけっこう見かける。

* <a href="http://www.muji.net/" target="_blank">無印良品</a>
* <a href="http://www.apple.com/" target="_blank">Apple</a>
* <a href="http://www.lawson.co.jp/index.html" target="_blank">LAWSON｜ローソン</a>
* <a href="http://www.united-arrows.co.jp/index.html" target="_blank">UNITED ARROWS LTD.</a>
* <a href="http://www.beams.co.jp/" target="_blank">BEAMSオフィシャルサイト</a>

spec

* <a href="http://www.w3.org/TR/html5/" target="_blank">HTML5</a> / <a href="http://www.w3.org/TR/html51/" target="_blank">HTML 5.1</a>

## <span class="yellow">HTML5</span> Markup
html5shiv 使ったり、createElement したり。

    <!--[if lt IE 9]>
      <script src="dist/html5shiv.js"></script>
    <![endif]-->

    elements = "abbr article aside audio bdi canvas data datalist details figcaption figure footer header hgroup mark meter nav output progress section summary time video".split(" ");
    for(var i=0; i<elements.length; i++){
      document.createElement(elements[i]);
    }

* <a href="samples/markup.html">Sample: HTML5 fall back Sample</a>




## CSS3 Backgrounds,Borders

<span class="green">border-radius</span> とか <span class="green">text-shadow</span> はいろいろなサイトで使われてる。
<a href="http://yoyaku.tabelog.com/" target="_blank">cena</a>でも使ってる。
transform / transition / animation はあまり使わないかも。

* <a href="http://www.w3.org/TR/css3-background/" target="_blank">CSS Backgrounds and Borders Module Level 3</a>
* <a href="http://www.w3.org/TR/css3-transforms/" target="_blank">CSS Transforms</a> / <a href="http://www.w3.org/TR/css3-animations/" target="_blank">CSS Animations</a>

確認は、こんなツールがべんり。

* <a href="http://www.modern.ie/" target="_blank">modern.IE</a>
* <a href="http://www.browserstack.com/" target="_blank">BrowserStack</a>
* <a href="https://browserlab.adobe.com/ja-jp/" target="_blank">Adobe® BrowserLab</a>

## CSS3 Backgrounds,Borders

    border-radius: 10px 10px 10px 10px;
    box-shadow: 10px 10px 10px #aaa;
    text-shadow: 5px 5px 5px #aaa;

* <a href="samples/css3.html" target="_blank">Sample: CSS3 Backgrounds, Borders</a>

関係ないけど CSS Variables が気になる。調べてないけど。

* <a href="http://www.w3.org/TR/css-variables/" target="_blank">Sample: CSS Variables Module Level 1</a>


## MediaQueries
たくさん見かける、見つかる。

* <a href="http://www.w3.org/" target="_blank">World Wide Web Consortium (W3C)</a>
* <a href="http://www.microsoft.com/ja-jp/default.aspx" target="_blank">日本マイクロソフト│Microsoft Japan</a>
* <a href="http://www.nttdata.com/jp/ja/index.html" target="_blank">NTTデータ</a>

bookmarklet とか、いろいろ。

* <a href="http://mediaqueri.es/" target="_blank">Media Queries</a>
* <a href="http://lab.maltewassermann.com/viewport-resizer/" target="_blank">Responsive design testing tool – Viewport Resizer – Device simulation tool</a>
* <a href="http://mattkersley.com/responsive/" target="_blank">Responsive Design Testing</a>


## MediaQueries

    @media screen and (max-width: 479px) {
      .media-test { color: red; }
    }
    @media screen and (min-width: 480px) and (max-width: 1023px) {
      .media-test { color: blue; }
    }
    @media screen and (min-width: 1024px) {
      .media-test { color: green;}
    }

* <a href="samples/mediaqueries.html" target="_blank">Sample: MediaQueries</a>

<a href="http://sadah.github.com" target="_blank">僕のシンプルなサイト</a>でさえ、確認が大変でちょっと泣けた。CSS力が低いせいだけど。

静的なサイトにはいいかも。食べログのようなWebアプリケーションには向かないかも。

<span class="yellow">PCとスマホで利用シーンや必要な機能が異なる。</span>


## WebFonts
普通に使ってるサイトがたくさん。見つけるのはちょっと大変だけど、DevToolsを開くとすぐに分かる。

* <a href="http://www.beams.co.jp/" target="_blank">BEAMSオフィシャルサイト｜ビームス</a>
* <a href="http://www.nttdata.com/jp/ja/index.html" target="_blank">NTTデータ</a>
* <a href="http://webfont.fontplus.jp/" target="_blank">FONTPLUS｜フォントプラス</a>

僕も使ってる。

* <a href="http://sadah.github.com" target="_blank">sadah.github.com</a>
* <a href="http://sadah.github.com/sada-samplecode/FontsCompare/" target="_blank">Google Web Fonts Compare</a>


## WebFonts

    /* using Google Web Fonts */
    @font-face {
      font-family: 'Allerta Stencil';
      src: url(http://themes.googleusercontent.com/static/fonts/allertastencil/v4/CdSZfRtHbQrBohqmzSdDYKqcRvMv63bhrwdN_8Hu8N8.woff) format('woff');
    }

    .webfonts{
      font-family: 'Allerta Stencil', sans-serif;
    }

* <a href="samples/webfonts.html" target="_blank">Sample: WebFonts</a>
* <a href="http://www.atmarkit.co.jp/fwcr/design/tool/webfonts01/01.html" target="_blank">インストールせずに、好きなWeb Fontsを使おう ＠IT</a>

これらの Extension いれるといろいろべんり。

* <a href="https://chrome.google.com/webstore/detail/whatfont/jabopobgcpjmedljpbcaablpmlmfcogm" target="_blank">Chrome - WhatFont</a>
* <a href="https://chrome.google.com/webstore/detail/google-font-previewer-for/engndlnldodigdjamndkplafgmkkencc" target="_blank">Chrome - Google Font Previewer for Chrome</a>


## Canvas
Canvas はGoogleMapsで使われてる。

Thanks komasshu !

あとはプロフィール画像の切り出しとか。見つけられなかったけど。

* <a href="https://maps.google.co.jp/maps?saddr=%E7%A5%9E%E5%A5%88%E5%B7%9D%E7%9C%8C+%E9%8E%8C%E5%80%89%E9%A7%85&daddr=%E5%AE%AE%E5%B4%8E%E7%9C%8C+%E5%AE%AE%E5%B4%8E%E9%A7%85&ie=UTF8&dirflg=t&ttype=now&t=m&z=7&start=0&geocode=FffsGgId719RCCnfc08qwkUYYDEODvuEPjrpxw%3BFS_-5gEdYn7VBymJj9bEXLc4NTHEGuIFnPgASw&brcurrent=3,0x34674e0fd77f192f:0xf54275d47c665244,1" target="_blank">鎌倉から宮崎 / Google Maps</a>
* <a href="http://jp.wsj.com/public/npage/japan-market-data-center.html?mod=WSJJP_topnav_jp_market" target="_blank">マーケットデータ - WSJ日本版</a>

spec

* <a href="http://www.w3.org/TR/2dcontext/" target="_blank">HTML Canvas 2D Context</a>


## Canvas

    var ctx = $("#canvas-area")[0].getContext("2d");
    // x, y, radius, startAngle, endAngle [, anticlockwise ] )
    ctx.arc(200, 100, 50, 0, Math.PI*2, false);
    ctx.stroke();

* <a href="samples/canvas.html" target="_blank">Sample: Canvas</a>

とりあえず、円を描く。


## Canvas + WebFonts

    ctx.fillStyle = "navy";
    ctx.font = "72px 'Cabin Sketch', cursive";
    ctx.fillText("WebFonts", 200 , 50);

* <a href="samples/webfonts_canvas.html" target="_blank">Sample: Canvas + WebFonts</a>

CanvasでWebFontsも使える。
WebFontsは、利用されるときにダウンロードされるので、なにもしないと最初の1回はフォントが適用されない。

WebFont Loader 使いましょう。

* <a href="https://developers.google.com/webfonts/docs/webfont_loader?hl=ja" target="_blank">WebFont Loader - Google Web Fonts</a>


## SVG
思った以上に、いろいろなところで使われていた。

画像、図、グラフの代わりに。ロゴとか、拡大縮小されるところに使いたい。レスポンシブイメージとか。

Thanks Daniel, wks, myakura.

* <a href="http://newsapps.wsj.com/elections2010/#race=senate" target="_blank">Election 2010 - The Wall Street Journal Online</a>
* <a href="http://raphaeljs.com/" target="_blank">Raphaël—JavaScript Library</a>
* <a href="http://www.nytimes.com/" target="_blank">The New York Times</a>
* <a href="http://www.apple.com/jp/" target="_blank">アップル</a>


## SVG
    <svg width="800" height="300">
      <circle cx="150" cy="150" r="100" stroke="blue" fill="white" stroke-width="5"/>
    </svg>

    <img src="image.svg">

* <a href="samples/svg.html" target="_blank">Sample: SVG</a>
* <a href="samples/svg_webfonts.html" target="_blank">Sample: SVG + WebFonts</a>

Raphaël使うと…

* <a href="http://raphaeljs.com/australia.html" target="_blank">Raphaël · Australia</a>
* <a href="http://raphaeljs.com/text-rotation.html" target="_blank">Raphaël · Text Rotation</a>



## History API
上手に使うとすごく便利だと思う。
History API(pjax) はgithubやflickrやfacebookで使われてる。

* <a href="https://github.com/sadah/" target="_blank">sadah github</a>
* <a href="http://www.flickr.com/photos/j7400157/3132470039/in/set-72157611522875239/" target="_blank">IMG_6077 | Flickr - Photo Sharing!</a>
* <a href="http://html5demos.com/history" target="_blank">HTML5 Demo: HTML5 History API</a>


## File API & Drag and Drop
Drag and Drop(& File API) もいろいろ使われてました。

* <a href="https://plus.google.com/photos/instantupload" target="_blank">写真 - Google+</a>


## File API & Drag and Drop

      // jquery
      // var files = e.originalEvent.dataTransfer.files;
      var files = e.dataTransfer.files;
      var fileName = files[0].name;
      var fileSize = files[0].size;

      var reader = new FileReader();
      reader.onload = function() {
        var line = reader.result;
      }
      reader.readAsText(file[0], 'UTF-8');

* <a href="samples/dnd.html" target="_blank">Sample: Drag and Drop</a>


## microdata
身近な microdata。

* <a href="http://www.barackobama.com/" target="_blank">Barack Obama</a>
* <a href="http://schema.org/" target="_blank">Home - schema.org</a>
* <a href="https://www.google.co.jp/search?q=%E3%83%A9%E3%82%B7%E3%82%A8%E3%83%83%E3%83%88" target="_blank">ラシエット - Google 検索</a>
* <a href="http://support.google.com/webmasters/bin/answer.py?hl=ja&answer=176035" target="_blank">microdata について - ウェブマスター ツール</a>
* <a href="http://support.google.com/webmasters/bin/answer.py?hl=ja&answer=173379" target="_blank">リッチ スニペット - レシピ - ウェブマスター ツール</a>
* <a href="http://www.google.com/webmasters/tools/richsnippets" target="_blank">Google Structured Data Testing Tool</a>


## microdata

    <div itemscope itemtype="http://data-vocabulary.org/Person">
      私の名前は<span itemprop="name">ひらい さだあき</span>ですが、
      みんなから「<span itemprop="nickname">さだ</span>」と呼ばれています。
      私のホームページは、
      <a href="http://sadah.github.com" itemprop="url">sadah.github.com</a> です。
      鎌倉に住んでおり、<span itemprop="title">エンジニア</span>として
      <span itemprop="affiliation">カカクコム</span>に勤めています。
    </div>

* <a href="samples/microdata.html" target="_blank">Sample: microdata</a>

こちらを参考に。

* <a href="http://support.google.com/webmasters/bin/answer.py?hl=ja&answer=176035" target="_blank">microdata について - ウェブマスター ツール</a>
* <a href="http://support.google.com/webmasters/bin/answer.py?hl=ja&answer=146646" target="_blank">リッチ スニペット - 人物 - ウェブマスター ツール</a>


## Custom Data Attributes
グラフのデータを入れたり。

* <a href="http://staff.hatenablog.com/" target="_blank">はてなブログ開発ブログ</a>
* <a href="http://www.barackobama.com/" target="_blank">Barack Obama</a>
* <a href="http://www.w3.org/TR/html5/dom.html#embedding-custom-non-visible-data-with-the-data-*-attributes" target="_blank">3.2.3.9 Embedding custom non-visible data with the data-* attributes</a>


## data URL Scheme

画像を埋め込んだり。

* <a href="http://staff.hatenablog.com/" target="_blank">はてなブログ開発ブログ</a>
* <a href="http://www.apple.com/jp/" target="_blank">アップル</a>
* <a href="http://tools.ietf.org/html/rfc2397" target="_blank">RFC 2397 - The "data" URL scheme</a>


## data URL Scheme

    <img src="data:image/jpeg;base64,/9j/4AAQSkZJ ... "

    var strDataURI = document.getElementById("canvas-area").toDataURL("image/png");

細かい画像が多いときには便利。

* <a href="samples/dataurlscheme.html" target="_blank">Sample: data URL Scheme</a>
* <a href="samples/dataurlscheme_canvas.html" target="_blank">Sample: data URL Scheme + Canvas</a>

実用性はないけど、こんなことも。

* <a href="samples/getUserMedia.html" target="_blank">Sample: Video + Canvas + data URL Scheme + FullScreen</a>


## Performance

Navigation Timingとか。

* <a href="http://www.w3.org/TR/navigation-timing/" target="_blank">Navigation Timing</a>

link prefetch とか script defer async とか。

* <a href="http://www.w3.org/TR/html5/links.html#link-type-prefetch" target="_blank">4.12 Links — HTML5</a>
* <a href="http://www.w3.org/TR/html5/scripting-1.html#attr-script-async" target="_blank">4.3 Scripting — HTML5</a>


## Performance
HTML5じゃないけど、HTTP 2.0 とか SPDY とか。

* <a href="http://tools.ietf.org/html/draft-ietf-httpbis-http2-01" target="_blank">draft-ietf-httpbis-http2-01 - Hypertext Transfer Protocol version 2.0</a>
* <a href="http://www.chromium.org/spdy" target="_blank">SPDY - The Chromium Projects</a>
* <a href="http://tools.ietf.org/html/draft-mbelshe-httpbis-spdy-00" target="_blank">draft-mbelshe-httpbis-spdy-00 - SPDY Protocol</a>


## まとめ

フォールバックが面倒なものは、使わないほうが楽かも。勝手にフォールバックされるものはいいかも。

直感的な処理ができるようなところは、使っていくといいのかも。

Drag and Drop や Canvas の画像のトリミングとか。


## まとめ

<span class="yellow">HTML5</span>、いろいろある。

仕様が安定しているもの、そうじゃないもの。

自分のサイトの特性を考えて、効果の高いところから。

メリットの大きいところから。

使えるところから使っていけばいいと思う。


## まとめ

ちょっとずつ使う。

大きなリニューアルがあれば、一気に使ってもいい。

使えそうなものが、ひとつでもあれば幸いです。


**みんながハッピーになる？**


**みんながハッピーになるなら<br><span class="yellow">HTML5</span> で作りたい<br><span class="yellow">HTML5</span> を使いたい**


## The End
### Thank you so mach.
### <span class="yellow">Familiar HTML5</span>

**<a href="http://twitter.com/sada_h" target="_blank">@sada_h</a>**

**<a href="http://bit.ly/h5m2013b2" target="_blank">http://bit.ly/h5m2013b2</a>**
