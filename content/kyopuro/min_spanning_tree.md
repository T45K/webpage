---
title: 最小全域木メモ
date: 2020-02-29T22:37:36+09:00
draft: false
---

最小全域木という概念を知ったのでメモ．

## 最小全域木とは
*無向グラフが与えられた時に，その部分グラフで任意の2頂点を連結にする様な木を全域木(Spanningu Tree)と言います．辺にコストがある場合に，使われる辺のコストの和を最小にする全域木を最小全域木(MST : Minimum Spanning Tree)と言います．*（蟻本より）<br>
つまり，グラフが連結であることを保ったまま，コストの大きい辺を間引いてできたグラフを指します．連結であり，かつ辺のコストの和が最小なので，グラフは木となります．<br>
[ABC065-D](https://atcoder.jp/contests/abc065/tasks/arc076_b)がこの問題に該当します．

## 解き方
有名なアルゴリズムとして，クラスカル法とプリム法があります．
今回はプリム法を紹介します．<br>
プリム法は至って単純で，各辺をコスト順にソートし，その辺が繋ぐノードが連結でなければその辺を採用，そうでなければ不採用としMSTを作ります．
ノード同士が連結であるかどうかは，Union-Find Treeを用いて確認します．

```java
// edges は Edge(int label1, int label2, long cost) のリスト
edges.sort(Comparator.comparingLong(o -> o.cost));
final UnionFindTree unionFindTree = new UnionFindTree(n); // 要素数nのUnion-Find Treeを構築
long sum = 0;
for (final Edge edge : edges) {
    if (!unionFindTree.isSame(edge.label1, edge.label2)) {
        unionFindTree.unit(edge.label1, edge.label2);
        sum += edge.cost;
    }
}
```

辺のソートに一番計算量を食われます．
