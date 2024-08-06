---
title: "「単体テストの考え方/使い方」読了"
date: 2024-08-06T22:44:20+09:00
draft: false
tags: ["技術書"]
---

単体テストの考え方/使い方を読んだのでその感想。

<table border="0" cellpadding="0" cellspacing="0"><tr><td><div style="border:1px solid #95a5a6;border-radius:.75rem;background-color:#FFFFFF;width:504px;margin:0px;padding:5px;text-align:center;overflow:hidden;"><table><tr><td style="width:240px"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17341285%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><img src="https://hbb.afl.rakuten.co.jp/hgb/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?me_id=1213310&item_id=20818219&pc=https%3A%2F%2Fthumbnail.image.rakuten.co.jp%2F%400_mall%2Fbook%2Fcabinet%2F1723%2F9784839981723_1_5.jpg%3F_ex%3D240x240&s=240x240&t=picttext" border="0" style="margin:2px" alt="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]" title="[商品価格に関しましては、リンクが作成された時点と現時点で情報が変更されている場合がございます。]"></a></td><td style="vertical-align:top;width:248px;display: block;"><p style="font-size:12px;line-height:1.4em;text-align:left;margin:0px;padding:2px 6px;word-wrap:break-word"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17341285%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;">単体テストの考え方/使い方 プロジェクトの持続可能な成長を実現するための戦略 [ Vladimir Khorikov ]</a><br><span >価格：4,488円（税込、送料無料)</span> <span style="color:#BBB">(2024/8/6時点)</span></p><div style="margin:10px;"><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17341285%2F&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ%3D%3D" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><img src="https://static.affiliate.rakuten.co.jp/makelink/rl.svg" style="float:left;max-height:27px;width:auto;margin-top:0" ></a><a href="https://hb.afl.rakuten.co.jp/ichiba/2c4e7c40.9ea290f6.2c4e7c41.04aec2a1/?pc=https%3A%2F%2Fitem.rakuten.co.jp%2Fbook%2F17341285%2F%3Fscid%3Daf_pc_bbtn&link_type=picttext&ut=eyJwYWdlIjoiaXRlbSIsInR5cGUiOiJwaWN0dGV4dCIsInNpemUiOiIyNDB4MjQwIiwibmFtIjoxLCJuYW1wIjoicmlnaHQiLCJjb20iOjEsImNvbXAiOiJkb3duIiwicHJpY2UiOjEsImJvciI6MSwiY29sIjoxLCJiYnRuIjoxLCJwcm9kIjowLCJhbXAiOmZhbHNlfQ==" target="_blank" rel="nofollow sponsored noopener" style="word-wrap:break-word;"><div style="float:right;width:41%;height:27px;background-color:#bf0000;color:#fff!important;font-size:12px;font-weight:500;line-height:27px;margin-left:1px;padding: 0 12px;border-radius:16px;cursor:pointer;text-align:center;"> 楽天で購入 </div></a></div></td></tr></table></div><br><p style="color:#000000;font-size:12px;line-height:1.4em;margin:5px;word-wrap:break-word"></p></td></tr></table>

単体テストを中心に扱った本を読んだのは初めてだったのですが、
単体テストを用いてプロダクションコードを価値あるものにすることについて終始述べられていて良かったです。

単体テストは

- 実行時間が十分に短く
- かつ、テストの実行は隔離されている（=容易に並列実行できる）

ものとして定義されています。

単体テストの実行方式はよくロンドン学派と古典学派に分類され、
後者は積極的にモックを使う、くらいの説明に留められていることが多いのですが、
これに関しても十分な説明がありました。

曰く、古典学派は単体の範囲をテストを実行するプロダクションコードの範囲と定め、
それ以外の部分はモックする、
ロンドン学派は単体の範囲をそれぞれのテストと定め、
DBといったテスト間で共有されうる依存に関してのみモックを使う、という定義をされていました。

ロンドン学派は単体テストでDBを扱うものだと思っていたので、この定義は初めて知りました。

また、テストしやすいアーキテクチャとして、
最初にクエリを行い、最後にコマンドを行う順番を推奨しており、
具体的に関数型アーキテクチャやヘキサゴナルアーキテクチャが紹介されていたのが良かったです。

スタブとモックの違いや、スタブ（クエリ）は検証しない、モック（コマンド）はするなどの説明は腹落ちしました。

本書では一貫して、

- 単体テストはリファクタリングに対する耐性を兼ね備えてなければならない
- そのために、単体テストは振る舞いをテストするべき

を柱にしていたので良かったなと思いました。
