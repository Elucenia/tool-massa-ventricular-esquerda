<!-- ELUCENIA technical documentation · massa-ventricular-esquerda · zh · no clinical/professional/rights approval -->

# 左心室质量与心室几何形态

[条件、来源与许可](https://elucenia.org/zh/tools/massa-ventricular-esquerda)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 室间隔（舒张期）

`siv`

cm · 范围: 0.4–3

### 左心室舒张末期内径

`ddve`

cm · 范围: 2–9

### 后壁（舒张期）

`ppve`

cm · 范围: 0.4–3

### 体重

`peso`

kg · 范围: 20–300

### 身高

`altura`

cm · 范围: 100–230

### 性别

`sexo`

- `F` — 女性
- `M` — 男性

## 方法版本

Devereux 1986校正立方方程0.8×1.04+0.6；ASE/EACVI 2015；Mosteller体表面积标化

## 已记录的公式

左室质量（g） = 0.8 × 1.04 × \[(SIV + DDVE + PP)³ − DDVE³\] + 0.6 (测量单位cm；SIV：室间隔厚度，DDVE：左室舒张末期内径，PP：左室后壁厚度；所有测量均在舒张末期进行)

质量指数 = 质量 ÷ 体表面积 (Mosteller)

相对室壁厚度 = 2 × PP ÷ DDVE

## 限制与适用人群

ASE/EACVI 2015线性法要求在舒张末期测量以厘米为单位的尺寸，测量方向应垂直于心室长轴。该方法依赖适当的几何形态；非对称性肥厚、扩张及局部壁厚差异可能使其不准确。由于测量值要取三次方，微小的采集误差也会改变计算的心肌质量。线性法、二维法和不同体格校正方法的参考值不能自动互换。

## 参考文献

- [Lang RM et al. Recommendations for cardiac chamber quantification by echocardiography in adults (ASE/EACVI). J Am Soc Echocardiogr, 2015.](https://doi.org/10.1016/j.echo.2014.10.003)

- [Devereux RB et al. Echocardiographic assessment of left ventricular hypertrophy: comparison to necropsy findings. Am J Cardiol, 1986.](https://doi.org/10.1016/0002-9149(86)90771-X)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 已记录的结果

以下信息保留该方法对合成示例的输出，不构成独立的临床验证。

### 1

正常几何形态

| 结果详情 | |
| --- | --- |
| 左心室质量 | 182 g |
| 体表面积 | 1.82 m² |
| 相对壁厚 | 0.40 |


### 2

向心性肥厚

| 结果详情 | |
| --- | --- |
| 左心室质量 | 243 g |
| 体表面积 | 1.82 m² |
| 相对壁厚 | 0.57 |

