<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · ja · no clinical/professional/rights approval -->

# 左室心筋重量・左室形態

[条件・出典・許諾](https://elucenia.org/ja/tools/massa-ventricular-esquerda)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 心室中隔（拡張期）

`siv`

cm · 範囲: 0.4–3

### 左室拡張末期径

`ddve`

cm · 範囲: 2–9

### 後壁（拡張期）

`ppve`

cm · 範囲: 0.4–3

### 体重

`peso`

kg · 範囲: 20–300

### 身長

`altura`

cm · 範囲: 100–230

### 性別

`sexo`

- `F` — 女性
- `M` — 男性

## 方法の版

Devereux 1986補正三乗式0.8×1.04+0.6；ASE/EACVI 2015；Mosteller体表面積補正

## 記載された計算式

左室心筋重量（g） = 0.8 × 1.04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0.6 (測定単位cm；SIV：心室中隔厚、DDVE：左室拡張末期内径、PP：左室後壁厚；すべて拡張末期に測定)

重量係数 = 重量 ÷ 体表面積 (Mosteller)

相対壁厚 = 2 × PP ÷ DDVE

## 限界・対象集団

ASE/EACVI 2015の線形法では、拡張末期に心室長軸に垂直な方向で測定したセンチメートル単位の寸法が必要です。適切な形状を前提としており、非対称性肥大、拡張、局所的な壁厚の違いによって不正確になることがあります。測定値を3乗するため、わずかな画像取得の誤差でも心筋重量が変化します。線形法、2D法、異なる体格補正法の基準値を自動的に相互置換してはなりません。

## 参考文献

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
