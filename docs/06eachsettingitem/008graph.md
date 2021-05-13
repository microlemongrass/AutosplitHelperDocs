---
title: Graph
weight: 8
bookToc: false
---

# Graph

{{<hint info>}}
区間ごとの成功率の記録に関する項目です。表の「G.C.」「G.R.」「G.V.」列がこの項目に関与します。
{{</hint>}}

{{< figure src="/image/ash/setgraph001.png" class="center" >}}

### 計測開始後の最初のラップ
計測を開始後、最初に取るラップが表の何番目に対応するかを指定してください。試行回数のカウント、LiveSplitへの成功回数追記に影響します。

　
### カウントリセット
試行回数、リセット回数を初期化します。

　
### 表の初期化
表に記録されている成功回数、成功率を初期化します。

　
### LiveSplitのカウント初期化
LiveSplitのSegment nameを初期化します。\
（**LiveSplitのSegment nameにカウント追加**にチェックを入れている場合、LiveSplitのSegment nameに成功数が追記されます。）

　
## 各ラップの到達数について
**LiveSplitのSegment nameにカウント追加**にチェックを入れると、Segment nameの末尾に```[count]```が追記されます。

また、到達数、到達率を簡易的に視覚化したウィンドウを用意しています。どのポイントでリセット回数が嵩んでいるのか等の確認にお使いいただけます。