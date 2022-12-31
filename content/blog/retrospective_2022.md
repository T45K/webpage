---
title: "2022年の振り返り"
date: 2022-12-31T09:39:23+09:00
draft: false
---

2022年を振り返る。

## 総評

楽しく仕事ができた。
特に、チーム内でやっていることをチーム外に啓蒙するという活動をしてて、それが評価されたという感じ。

先輩、後輩とのつながりも増えて申し分ない1年間だった。

## 仕事

### 1月 -- 3月

- 主にインターンのメンターとJenkinsおじさんをやってた
  - インターンのメンターは、インターンの子が超絶優秀だったのであまりやることがなかった。
    - 逆に色々教えてもらえて良かった。
    - リリースが間に合わなかったのはシンプルに申し訳なかった。
  - JenkinsはIaaS環境に載せてたJenkinsがあまりにも使い物にならなくなってきたので、k8s環境に載せ替えた。
  <blockquote class="twitter-tweet"><p lang="ja" dir="ltr">- 一つのコンテナに全ての機能を突っ込む<br>- コンテナにcredentialを突っ込む<br><br>みたいなカスみたいなアンチパターンから、<br><br>- 機能ごとにコンテナを分割して、ポートで通信する<br>- credentialはコンテナに持たせず、都度Jenkins側から渡す<br><br>に改善できて良い</p>&mdash; task@血圧・尿酸 (@getupmax) <a href="https://twitter.com/getupmax/status/1496688678546321409?ref_src=twsrc%5Etfw">February 24, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

  - 個人的には大満足なマイグレーション。
  - ちなみにこの話をこの1年間擦り続けてる。

### 4月 -- 6月

- この辺りから、趣味で他のチームのコードレビューにも参加するようになる。
  - 啓蒙活動。
  - 特に汚いソースコードに関してコメントすることが多かった。この辺は個人の思想の押し付けになってたかも。
  - 最終的に綺麗なソースコードを書こうとしても設計が崩壊してると終わりなことに気づいた。

### 7月 -- 9月

- Java8環境に耐えきれなくなり、Java17にアプデするプロジェクトを勝手に立ち上げる。
  - PDMに話通して、スケジュール設定 → 実装 → テスト → リリースまでを自分でできたのは良い経験だったなと。
  - 終わった後にLT会でナレッジを共有したり、他のチームのJava17導入に噛んだりできて良かったなと。
  - チームに自動E2Eテストを書く文化が根付いていたので、マイグレーションがかなりやりやすかった。ありがたい。

- 夏のインターンのメンター
  - 1週間
  - 自分も夏のインターンからの採用だったので、その辺も踏まえて会社に貢献できたらという気持ち。
  - どっちかというと1日の終わりのレビューがメインのお仕事でした。
  - 最終的に優勝してた。すごい。
  - その辺の話はこちら<br>
    https://commerce-engineer.rakuten.careers/entry/workstyle/0025
  - 以降、インターン経験者かつメンターで優勝みたいな経歴もあって新卒向けイベントみたいなのに呼ばれる機会が増えた。

### 10月 -- 12月
- 複数チームにまたがって改善活動をやっていこうぜ的なチームが発足。
  -「自チームの改善」 + 「コードレビューを通した他チームへの貢献」みたいなところに目をつけれられて、そのチームに放り込まれる。
  - 他のチームの人と議論したり、自分がやった改善活動の横展みたいなことをしてた。

- これまでやってきたことが認められて昇格。
  - 特別昇格扱いだとかなんとか。
  - ほとんど残業せずに昇格できたので、コスパ良かったなぁと。

- 他のチームに2ヶ月弱移籍。
  - 他のチームのサービスも知っておいた方が良いという上の方針で。
  - 100%英語での仕事だったので大変だった。

## 人間関係

- 出社が増えて、社内の人たちと仲良くなった。
  - 特に、会社が晩御飯の提供を始めてから、三食同期と一緒に食べる機会が多かったのが良かった。
  - 後輩が入ってきた。今のところ仲良くしてもらってる。
    - ライブとかクラブとかに引きずり回されたそれはそれで良かった。
  - 年が近い先輩と飲みに行く機会が何回かあって楽しかった。
  - 他のチームのよく関わるメンバーと仲良くなれたのも大きかった。英語でのコミュニケーションも慣れてきたかも。

- 社外の人間関係は特に変わらず。

## プログラミング

- JenkinsプラグインとかIntelliJプラグインみたいな、仕事で使えるプラグインを趣味の一環で使ってた。
  <iframe width="384px" height="319px" src="https://plugins.jetbrains.com/embeddable/card/20589"></iframe>
- 「Scala関数型デザイン&プログラミング」をやった。いわゆる純粋関数型プログラミングの思考をふんわりと理解した。
  <table border="0" cellpadding="0" cellspacing="0"><tr><td><div style="border:1px solid #95a5a6;border-radius:.75rem;background-color:#FFFFFF;width:504px;margin:0px;padding:5px;text-align:center;overflow:hidden;"><table><tr><td style="width:240px"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F13176662%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><img src="https://hbb.afl.rakuten.co.jp/hgb/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?me_id=1213310&item_id=17383699&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fbook%2Fcabinet%2F7768%2F9784844337768.jpg%3F_ex%3D240x240&s=240x240&t=picttext" border="0" style="margin:2px" alt="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]" title="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]"></a></td><td style="vertical-align:top;width:248px;"><p style="font-size:12px;line-height:1.4em;text-align:left;margin:0px;padding:2px 6px;word-wrap:break-word"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F13176662%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  >Scala関数型デザイン＆プログラミング Scalazコントリビューターによる関数型徹底ガイ （impress　top　gear） [ ポール・キウザーノ ]</a><br><span >価格：4290円（税込、送料無料)</span> <span style="color:#BBB">(2022/12/31時点)</span></p><div style="margin:10px;"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F13176662%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><img src="https://static.affiliate.rakuten.co.jp/makelink/rl.svg" style="float:left;max-height:27px;width:auto;margin-top:0"></a><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F13176662%2F%3Fscid%3Daf_pc_bbtn&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ==" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><div style="float:right;width:41%;height:27px;background-color:#bf0000;color:#fff!important;font-size:12px;font-weight:500;line-height:27px;margin-left:1px;padding: 0 12px;border-radius:16px;cursor:pointer;text-align:center;">楽天で購入</div></a></div></td></tr></table></div><br><p style="color:#000000;font-size:12px;line-height:1.4em;margin:5px;word-wrap:break-word"></p></td></tr></table>
