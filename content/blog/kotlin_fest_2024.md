---
title: "Kotlin Fest 2024に参加・登壇した話"
date: 2024-06-23T22:54:46+09:00
draft: false
tags: [ "技術" ]
---

2024年6月22日に開催されたKotlin Fest 2024に参加・登壇してきました。

## Kotlin Fest

https://www.kotlinfest.dev/

Kotlin Festは「Kotlinを愛でる」をビジョンに開催されるカンファレンスです。  
今回は4回目の開催であり、5年ぶりのオフライン開催になりました。  
100以上のプロポーザルがあったことから、国内での注目度が伺えます。

## 登壇内容

「withContextってスレッド切り替え以外にも使えるって知ってた？」というタイトルで登壇しました。

https://fortee.jp/kotlin-fest-2024/proposal/d3105065-ee4e-4a7b-be92-3aae10ab6c01

CoroutineContextとwithContextを活用することで、Kotlinでコンテキスト変数を扱う方法や、
実際の利用例について紹介しました。

業務で思いつきでやったことが、こうやって登壇機会にまで結びついて良かったな、という感想です。

「知らなかった」「勉強になった」などの感想をいただけ、励みになりました。

一方で、自身の登壇の仕方には反省すべき点がいくつかあったなと思っています。

一番はタイムマネージメントが全然できておらず、最終的に時間が足りなくなってしまったことです。

次回このような機会があれば、資料作成を早めに終わらせ、発表練習に時間を割きたいです。

## セッション内容

今回様々なセッションを聴講しましたので、それぞれについて軽く感想を書きたいと思います。

### KotlinConf 2024 を後から256倍楽しむためのヒント

JetBrainsの堀岡さんの招待セッションです。

少し前に開催されたKotlin Confのサマリや、そもそもどうやって海外カンファレンスを楽しむか、
要約するかについて紹介していただきました。

Kotlin Confはビデオが提供されていて、全ては見れていないのですが、
タイトル一覧を紹介していただき、中には興味深いものがあったので、
あとで確認しようと思いました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Server-Side Kotlin Meetupもよろしくお願いします！ <a href="https://twitter.com/hashtag/kotlinfest?src=hash&amp;ref_src=twsrc%5Etfw">#kotlinfest</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1804336555613659642?ref_src=twsrc%5Etfw">June 22, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### Kotlinで愉しむクリエイティブコーディング

畠山さんのセッションです。

クリエイティブコーディングについて何も知らなかったのですが、
コーディングで作曲や絵を描いたりする行為だそうです。

今回は、Kotlinで書かれたOPENRNDRというライブラリを使ってのクリエイティブコーディングを
紹介いただけました。

コードに書いた通りに、一定の規則を持って物体が移動することで面白い絵や動画が完成していき、
とても興味深かったです。

視覚的なフィードバックをすぐに得られるので、確かに初心者向けのコーディングにも良いなと思いました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">君だけのノイズ関数を作ろう！ <a href="https://twitter.com/hashtag/kotlinfest?src=hash&amp;ref_src=twsrc%5Etfw">#kotlinfest</a> <a href="https://twitter.com/hashtag/A?src=hash&amp;ref_src=twsrc%5Etfw">#A</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1804344495565344777?ref_src=twsrc%5Etfw">June 22, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### 2024年版 Kotlin サーバーサイドプログラミング実践開発

「Kotlin サーバーサイドプログラミング実践開発」の著者である竹端さんのセッションです。

著書が書かれた時点と現在を比較し、現在の流行の構成のサーバーサイドKotlin構成を考察するという内容です。

フレームワークにKtor、DIにKoin、DBアクセスにjOOQ、テストフレームワークにKotestという結論でした。

Ktor、Koinは面白そうと思いつつ、Spring Bootと違って個人が管理することが増えそうなので、
難易度は増すかもな...という感想でした。

発表中でサーバーサイドKotlinを盛り上げたい、という気持ちが伝わったのはとても良かったです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">&gt; サーバーサイドの選択肢として、Kotlinが一番人気という状況ではない<br><br>ので、我々で盛り上げねば、かな？<br> <a href="https://twitter.com/hashtag/kotlinfest?src=hash&amp;ref_src=twsrc%5Etfw">#kotlinfest</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1804358391105458464?ref_src=twsrc%5Etfw">June 22, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### KotlinのLinterまなびなおし2024

