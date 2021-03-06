---
weight: 110
bookFlatSection: true
title: "FAQ"
---

# FAQ

## ★★★★★トラブル★★★★★

## 正常に自動ラップが機能しない

### リセットの自動監視が動かない
- [設定-Monitoring]({{< ref "/docs/06eachsettingitem/001monitoring.md" >}})の```自動化の対象```で、Resetにチェックが入っているかご確認ください。
- リセットの監視は2枚目のテンプレート監視が始まったときに始まります。監視開始直後/リセット直後は動きません。

### 想定外の場面で一致率が高くなり、誤判定が発生する
ユニーク（特異的）ではない、もしくは平坦な画像をテンプレート画像としている場合、目的の場面以外でも一致率が高くなり、誤判定を起こすことがあります。ラップを取る場所を変更したり、監視メソッドを変更したりしてみてください。

### 以前は正常に動いていたのに、一致率が低く、一致判定が発生しないようになった
ゲーム画面を映しているソフトのサイズや解像度、アスペクト比、また仮想webカメラのリサイズメソッド等が変わっていないか確認してみてください。

### 一致判定が発生しても、ラップタイマーなどが反応しない
ラップタイマーがGlobal Hotkeyに対応していない場合、Focusの設定を行う必要があります。
また、ラップタイマーが完全にアクティブになる前にキー送信をしたり、キー押下時間が短すぎてラップタイマーが入力を認識していない可能性があります。キー送信までの時間、キー押下時間を長めに設定してみて下さい。

### 監視途中に不定期にエラーが発生する
仮想webカメラと本ソフトウェアとの相性が悪いと接続が不安定になることがあるようです。仮想カメラデバイスを変更してみて下さい。

## ASHがボケて表示される。また、その時仮想webカメラと接続ができない。
Windows10の場合、実行ファイルのプロパティ→互換性を開き、「高いDPIスケールの動作を上書き」にチェック、実行元を「アプリケーション」にして下さい。

Windows8の場合、

Windows7の場合、

## (ビデオ再生において)再生、シークがワンテンポ遅れる。
PCスペックや動画ファイルのエンコード設定によっては、再生やシーク等が遅れることがあります。動画の解像度、フレームレート、エンコード設定を調整してみてください。

{{<hint info>}}
例\
解像度：320x180~640x360、フレームレート：30\
keyint = 動画のフレームレート\
※Aviutl 拡張x264出力の場合、[フレーム]タブ、GOP関連設定の"キーフレーム間隔の上限" = 動画のフレームレート
{{</hint>}}

## 監視途中に不定期にエラーが発生する。
仮想カメラデバイスと本ソフトウェアとの相性が悪いと、接続が不安定になることがあるようです。仮想カメラデバイスを変更してみて下さい。

## PC負荷が大きすぎてまともに動作しない。
監視間隔、更新間隔が小さい、解像度、フレームレートが大きいほど負荷が大きくなります。これらの値を調整してみて下さい。

また、Reset、Load Removerを併用すると負荷が大きくなります。どうしても必要、というわけでない場合、これらの監視を行わない（Splitのみ）ようにすると、負荷の軽減に繋がります。

さらに、監視中にコンパクトモードにする（[たたむ]を押す）と、一部処理をスキップするため処理が軽くなります。

## 以前は使用できたのに使えなくなってしまった。
以下の理由が考えられます。
1. 画面キャプチャの対象としていたウィンドウのサイズ等が変わった。

   ソフトウェアのアップデートで表示にズレが発生することもあるようです。



## ★★★★★改良★★★★★

