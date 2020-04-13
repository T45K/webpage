---
title: "パナソニックプログラミングコンテスト2020の解説"
date: 2020-03-14T22:56:44+09:00
draft: false
---

4完．[コード](https://github.com/t45k/kyopuro/tree/master/AtCoder/others/pana20)

## A - Kth Term
実装するだけ．
Javaの場合は問題文をコピペして`final int[] array = {1, 1, ...};`と宣言すると早い．

## B - Bishop
ここに一番時間を吸われた．<br>
問題例を見ると最終的に`(h * w + 1) / 2`でいけそうに見えるが，hまたはwが1の時角は一切移動できなくなることに気付けるかがポイント．

## C - Sqrt Inequality
ここにも時間を吸われた．<br>
`Math#sqrt`を使うと解けそうな気がするが，精度の都合上間違いになることがある．
今回は式変換を行うと`4ab < a^2 + b^2 + c^2 + 2ab - 2bc - 2ca`に持っていけるので，そこに代入するだけ．
あるいは`BigDecimal`を使っても大丈夫らしい．

## D - String Equivalence
偶然通った問題．<br>
左側から文字を決めていくが，使える文字は自身より左に存在している一番大きい文字 + 1までしか使えないことに注意．

## E - Three Substrings
全探索の問題．[ここ](https://www.hamayanhamayan.com/entry/2020/03/15/002311)を参考にした．<br>
Editorialではa，b，cの順番を考慮せずにやる方法を紹介しているが，考えることが増えるので素直に全ての順列で場合分けした方が良さそう．
以降，(aの先頭) ≦ (bの先頭) ≦ (cの先頭)の場合を考える．<br>
まず，a中のどの箇所がbと被っているかを全探索して，配列か何かに記録する(O(n^2))．これをaとc，bとcに対してもやる．
コードだとこんな感じ．
```java
private static boolean[] init(final int length, final String a, final String b) {// 配列の初期化
    final boolean[] array = new boolean[length]; // lengthは十分大きい値
    Arrays.fill(array, true);
    for (int i = 0; i < a.length(); i++) {
        for (int j = 0; j < b.length() && i + j < a.length(); j++) {
            // 文字列aの位置i以降がbと被っているかの確認
            if (!match(a.charAt(i + j), b.charAt(j))) { 
                array[i] = false;
                break;
            }
        }
    }
    return array;
}
private static boolean match(final char a, final char b) {
    return a == '?' || b == '?' || a == b;
}
```
それぞれの結果をab，ac，bcとする．<br>
これらの配列の
- `ab[i] == true`となる`i`
- `bc[j] == true`となる`j`

に対して`ac[i + j] == true`となれば，その配置は矛盾がないことになる．
図だとこんな感じ

{{< figure src="/img/kyopuro/pana2020_e.png" height="50%" width="50%" >}}

iの探索範囲は0からaの長さ，jの探索範囲はbの長さかiからaの終端までの長さの長い方になる．<br>
あとは長さの最小値を出すだけ．