にゃふんたさんのセッションです。

KotlinのLinterとしてktlint、detekt、konsistそれぞれの特徴や利用例を紹介いただきました。

自身のプロジェクトリードの経験から、Linterの選定理由などを聞けたのが面白かったです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Konsist、確かに1モジュールに全てをぶち込む場合は良さそう <a href="https://twitter.com/hashtag/kotlinfest?src=hash&amp;ref_src=twsrc%5Etfw">#kotlinfest</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1804380793499980219?ref_src=twsrc%5Etfw">June 22, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### もっとKotlinを好きになる！K2時代のKotlin Compiler Plugin開発

kitakkunさんのセッションです。

K2コンパイラのフロントエンドの説明から、コンパイラプラグインの作り方、
実際に作ったプラグインの例について説明していただけました。

コンパイラに14フェーズあり、全てのフェーズで何をしているのかは全く知らなかったので、
とても勉強になりました。

コンパイラプラグインの作り方や周辺の知識は一発で理解できなかったのですが（スライド作ってた）、
あとでスライドを見ながら手を動かしたいな、と思いました。

こういった話は言語特化のカンファレンスでないと出てこないと思うので、面白かったです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">挨拶は大事 <a href="https://twitter.com/hashtag/kotlinfest?src=hash&amp;ref_src=twsrc%5Etfw">#kotlinfest</a> <a href="https://twitter.com/hashtag/a?src=hash&amp;ref_src=twsrc%5Etfw">#a</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1804397190913376576?ref_src=twsrc%5Etfw">June 22, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### Kotlin sealed classを用いた、ユーザーターゲティングDSL（専用言語）と実環境で秒間1,000万評価を行う処理系の事例紹介

松田さんのセッションです。

LINEマンガで使っているターゲティングDSLについて説明していただきました。

「1msは遅い」というのはあんまり考えたことがなかったので、
大規模トラフィックを捌くサービスはすごいなと感じました。

DSLそのものはsealed interfaceとして表現し、
それを評価するロジックと分けていた部分についてはなるほどなと思いました。

また、データ構造の（デ）シリアライズも含めて考慮していた点が実践的に感じました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">データを表現するDSLとそれを評価する関数を分ける。なるほど <a href="https://twitter.com/hashtag/kotlinfest?src=hash&amp;ref_src=twsrc%5Etfw">#kotlinfest</a> <a href="https://twitter.com/hashtag/a?src=hash&amp;ref_src=twsrc%5Etfw">#a</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1804418730811908512?ref_src=twsrc%5Etfw">June 22, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### K2のKotlin IDEプラグインの中を覗いてみよう♪

JetBrainsでKotlinプラグイン開発のリードをしているYanさんのセッションです。

この辺で燃え尽きておりセッション内容を詳しく覚えていないのですが、
K2モードで大きな改善が入ったんだなぁ...という感想でした。

現状Kotest等のIDEプラグインがK2モードに対応していないので僕はまだ使えないのですが...

また、Kotlin Analysis APIについて紹介いただきました。

これはいろんなことに使えそうな雰囲気を感じたので、ぜひ触りたいなと思いました。

（学生時代にJDTでJavaのコード解析してたのを思い出した）

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr"><a href="https://t.co/eFBGEUrZGl">https://t.co/eFBGEUrZGl</a><br>ほんまや、Yanさんの名前がある<a href="https://twitter.com/hashtag/kotlinfest?src=hash&amp;ref_src=twsrc%5Etfw">#kotlinfest</a> <a href="https://twitter.com/hashtag/a?src=hash&amp;ref_src=twsrc%5Etfw">#a</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1804430664374325383?ref_src=twsrc%5Etfw">June 22, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## まとめ

参加者全員がKotlinを好きなのが伝わり、刺激的な1日でした。

運営の方々、登壇された方々、参加された方々にこの場を借りてお礼を申し上げます。

今回は資料作成に時間をかけすぎてしまい、当日も余裕がなく、他の方との交流もあまりできませんでした。  

以降、聴講のみで参加するか、登壇するにしても余裕を持った状態で臨みたいです。

一般参加9,000円は高いので、なんとかならんかなぁという印象です。
