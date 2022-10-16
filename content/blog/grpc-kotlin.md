---
title: "gRPC-JavaのチュートリアルをKotlinでやってみる"
date: 2022-08-22T21:51:41+09:00
draft: true
---

マイクロサービスアーキテクチャに関する記事を漁っていると、gRPC というメッセージング方法があることを知ったので、チュートリアルをやってみた。

## gRPC とは

まず RPC とは Remote Procedure Call の略で、読んで字の如く遠隔のプログラムの手続きを呼び出す手法らしい。
Google が策定した RPC なので gRPC。
