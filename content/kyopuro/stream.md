---
title: "JavaでN個の入力を良い感じにリストにする方法"
date: 2021-04-18T18:05:46+09:00
draft: false
---

これが多分ベスト
```java
Stream.generate(scanner::nextInt)
  .limit(N)
  .collect(Collectors.toList());
```

配列にしたいときは
```java
Stream.generate(scanner::nextInt)
  .limit(N)
  .mapToInt(Integer::intValue)
  .toArray();
```
