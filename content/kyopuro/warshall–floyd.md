---
title: "ワーシャルフロイド法メモ"
date: 2020-02-23T01:54:16+09:00
draft: false
---

ワーシャルフロイド法というアルゴリズムを知ったのでメモ．

## ワーシャルフロイド法とは
グラフのある一点から任意の点への最短距離を求めるアルゴリズム．
計算量は点の個数nに対してO(n^3)．
似たようなアルゴリズムに**ダイクストラ法**があるが，あちらはある2点の最短距離をO(n^2)で求めるアルゴリズムである．
計算量が重ためなので，使う場面はかなり限られるが，知っておくと便利だと思った．

## 実装
このアルゴリズムは，動的計画法を用いて最短距離を計算するというアイデアに基づいており，実装がとても簡単．
二次元配列を用いた例がこちら．

```java
public static void main(final String[] args) {
    final int[][] graph = new int[n][n];
    // 初めに無限大の値で各要素を初期化
    for (int i = 0; i < graph.length; i++) {
        Arrays.fill(graph[i], Integer.MAX_VALUE / 2); // Integer.MAX_VALUEでないことに注意
        graph[i][i] = 0;
    }

    // グラフの各辺を与えられた値に変更

    // ここからワーシャルフロイド
    for (int k = 0; k < graph.length; k++) { // 中継する点
        for (int i = 0; i < graph.length; i++) { // 出発する点
            for (int j = 0; j < graph.length; j++) { // 到着する点
                graph[i][j] = Math.min(graph[i][j], graph[i][k] + graph[k][j]); // 中継する点をとった方が短となるか判定
            }
        }
    }
}
```

三重ループを回すだけである．
注意点は，グラフの初期化時に`Integer.MAX_VALUE`を代入しないこと．
`Math.min`のタイミングでオーバーフローするため
