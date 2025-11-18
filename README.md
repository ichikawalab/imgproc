# 医用画像処理工学演習

## 7.2 値画像処理  
### 純粋なモルフォロジ処理（演習7-3考察）

このリポジトリは、医用画像処理工学演習の一環として **モルフォロジ処理（Erosion / Dilation）** を実装・考察するための教材です。  
対象画像は TIFF/PNG を想定し、構造要素は十字型を使用しています。

---

## 📌 内容
- 原画像の読み込み（OpenCV）
- 十字型構造要素による **Erosion（収縮）**
- 十字型構造要素による **Dilation（膨張）**
- 結果の可視化（Matplotlib）

---

## 🚀 Google Colab で実行
以下のリンクから直接 Colab 上でノートブックを開けます。

👉 [Open in Colab](https://colab.research.google.com/github/ichikawalab/imgproc/blob/main/morphology.ipynb)

---

## 🛠 実行方法（Colab）
1. 上記リンクから Colab を開く  
2. 必要に応じて GitHub 上の画像ファイルを読み込み  
   ```python
   import cv2, numpy as np, urllib.request
   url = "https://raw.githubusercontent.com/ichikawalab/imgproc/main/sample.tiff"
   resp = urllib.request.urlopen(url)
   img_array = np.asarray(bytearray(resp.read()), dtype=np.uint8)
   img = cv2.imdecode(img_array, cv2.IMREAD_GRAYSCALE)