- ISUCONに出た。Javaで頑張ったけどスコアが伸びなかったので、最終的に何もしていないRust実装を提出して終わった。
- その他、Mockitoにバグ報告したり、IntelliJに機能修正パッチ投げたり。

## 飲酒

- 去年と比較して、外に飲みに行く機会が増えた印象。
  - 先輩に誘ってもらったり。
  - 会社で晩御飯を食べるようになってからは、その日のメニューが微妙だったら飲みに行ったりしてた。

- 地酒を買う機会が増えた。
  - 特に難波エディオンでは有名な地酒を、阪急百貨店では地方の蔵元が直接売りに来る酒を買ったりしてた。

## 健康

- ついに血圧だけでなく尿酸値も基準値を突破し、無事再検査へ。
- その他はまあぼちぼち。
- ランニングする機会は減ったかも。

## バイク
- 大型二輪の免許を取った。
- 夏休みに遠出する予定だったが、北陸の豪雨で道が無くなったりしてたらしいので断念。
- 11月に出雲大社に参拝。往復600km超を1日で走る。多分人生で一番長い。

## アニメ
- 久々にリアタイでアニメを追うことをしてた。
- パリピ孔明、リコリコ、ぼっち・ざ・ろっく、etc.
- 職場の先輩もアニメ好きで、アニメの話で盛り上がれるのが良い。
- 趣味の話をできる人が身近にいることが重要だなぁと改めて実感した。

## 読書

- 月一くらいのペースで小説、技術書問わず何かしらを読むようにした。
- 今年読んでて一番ためになったのは「現場で役立つシステム設計の原則」かなぁ。
  <table border="0" cellpadding="0" cellspacing="0"><tr><td><div style="border:1px solid #95a5a6;border-radius:.75rem;background-color:#FFFFFF;width:504px;margin:0px;padding:5px;text-align:center;overflow:hidden;"><table><tr><td style="width:240px"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F15017530%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><img src="https://hbb.afl.rakuten.co.jp/hgb/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?me_id=1213310&item_id=18637464&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fbook%2Fcabinet%2F0877%2F9784774190877.jpg%3F_ex%3D240x240&s=240x240&t=picttext" border="0" style="margin:2px" alt="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]" title="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]"></a></td><td style="vertical-align:top;width:248px;"><p style="font-size:12px;line-height:1.4em;text-align:left;margin:0px;padding:2px 6px;word-wrap:break-word"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F15017530%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  >現場で役立つシステム設計の原則 変更を楽で安全にするオブジェクト指向の実践技法 [ 増田亨 ]</a><br><span >価格：3234円（税込、送料無料)</span> <span style="color:#BBB">(2022/12/31時点)</span></p><div style="margin:10px;"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F15017530%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><img src="https://static.affiliate.rakuten.co.jp/makelink/rl.svg" style="float:left;max-height:27px;width:auto;margin-top:0"></a><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F15017530%2F%3Fscid%3Daf_pc_bbtn&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ==" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><div style="float:right;width:41%;height:27px;background-color:#bf0000;color:#fff!important;font-size:12px;font-weight:500;line-height:27px;margin-left:1px;padding: 0 12px;border-radius:16px;cursor:pointer;text-align:center;">楽天で購入</div></a></div></td></tr></table></div><br><p style="color:#000000;font-size:12px;line-height:1.4em;margin:5px;word-wrap:break-word"></p></td></tr></table>
- その他書評は[ブログ](/blog/)に書いてます。

## 音楽

- 年の初めは某動画の影響でRussian Hard Baseとか聴いてた。
  <iframe width="560" height="315" src="https://www.youtube.com/embed/1qzSagjh1ck" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
- 年の終わりは某アニメの影響で八十八ヶ所巡礼を聴いてた。
  - 「攻撃的国民的音楽」とかは比較的キャッチーで良い。
    <iframe width="560" height="315" src="https://www.youtube.com/embed/D90AOhojK3M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## その他

- インスタを始めた。
- スマホキャリアが楽天モバイルになった。
  <blockquote class="twitter-tweet"><p lang="ja" dir="ltr">箕面山 vs 楽天モバイル　<br><br>勝者、楽天モバイル（圏外にならなかったので） <a href="https://t.co/8QedXGkSi7">pic.twitter.com/8QedXGkSi7</a></p>&mdash; task@血圧・尿酸 (@getupmax) <a href="https://twitter.com/getupmax/status/1513049757123448837?ref_src=twsrc%5Etfw">April 10, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
- 5年ぶりにコミケに現地参加した。第100回だったので。
  <blockquote class="twitter-tweet"><p lang="ja" dir="ltr">ビッグサイトへ</p>&mdash; task@血圧・尿酸 (@getupmax) <a href="https://twitter.com/getupmax/status/1558619249534349312?ref_src=twsrc%5Etfw">August 14, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
- JJUGを聴講した。
