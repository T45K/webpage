---
title: "作ったもの"
date: 2021-03-25T11:07:17+09:00
draft: false
---

## [GitHubContributionBot](https://github.com/T45K/GHCBotForLambda)

GitHub のコントリビューション（草の生え具合）について Twitter で報告してくれるボット．
0 時になると

- その日のコントリビューション数
- その日までの連続コントリビューション日数（Streak）

を呟いてくれる．

技術的には定時に GitHub のトップページをスクレイピングしてるだけ．

何か[似たようなサービス](https://contributter.potato4d.me/)が出てきて草が生えた．
サービスとして公開しておくべきだった 🤔

## [CLIONE](https://github.com/T45K/CLIONE)

<img src="/img/logo.png" width="20%">

類似コードの修正漏れを教えてくれるボット．
GitHub Apps を用いて設計されていて，PR の作成ごとに勝手に通知を飛ばしてくれる．

論文は[こちら](https://sdl.ist.osaka-u.ac.jp/pman/pman3.cgi?D=675)

## [NIL](https://github.com/kusumotolab/NIL)

類似コード検出ツール．

既存のツールでは検出が難しかった「コピペされた後に大量の変更が行われた類似コード」を検出できるように設計されている．
また，N-gram と転置索引を組み合わせることで高速な検出が可能となっている．

論文は[こちら](https://sdl.ist.osaka-u.ac.jp/pman/pman3.cgi?D=669)

## [Bitbucket-Server-Code-Insights-plugin](https://github.com/T45K/Bitbucket-Server-Code-Insights-plugin)

BitBucket Server で、PR の diff 上にコメントのようなものを表示できる機能、Code Insights を利用するための Jenkins プラグイン。
Checkstyle や SpotBugs といった静的解析ツールや、SonarQube と行ったシステムの実行結果を PR の diff 上に表示できる。

## [Back-Merge-plugin](https://github.com/T45K/Back-Merge-plugin)

main ブランチが更新された時に、main ブランチから各派生ブランチ向けへの PR を作成する Jenkins プラグイン。

## [Approve-LGTM-plugin](https://github.com/T45K/Approve-LGTM-plugin)

Bitbucket Server 上で PR を承認した際に、LGTM な画像を投稿する Jenkins プラグイン。

## [Coverage Uploader for Bitbucket Server](https://github.com/T45K/IntelliJ-Bitbucket-Server-Coverage-Upload-plugin)

Bitbucket Server の PR の画面上にカバレッジ情報を表示するために、
IntelliJ IDEA 上で計測したカバレッジ情報を Bitbucket Server に送信する IntteliJ プラグイン。

<iframe width="384px" height="319px" src="https://plugins.jetbrains.com/embeddable/card/20589"></iframe>
