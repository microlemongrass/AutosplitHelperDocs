---
title: Virtual Capture
weight: 2
bookToc: false
---

# Virtual Capture

{{<hint info>}}
キャプチャ方式をVirtualにした場合、この項目を設定する必要があります。
{{</hint>}}

{{< figure src="/image/ash/setvirtualcapture001.png" class="center" >}}

使用例（OBSStudio x OBS-VirtualCamを例にとって）
{{< youtube 6uRJ-58HcMg >}}


①仮想デバイスの設定（使用する仮想デバイス、入力解像度、フレームレート）、②実際に監視などの処理をするときの解像度（表示解像度）をそれぞれ指定してください。表示解像度に[Cropped]を指定すると、クロップ後の映像をそのまま使用します。

動作確認済みのデバイス
- SCFH DSF
- SCFF DSF
- XSplit Broadcaster
- NDC(XP)
- アマレコTV V3.1、V4
- OBS Studio(OBS VirtualCamインストール時)\
※OBS26.0.0.rc1で実装されたネイティブの仮想webカメラは動作しません。

\
仮想デバイスの設定を済ませた後に[接続]を押せば仮想デバイスと接続されます。

{{<hint info>}}
- 入力解像度、表示解像度が小さいほどPCへの負荷が少なくなります。
- 入力と出力の解像度を一致させた場合が最もパフォーマンスが良くなるので、可能な場合はそのように設定してください。\
※入力解像度、出力解像度はsavedata/Base.iniファイル内の該当箇所を編集することで追加できます。
{{</hint>}}

{{<hint warning>}}
仮想カメラとの接続が不安定となった場合は一旦切断し、再接続を試みてください。
{{</hint>}}

{{<hint danger>}}
他デバイスへの接続後にSCFF DSFに接続するとフリーズする現象を確認しています。変更前にプロファイルを保存してASHの再起動等をするようにして下さい。
{{</hint>}}

　
### クロップ
　キャプチャした映像に黒帯など消したい部分がある場合、[クロップ]にチェックを入れて[設定]からクロップ範囲の指定をすることで、不要な部分を除去することができます。

{{< figure src="/image/ash/setvirtualcapture002.png" class="center" >}}

プレビュー画面からクロップ領域を指定することができます。

{{<hint info>}}
キャプチャ/クロップ後にゲーム画面のみが映っている状態が望ましいです。
- ソフトウェアのアップデートなどでゲーム画面の表示位置やサイズが変わってしまった場合、クロップの調整で対応することが出来る。
- 他の人にプロファイルデータを送る際、同じキャプチャ状態を作り出しやすい。
{{</hint>}}

{{<hint warning>}}
※クロップ領域が仮想カメラの範囲外を参照しようとすると「Bad cropping!」と表示されます。クロップ領域が範囲内となるようにして下さい。
{{</hint>}}