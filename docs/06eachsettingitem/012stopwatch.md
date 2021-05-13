---
title: Stopwatch
weight: 12
bookToc: false
---

# Stopwatch
画像画像画像

{{<hint info>}}
ストップウォッチに関する項目です。表の「Comment」列がこの項目に関与します。
{{</hint>}}

## Stopwatch

{{< figure src="/image/ash/setstopwatch001.png" class="center" >}}

フォント名、フォントサイズ、表示形式を設定して[**表示**]を押すと、ストップウォッチウィンドウが表示されます。

ストップウォッチは、表の「Comment」列に入力されている文字列に```「_start_」「_stop_」```が含まれている場合、ストップウォッチを開始、停止します。

表示例：
{{< figure src="/image/ash/setstopwatch002.png" class="center" >}}


## Table
セグメントタイム等各種情報を記録します。

### 使用方法
- Tableウィンドウを開いたら表を右クリックし、「Initialize」を選択してください。\
　このとき、メイン画面の表の「Comment」列に```_start_```、```_stop_```が記述されていなければなりません。

- Tableウィンドウを開いたまま監視を行うと自動的にタイムを記録します。

### BestSplitTimeについて
　これはLiveSplitのBestSplitTimeとは機能が異なります。\
　表の「Comment」列に```_bst_```が含まれている場合、その行までの最短記録を保存します。
  
  以下のような場合、xxには区間1~3のベストタイム、yyには区間4~6のベストタイムが保存されます。

  Comment | ... | BST
----------|-----|---------
  1       | ... | --
  2       | ... | --
  3_bst_  | ... | xx
  4       | ... | --
  5       | ... | --
  6_bst_  | ... | yy
  7       | ... | --