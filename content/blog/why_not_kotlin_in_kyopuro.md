---
title: "競プロでKotlinを使わない理由"
date: 2022-07-04T22:38:27+09:00
draft: false
tags: ["技術"]
---

仕事や趣味でソースコードを書く時は Kotlin を使っているが、競プロでは Java を使っている。

ちょくちょく Kotlin に移行することを考えるのだが、その度に色々な理由で断念するので、その理由を書き出してみる。

## ビット演算子がない

多分これが一番大きい。

競プロではビット演算をする場面がたびたびある（ビット全探索とか）。

Java では`<<`や`|`などが使えるが、Kotlin では`lhs`や`or`などの中置関数を使う必要があり、可読性が大きく下がる。

## 配列宣言が面倒臭い

競プロの性質上、配列に対してプリミティブな操作を行う場面が多くあるため、配列宣言はなるべく簡潔に済ませたい。

Java では`int[]`のように宣言できるが、Kotlin では`Array<Int>`のように宣言する必要がある。

また、一次元配列では特に問題ないのだが、多次元配列（競プロでは三次元配列を書く場面が多々ある）になると Kotlin の記法は特に面倒になる。

## null チェックが厳しい

仕事で使う分にはありがたいが、競プロのような使い捨てるコードに対しては意義が薄れる感じがする。

とくに、Map のキーの存在が確定している場合でも何らかのエスケープが発生する。

`!!`演算子で無理やり非 null 型に変換することもできるが、個人の信条からあまり使いたくない（`!!`演算子の利用に慣れたくない）。

## トラディショナル for が使えない

Kotlin の for 文はイミュータブルな変数を使った記法なので、トリッキーでアドホックな for 文を書きにくいという欠点がある。
例えば、添字の`i`を条件によって更新したりしなかったりする場合など。

## 暗黙の型変換がない

`int`と`long`で足し算したり、`char`同士の引き算の結果を`int`にしたりするのが面倒臭い。
