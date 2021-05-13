---
title: Other
weight: 14
bookToc: false
---

{{<hint info>}}
その他の設定項目はここにおいてあります。
{{</hint>}}

{{< figure src="/image/ash/setother001.png" class="center" >}}


### Preview extra setting

#### Interval
テンプレート取得画面で表示される映像のインターバル。

### Replay size[1-1000]
テンプレート取得画面において、リプレイ用に映像を保持する枚数を指定。\
Intervalを大きく、Replay sizeを大きくすることで、より長時間映像を保持することができます。\
シビアな場面を取りたい場合はインターバルを小さくすることでほしい映像が残る可能性が高くなります。

### リサイズメソッド
取り込んだ映像をリサイズする際のリサイズ方式を指定。



### LiveSplitをコントロールする前にチェックを行う
このチェックを有効にすると、LiveSplitにSplit等の信号を送る前に起動チェック、現在のLiveSplitの状態、現在のSegmentを取得し、正常に信号を送ることができたかの確認を行います。
このチェックを無効にした場合、画像がマッチングしてからLiveSplitが信号を認識するまでの時間が約0.03秒少なくなります。
