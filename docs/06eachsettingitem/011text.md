---
title: Text
weight: 11
bookToc: false
---

# Text

{{<hint info>}}
テキスト表示に関する項目です。\
テンプレート画像をキャプチャする際、テキストフォルダ以下に対応するテキストファイルが生成されます。事前にそのファイルに記述しておき、テキストウィンドウを表示しておくことで、画像マッチング毎にそのテキストを閲覧することができます。
{{</hint>}}

{{< figure src="/image/ash/settext001.png" class="center" >}}

{{< figure src="/image/ash/settext002.png" class="center" >}}

テキストファイルの形式はrtfのため、文字のフォント、色、ハイライト、画像表示などが行なえます。

　
### スクリプトを使用する
テキストフォルダ内にスクリプトファイルを配置することで、それらのスクリプトを実行することができます。ファイル名は[n].[拡張子]　(例：1.uws)とリネームして配置し、[**スクリプトを使用**]にチェックを入れてください。

**対応スクリプト**
- VBScript(CScript)
- JScript(WScript)
- AutoItX
- UWSC




{{<hint warning>}}
スクリプトを使用する場合であっても、rtfファイルは削除しないでください。
{{</hint>}}
