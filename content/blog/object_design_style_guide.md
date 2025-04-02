---
title: "「オブジェクト設計スタイルガイド」読了"
date: 2025-04-02T23:28:26+09:00
draft: false
tags: ["技術書"]
---

オグジェクト設計スタイルガイドを読みました。

<table border="0" cellpadding="0" cellspacing="0"><tr><td><div style="border:1px solid #95a5a6;border-radius:.75rem;background-color:#FFFFFF;width:504px;margin:0px;padding:5px;text-align:center;overflow:hidden;"><table><tr><td style="width:240px"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17511069%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><img src="https://hbb.afl.rakuten.co.jp/hgb/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?me_id=1213310&item_id=20965144&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fbook%2Fcabinet%2F0331%2F9784814400331_1_3.jpg%3F_ex%3D240x240&s=240x240&t=picttext" border="0" style="margin:2px" alt="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]" title="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]"></a></td><td style="vertical-align:top;width:248px;display: block;"><p style="font-size:12px;line-height:1.4em;text-align:left;margin:0px;padding:2px 6px;word-wrap:break-word"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17511069%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;">オブジェクト設計スタイルガイド [ Matthias Noback ]</a><br><span >価格：3,520円（税込、送料無料)</span> <span style="color:#BBB">(2025/4/2時点)</span></p><div style="margin:10px;"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17511069%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><img src="https://static.affiliate.rakuten.co.jp/makelink/rl.svg" style="float:left;max-height:27px;width:auto;margin-top:0" ></a><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17511069%2F%3Fscid%3Daf_pc_bbtn&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ==" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><div style="float:right;width:41%;height:27px;background-color:#bf0000;color:#fff!important;font-size:12px;font-weight:500;line-height:27px;margin-left:1px;padding: 0 12px;border-radius:16px;cursor:pointer;text-align:center;"> 楽天で購入 </div></a></div></td></tr></table></div><br><p style="color:#000000;font-size:12px;line-height:1.4em;margin:5px;word-wrap:break-word"></p></td></tr></table>

オブジェクト指向言語を用いたアプリケーション開発（主にサーバーサイド）の設計について本でした。

オブジェクトの種類を大きくサービスとその他に分け、サービスをシングルトンでイミュータブルにする、
その他では不変状態を表明するなど実践的な設計方針が書かれていて良いなと感じました。

また、この手の本には珍しく、イベントリスナーを用いたイベントディスパッチについての記述が豊富にあり、
勉強になりました。

最後の方にはDDDとの用語についての説明があるので、そのままDDDに繋げることができそうだなと感じました。

処理失敗時に例外を投げるなど、一部個人の嗜好にそぐわない部分もありましたが、
全体的に現代的なサーバーサイド設計の参考になり、良いなと思いました。
