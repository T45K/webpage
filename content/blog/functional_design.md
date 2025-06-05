---
title: "「関数型デザイン」読了"
date: 2025-06-05T23:30:27+09:00
draft: false
tags: ["技術書"]
---

ボブおじの新作「関数型デザイン」を読んだ。

<table border="0" cellpadding="0" cellspacing="0"><tr><td><div style="border:1px solid #95a5a6;border-radius:.75rem;background-color:#FFFFFF;width:504px;margin:0px;padding:5px;text-align:center;overflow:hidden;"><table><tr><td style="width:240px"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17854386%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><img src="https://hbb.afl.rakuten.co.jp/hgb/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?me_id=1213310&item_id=21249977&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fbook%2Fcabinet%2F1151%2F9784048931151_1_4.jpg%3F_ex%3D240x240&s=240x240&t=picttext" border="0" style="margin:2px" alt="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]" title="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]"></a></td><td style="vertical-align:top;width:248px;display: block;"><p style="font-size:12px;line-height:1.4em;text-align:left;margin:0px;padding:2px 6px;word-wrap:break-word"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17854386%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;">関数型デザイン 原則、パターン、実践 [ Robert　C．Martin ]</a><br><span >価格：4,180円（税込、送料無料)</span> <span style="color:#BBB">(2025/6/5時点)</span></p><div style="margin:10px;"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17854386%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><img src="https://static.affiliate.rakuten.co.jp/makelink/rl.svg" style="float:left;max-height:27px;width:auto;margin-top:0" ></a><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17854386%2F%3Fscid%3Daf_pc_bbtn&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ==" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><div style="float:right;width:41%;height:27px;background-color:#bf0000;color:#fff!important;font-size:12px;font-weight:500;line-height:27px;margin-left:1px;padding: 0 12px;border-radius:16px;cursor:pointer;text-align:center;"> 楽天で購入 </div></a></div></td></tr></table></div><br><p style="color:#000000;font-size:12px;line-height:1.4em;margin:5px;word-wrap:break-word"></p></td></tr></table>

ボブおじはClean Architectureなどから分かる通り、これまでオブジェクト指向言語をメインにしていたが、
今回はこれまでオブジェクト指向言語で紹介していた原則、テクニックをClojureに置き換えた場合にどうなるか、について説明している。
これを通して、関数型言語が実用に耐えうるものだと説いていた。

いくつかのトピックに対して、OOPでFPでのコード例を並べて、FPでうまくいく例、いかない例を紹介しており参考になった。

また、OOPの基本原則であるSOLIDが、FPだとどうなるかを説明していて、根底にあるソフトウェア設計の理解に繋がった。

悲しいことにClojureの文法をあまり理解できなかったためコード例をほとんど読み飛ばすことになってしまった。
Clojureをどこかで入門したいなと思った。
