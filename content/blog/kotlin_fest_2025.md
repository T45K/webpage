---
title: "Kotlin Fest 2025に参加・登壇した話"
date: 2025-11-02T20:28:45+09:00
draft: false
tags: [ "技術" ]
---

今年もKotlin Festに参加してきました。

## Kotlin Fest

https://2025.kotlinfest.dev/

「Kotlinを愛でる」というキーワードで開催されているカンファレンスです。
国内のKotlinに関するイベントとしては最大級で、今年は24個のセッションで、400人ほどの参加者が集まりました。

今年も去年に引き続き、運良くプロポーザルが採択されたので、登壇もしてきました
（今年もスクリプトを完成させないまま発表に臨むはめになりました）。

## 登壇内容

[「デッドコード消せてますか？ - 構文解析とGradleプラグイン開発で始めるコードベース改善」](https://2025.kotlinfest.dev/timetable/1719031800_a/)
というタイトルで発表しました。

<iframe class="speakerdeck-iframe" frameborder="0" src="https://speakerdeck.com/player/2368e468ac424569b53f38045ac19e7f" title="デッドコード消せてますか？構文解析とGradleプラグイン開発で始めるコードベース改善" allowfullscreen="true" style="border: 0px; background: padding-box padding-box rgba(0, 0, 0, 0.1); margin: 0px; padding: 0px; border-radius: 6px; box-shadow: rgba(0, 0, 0, 0.2) 0px 5px 40px; width: 100%; height: auto; aspect-ratio: 560 / 315;" data-ratio="1.7777777777777777"></iframe>

フィーチャーフラグを用いた開発において、リリース後に不要になったフィーチャーフラグと、
それによって発生するデッドコードを削除する作業が必要になります。

今回は、そういったコードを自動で消すために、構文解析と自作のGradleプラグインを利用する方法を紹介しました。

発表後は、共感しやすい内容だったからか、ask the speakerセッションに多くの方に来ていただけました。

多くの方がフィーチャーフラグ管理に悩んでいるんだなと実感でき、[公開しているOSS](https://github.com/T45K/feature-flag-remover)
を使ってもらえると嬉しいかも...と思ったりしました。

ちなみに、もう一つ[ネタっぽいプロポーザル](https://fortee.jp/kotlin-fest-2025/proposal/bb11a90a-1b93-4814-8e32-3f1e5f7779ce)
も投げていたのですが、それは不採択となってしまいました。

## 聴講したセッション

### [【招待セッション】Kotlinを支える技術：言語設計と縁の下の力持ち](https://2025.kotlinfest.dev/timetable/1719021000_a/)

JetBrainsでAnalysis APIの開発をしているヤンさんのセッションでした。

今後追加されるであろうKotlinの言語仕様や、それに関しての社内やコミュニティにおける議論を紹介してもえらえました。

Kotlinに追加される機能がいかに慎重に議論されており、それがユーザーにいかに貢献しているかがわかった良いセッションでした。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">companion fun いいね <a href="https://twitter.com/hashtag/KotlinFest?src=hash&amp;ref_src=twsrc%5Etfw">#KotlinFest</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1984452666257522898?ref_src=twsrc%5Etfw">November 1, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### [Kotlin Compiler Pluginで実現するCustom String Interpolation](https://2025.kotlinfest.dev/timetable/1719023400_b/)

String Interpolationについて詳しく知らなかったのですが、文字列補間のことを指すそうです。

今回は、他の言語でサポートされているString InterpolationをKotlinでどのように実現するかについて、
SQLのプレースホルダーを題材にして解説してもらえました。

クエリに直接変数を埋め込んだ形の文字列が、プレースホルダと変数の形に分離する手法は、なるほどな、と感じました。

```kotlin
// 例
val userId = 1
val original = "select * from users where id = $userId" // これが

val converted = "select * from users where id = ?"
val vars = listOf(userId) // こんな感じになる
```

Kotlin Compiler PluginによるIR変換は本当に強力な方法なので、どこかで触ってみたいな、と思いました。
String Interpolationという題材も共感しやすくて良かったです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">SQL injectionを気にせんくて良くなって嬉しい <a href="https://twitter.com/hashtag/KotlinFest?src=hash&amp;ref_src=twsrc%5Etfw">#KotlinFest</a> <a href="https://twitter.com/hashtag/fun?src=hash&amp;ref_src=twsrc%5Etfw">#fun</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1984484436940111963?ref_src=twsrc%5Etfw">November 1, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### [ネストしたdata classの面倒な更新にさようなら！Lensを作って理解するArrowのOpticsの世界](https://2025.kotlinfest.dev/timetable/1719033600_c/)

Arrowは普段から使っているのですが、Opticsについては知っておらず、data classの更新というトピックも共感できたので聴講しました。

OpticsはImmutableなデータ構造を効率的に更新できるデータ表現であり、Lensだけでなくいくつかの種類が提供されており、それぞれが継承関係にあるそうです。
https://arrow-kt.io/learn/immutable-data/

セッション参加が途中からになってしまったため、十分に理解できなかったのですが、Opticsという概念を知れたのは良かったです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Optics学ばねば <a href="https://twitter.com/hashtag/KotlinFest?src=hash&amp;ref_src=twsrc%5Etfw">#KotlinFest</a> <a href="https://twitter.com/hashtag/let?src=hash&amp;ref_src=twsrc%5Etfw">#let</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1984513387003593175?ref_src=twsrc%5Etfw">November 1, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### [文字列操作の達人になる ~ Kotlinの文字列の便利な世界 ~](https://2025.kotlinfest.dev/timetable/1719035400_a/)

Kotlinの文字列操作において便利なAPIを紹介するセッションでした。

`@Language`をつけることで、文字列リテラルにシンタックスハイライトを適用できることや、正規表現の便利APIは知らなかったので、勉強になりました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">まだまだ知らないメソッドがありそうだ <a href="https://twitter.com/hashtag/KotlinFest?src=hash&amp;ref_src=twsrc%5Etfw">#KotlinFest</a> <a href="https://twitter.com/hashtag/var?src=hash&amp;ref_src=twsrc%5Etfw">#var</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1984526066845909191?ref_src=twsrc%5Etfw">November 1, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### [Rewind & Replay: Kotlin 2.2 が変えるCoroutine デバッグ最前線](https://2025.kotlinfest.dev/timetable/1719039000_b/)

Coroutineのデバッグで使えるツールやライブラリを紹介するセッションでした。

ローカル変数をキャプチャできなかった理由として、Coroutineの原理上、suspendしたタイミングで使わないローカル変数をContinuation中から消しているという説明を聞いて、納得しました。

知らなかった手法がいくつかあったため、いくつか試してみたいなと思いました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">なるほど<br>使わないローカル変数を継続から捨てるんや<a href="https://twitter.com/hashtag/KotlinFest?src=hash&amp;ref_src=twsrc%5Etfw">#KotlinFest</a> <a href="https://twitter.com/hashtag/fun?src=hash&amp;ref_src=twsrc%5Etfw">#fun</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1984530814806454662?ref_src=twsrc%5Etfw">November 1, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### [KoogではじめるAIエージェント開発](https://2025.kotlinfest.dev/timetable/1719040800_a/)

Koogの存在を知っていたのですが、何ができるかを知らなかったので聴講しました。

AIエージェントの仕組みやKoogで実装する方法、他のフレームワークとの比較やテストまで網羅的に含まれており満足度が高かったです。

このセッションを見て、ぜひKoogを試してアドカレで何か書きたいなと思いました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">アドカレ近いし、Koogで遊んで何か書こうかな<a href="https://twitter.com/hashtag/KotlinFest?src=hash&amp;ref_src=twsrc%5Etfw">#KotlinFest</a> <a href="https://twitter.com/hashtag/var?src=hash&amp;ref_src=twsrc%5Etfw">#var</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1984544420507926543?ref_src=twsrc%5Etfw">November 1, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### [Kotlin 2.2が切り拓く：コンテキストパラメータで書く関数型DSLと新しい依存管理のかたち](https://2025.kotlinfest.dev/timetable/1719042600_c/)

コンテキストパラメータを活用して、DIとは別の形で依存管理を行う方法を考察する、という内容だったと思います。

時間が短かったので例を完全に理解できなかったと思いますが、興味深いセッションでした。

コンテキストパラメータは僕も気になっているのですが、意外とできることが多そうな雰囲気なので、GAが楽しみです。

また、Spring Bootの利用において、IaCコンテナ非依存になることでNativeに移行しやすくなるというのは予想外の着眼点で、なるほどなと思いました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Nativeに移行しやすいのは良さそう<br>Ktorでもいけるのでは<br> <a href="https://twitter.com/hashtag/KotlinFest?src=hash&amp;ref_src=twsrc%5Etfw">#KotlinFest</a> <a href="https://twitter.com/hashtag/let?src=hash&amp;ref_src=twsrc%5Etfw">#let</a></p>&mdash; task (@getupmax) <a href="https://twitter.com/getupmax/status/1984555490685436356?ref_src=twsrc%5Etfw">November 1, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

その他、今回は参加できなかったのですが、Kotlin言語仕様やCoroutineの内部実装のセッションなどに興味があるので、
発表資料が公開されたら確認したいと思います。

## 最後に

Kotlin Festに参加した全ての方にお礼申し上げます。
特に、カンファレンス運営の方々は、今年も準備が大変だっただろうと察します。

来年も開催されると嬉しいです。
