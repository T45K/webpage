---
title: "JJUG CCC 2022 Fallに参加した話"
date: 2022-12-03T17:36:13+09:00
draft: false
tags: ["技術"]
---

2022 年 11 月 27 日日曜日に開催された JJUG CCC 2022 Fall に参加しました。

[リンク](https://jjug.doorkeeper.jp/events/143914)

## JJUG

JJUG は"Japan Java User Group"を指します。
日本最大の Java のコミュニティです。
JJUG CCC は毎年 2 回、春と秋に開催されるイベントで、
様々な参加者が Java に関する技術や事例などの紹介を行います。

参加者の中には、普段から Java コミュニティで活躍されていられる方も多くいらっしゃります。

今回僕は聴講側として参加しました。
以下、参加したセッションとそれぞれの感想を書いていきます。

### AWS 環境における Spring Boot アプリケーションの CI/CD を CircleCI で構築した話

株式会社 Red Frasco の篠原さんのセッション。

https://speakerdeck.com/red_frasco/cdwocirclecidegou-zhu-sitahua

現在開発中のサービスで、

- CI/CD に Circle CI を
- 実行環境に AWS を

利用した事例について紹介されていました。

個人的には CI/CD に興味があったためこのセッションに参加しました。

Java (Spring) に関連した内容は少なかったですが、Circle CI で AWS にアプリをデプロイする際に注意すべきこと、おすすめの方法等を紹介されており、今後これらのシステムを使う際には参考になりそうだなと感じました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">path-filteringええな<br>Jenkinsにもないかな</p>&mdash; task@血圧 (@getupmax) <a href="https://twitter.com/getupmax/status/1596672722070667264?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### バーチャルスレッド詳細

Java コミュニティでよく名前を見かけるもちださんのセッションで、
Java 19 でプレビュー版として導入されたバーチャルスレッドについて紹介されていました。

https://github.com/mike-neck/jjug-ccc-2022-fall-web

一つ前に参加したセッションとの時間の兼ね合いの都合上、後半から参加しました。
VOICEROID(?)を用いた発表をされておりすごく印象的でした。

これまでのスレッド効率化の技術（Rx 等）と比較したバーチャルスレッドの利点や利用例の紹介がメインでした。
最初から参加できなかったのが悔やまれました。
一方で、生のスレッドを仕事で使うことは少ないので、どちらかというとフレームワーク作成者やその辺り向けの機能に聞こえました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">VirtualThreadで勝ちですわ</p>&mdash; task@血圧 (@getupmax) <a href="https://twitter.com/getupmax/status/1596675949910626304?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### カード決済基幹システム　レガシーの克服と無停止更改の挑戦

GMO の羽鳥さんのセッション。

https://www.gmo-pg.com/corp/newsroom/news/event/2022/1122.html

金融系システムのパフォーマンス改善のために、DB で行っていた処理を Redis に移行した事例と、
そのプロジェクト中に起きた問題などの紹介をされていました。

そのシステムは、流量制御などの頻繁に更新される処理を RDB 上で行っており、
それによるロックが原因でパフォーマンスの低下が著しかったそうです。
個人的にも、そういったアトミック性が必要な処理を RDB で行うのはよくあるかなと思っており、
初めのうちは良くても、後々大幅な改修が必要になるのは世の常だなぁと感じました。

また、システムを止めることはできないので、新しいアプリケーションと古いアプリケーションを並行で実行する必要があるのですが、
その間で整合性をどう取るかなどは参考になりました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">こういうマイグレーション系の話、聞く分にはよくある話やなぁで終わってまうんやけど、やってる側からしたら語り尽くせんほどの苦労があったんやろうなぁっていうのが伺い知れる</p>&mdash; task@血圧 (@getupmax) <a href="https://twitter.com/getupmax/status/1596688985161576448?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### LINE NEWS における Java 移行の 5 年間の歩みとこれから

LINE の森藤さんによるセッション。

https://speakerdeck.com/line_developers/five-years-of-java-migration-and-the-future-of-line-news

LINE NEWS を Perl から Java に移行された話をされました。

"カード決済基幹システム　レガシーの克服と無停止更改の挑戦"のセッションと同時開催だったため 2 窓しました。
そのため、あまり集中して話を聞けなかったのですが、
言語移行の際に仕様を守りながら移行する大変さと、実際にリリースしてから負荷的な問題が露見した辺りが印象的でした。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/jjug_ccc?src=hash&amp;ref_src=twsrc%5Etfw">#jjug_ccc</a> <a href="https://twitter.com/hashtag/jjug_ccc_a?src=hash&amp;ref_src=twsrc%5Etfw">#jjug_ccc_a</a><br>実際に負荷をかけてみてからじゃないと気づけない問題は怖い</p>&mdash; task@血圧 (@getupmax) <a href="https://twitter.com/getupmax/status/1596690221873082369?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### コンテナ環境での Java 技術の進化

富士通の数村さんのセッション。

https://www.youtube.com/watch?v=nJJHSwywei0

コンテナ環境に対する Java と Linux の話をされていました。

Java の場合、古い Java 8 ランタイムでは、
コンテナ上ではリソースの情報が正しく取得できない問題などがあるようです。
これを聞いて、Java のバージョンを更新するのが必要だと一層強く思いました。

後半では Linux のコンテナ環境への対応を話されていましたが、悲しいことにあまり理解できませんでした。
動画は YouTube で公開されているため、時間があれば確認したいです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">マジでcontainerizationってゲームチェンジャーやったんやなって</p>&mdash; task@血圧 (@getupmax) <a href="https://twitter.com/getupmax/status/1596712953792761857?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### Java 開発ツールのあれこれ ～便利そうなツールを色々集めてみた～

マトリックスの大城さんのセッション。

https://parasoft.techmatrix.jp/jjug_ccc_2022_fall

こういう便利ツール系の話は大好きなので、喜んで参加しました。

便利なツールの紹介は知っているものもあったり知らないものもあったりしたのですが、
最後に、現在は更新が止まっているツールの紹介があったのが印象的でした。
このようなツールでも様々な事情で開発が止まることがあることを考えると、
仕事で使っている OSS に普段から興味を持ち、開発が止まっても自分たちで保守することを考えるべきなのかなぁと思いました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/jjug_ccc_d?src=hash&amp;ref_src=twsrc%5Etfw">#jjug_ccc_d</a> <br>悲しい</p>&mdash; task@血圧 (@getupmax) <a href="https://twitter.com/getupmax/status/1596731653753253888?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### 5 年ぶりのメジャーアップデート! Spring Framework 6 & Spring Boot 3

槙さんのセッション。

https://ik.am/entries/715

業務で利用しているので、Spring Framework のメジャーアップデートは大きな関心がありました。

1. Observability
2. Java Interface Client
3. Problem Details
4. AOT & Native

の四つの話題を提供されていましたが、1 つ目の Observability の話は一切理解できませんでした（おそらく監視に関する話）...

Java Interface Client は Interface を定義するだけで HTTP クライアントを利用できる昨日で、
API 呼び出しに関するボイラープレートを大幅に減らせそうだなと感じました。

Problem Details は、API 呼び出し失敗の際のレスポンスボディを良い感じに書けるビルダーに関する機能だったと思います。
そもそも、エラー時のレスポンスボディは RFC で定義されているらしいです（知らなかった）。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/jjug_ccc_b?src=hash&amp;ref_src=twsrc%5Etfw">#jjug_ccc_b</a> <br>エラーレスポンスって仕様決まってるんや</p>&mdash; task@血圧 (@getupmax) <a href="https://twitter.com/getupmax/status/1596751143924686848?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### Red Hat Application Foundations から学ぶアーキテクチャー入門

Red Hat の瀬戸さんのセッション。

https://speakerdeck.com/megascus/red-hat-application-fundationskaraxue-buakitekutiyaru-men

マイクロサービスにおける Red Hat（と Java EE）の活用方法のお話でした。
Red Hat 製品にも Java EE にも疎いのであまり理解できなかったです。
そもそも大規模な開発にも疎いというのもありそうですが。

### Maven Puzzlers

海外の方の英語のセッション。

https://www.javasummitil.com/events/maven-puzzlers/

Maven のビルドステップや依存関係の話でした。
発表者が 2 人おられ、掛け合いながら発表されていたのが印象的でした。

英語のセッションなのと、朝からずっと発表を聞いていたのもあって、集中して聞けませんでした（残念）。
これも動画が公開されているので、後ほど確認したいと思います。

## 全体的な感想

他の会社の方々がどのように Java を使っていて、どんな問題にぶつかったのかなどの話が聞けて良かったです。
いつか、発表者側として参加してみたいと思いました。
