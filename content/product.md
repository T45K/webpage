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

## [Contributor](https://github.com/T45K/Contributor)

CLIONE をスタンドアロンとして設計しなおしたツール．
手軽に PR を投げたい時に便利．
