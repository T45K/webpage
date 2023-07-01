---
title: "「データ指向プログラミング」読了"
date: 2023-07-01T19:17:51+09:00
draft: false
tags: ["技術書"]
---

データ指向プログラミングを読んだ。

本書では、データ指向プログラミングと名付けられた、イミュータブルかつ汎用的なデータ構造で表現されたデータと
参照透過かつジェネリックな関数を使ったプログラミング方法を紹介している。

イミュータブルなデータと参照透過なメソッドを使ったプログラミングは普段から実践しており、
それらを使って柔軟なシステムを構築する方法を紹介している本書にはとても興味があった。
が、内容としてはかなりがっかりした。

本書では、データを表現するためにクラスではなくマップを使うことを前提において話が進んでいく。
つまり

```kotlin
data class Hoge(fuga: Int, piyo: String)

val hoge = Hoge(0, "")
```

を

```kotlin
val hoge = mapOf(
    "fuga" to 0,
    "piyo" to "",
)
```

で書こうという内容だった。
この方法は確かに柔軟になるかもしれないが、静的型付けによる安全性を完全に無視しており、かなりがっかりした。

書籍内でもこのことについて触れられていて、以下のように紹介されていた。

|       | OOP | DOP  |
|:-:    |:-:  |:-:   |
| 安全性 | 高い | 低い |
| 柔軟性 | 低い | 高い |
| 汎用性 | 低い | 高い |

これは各要素を"高い"、"低い"のboolで表現しているDOPが良さそうに見えるだけで、
点数を付けるとDOPの安全性が-5000億くらいでトータだとOOPの方が良さそうだなと感じた
（また、表では触れられていないが、フィールドアクセス時に保管が効かないので、コーディング中のストレスがとんでもないことになりそう）。

その他の感想:

\+ JSON Schema便利そう<br>
\+ データの（デ）シリアライズが簡単なので、REPLが使いやすいのは良い<br>
\+ 汎用的な関数を作るという考え方は良さそう

\- 複雑なJSON Schemaを書こうとすると辛そう。OOPならSpecificationパターンとか使える<br>
\- 色んなところでJSON Schema Validationが挟まりそう<br>
\- ポリモーフィズムで、実装忘れを静的に検知できないのが辛い

<table border="0" cellpadding="0" cellspacing="0"><tr><td><div style="border:1px solid #95a5a6;border-radius:.75rem;background-color:#FFFFFF;width:504px;margin:0px;padding:5px;text-align:center;overflow:hidden;"><table><tr><td style="width:240px"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17434107%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><img src="https://hbb.afl.rakuten.co.jp/hgb/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?me_id=1213310&item_id=20896748&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fbook%2Fcabinet%2F9797%2F9784798179797_1_33.jpg%3F_ex%3D240x240&s=240x240&t=picttext" border="0" style="margin:2px" alt="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]" title="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]"></a></td><td style="vertical-align:top;width:248px;"><p style="font-size:12px;line-height:1.4em;text-align:left;margin:0px;padding:2px 6px;word-wrap:break-word"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17434107%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  >データ指向プログラミング [ Yehonathan Sharvit ]</a><br><span >価格：3,960円（税込、送料無料)</span> <span style="color:#BBB">(2023/7/1時点)</span></p><div style="margin:10px;"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17434107%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><img src="https://static.affiliate.rakuten.co.jp/makelink/rl.svg" style="float:left;max-height:27px;width:auto;margin-top:0"></a><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17434107%2F%3Fscid%3Daf_pc_bbtn&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ==" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"  ><div style="float:right;width:41%;height:27px;background-color:#bf0000;color:#fff!important;font-size:12px;font-weight:500;line-height:27px;margin-left:1px;padding: 0 12px;border-radius:16px;cursor:pointer;text-align:center;">楽天で購入</div></a></div></td></tr></table></div><br><p style="color:#000000;font-size:12px;line-height:1.4em;margin:5px;word-wrap:break-word"></p></td></tr></table>
