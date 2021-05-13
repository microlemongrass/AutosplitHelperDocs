---
title: ASHにおける画像認識
weight: 2
bookToc: false
---

# AutoSplit Helperにおける画像認識

このソフトは、主にOpenCVSharp（OpenCVの.NET用ラッパー）を使用して画像認識を行っています。  
  
OpenCV(Sharp)には画像処理に関する多くの機能があり、このソフトではその中から2枚の画像を比較するために使われる機能を使用して画像認識を行っています。

### 使用可能な画像認識方法  
  
1. テンプレートマッチング
2. ヒストグラム
3. dHash
4. L2Norm
5. AKAZE
6. 色情報(RGB)を直接比較

各方式の説明については[各監視方式の特徴]({{< ref "/docs/10tips/007monitoringmethod/_index.md" >}})を参照してください。
   
