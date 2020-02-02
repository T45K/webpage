---
title: "ICSE2020の面白そうな論文をピックアップしてみた"
date: 2020-02-01T18:59:35+09:00
draft: false
---

ICSEはInternational Conference of Software Engineeringの略です．
ソフトウェア工学の国際学会の中で一番ランクが高い会議です．
会議自体は5月に行われるのですが，再録された論文一覧とアブストが公開されているので，
面白そうな論文をピックアップしてみました．

## Is Rust Used Safely by Software Developers?
RustはC，C++に取って代わることを目指した，メモリ安全性や実行速度を売りにしているプログラミング言語です．
その特徴から，ソフトウェア開発界隈からの注目度が高まりつつあります．<br>
この論文では，メモリ安全性を放棄する代わりにパフォーマンスを上げる **Unsafe Rust** についての調査を行っています．

## Securing UnSafe Rust Programs with XRust
これもRustの論文です．<br>
XRustという，Unsafe Rustを通常のRustに移行する手法を提案しています．<br>
ICSEに(Unsafe)Rustに関する論文が2本採択されていることから，ソフトウェア開発におけるRustの盛り上がり具合が分かります．

## Big Code != Big Vocabulary: Open-Vocabulary Models for Source code
キャッチーなタイトルだったのでピックアップしてみました．<br>
変数名などのユーザー定義の識別子があるため，ソースコードは自然言語に比べて，大規模になるとコーパスが巨大になってしまいます．
この論文では，コーパスがスケールするように，新しい言語モデルを提案しています．

## DLFix: Context-based Code Transformation Learning for Automated Program Repair
最近のソフトウェア工学の大きなトピックの一つであるAPRの論文．<br>
機械学習ベースのAPRは過去のバグ修正の学習に制限があるのに対して，DLFixでは学習のレイヤを2層に分けることでうまくこの制限を回避したらしいです．

## A Cost-efficient Approach to Building in Continuous Integration
CIの論文．<br>
CIのコストはビルドを回している時間だけかかってしまい，かつ，CIの目的はバグを発見することなので，
多くのバグを発見するビルドをなるべく早い段階で回す手法を提案しています．

## Here We Go Again: Why Is It Difficult for Developers to Learn Another Programming Language?
ある言語を習得したプログラマが他の言語を習得する際の難易度に関する調査を行った研究．

### 終わりに
以上です．
会議全体としては，機械学習とFuzzing周りの論文が多い印象です．
おそらく今年もICSE勉強会が実施されると思うので，楽しみにしてます．

論文一覧は[ここ](https://conf.researchr.org/track/icse-2020/icse-2020-papers#event-overview)から見れます．
