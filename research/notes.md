# 研究ノート：配置補空間の多重スケールKE幾何
2026-11-20 / v1.0

## 大域pGHへの残された障害
Part III原稿のcurrent theoremは、quantified wall-compatible systemを仮定した場合のpGH収束である。actual metricで必要なのはcentral、lateral、ordinary/tie overlapを横断するtracked lifting（template lifts、kernel connectors、zero-cost directionsの有効な商）が同時に (o(R)) で制御されること。局所conifoldでの定性的収束と、全層の一様global liftingは異なる。

## 定量化・Jacobi・scattering
Canonical tube modelのphase-zero operatorの形式計算では、\(\mathcal L_\\mathcal H=-\Delta_\\mathcal H\) に対し \(B_\square=\sqrt{33/4+3\\mathcal L_\\mathcal H}-3/2\) と連続スペクトルの閾値 (\(\sqrt{33}-3\)/2) が現れる。global metricにintrinsicな係数と解釈するにはcentralとlateralのPoisson–Calderón matchingが必要。boundary traceの任意な右逆による減算はcanonical threshold scalarを与えない（(ker T) 上のfunctionalが一般に消えない）。

## Family-uniformity
固定realizationでのlocalizationと (M_{0,5}) の族全体での一様性を区別する。\(\\lambda\\mu\(\\lambda-1\)\(\\mu-1\)\(\\lambda-\\mu\)\to0\) では残差曲線が退化し、conifold depth、plumbing depth、scattering depthを連動して扱う必要がある。

## 今後の独立問題
- 一般matroidに対するcanonical metrized Bergman quotientとresolution-independentなsingular face masses。
- 一般 ((n,m)) のresidual period mapのmatroid criterion、secondary WP inner completion、branch separation。
- 相対極限とweight/filterを使うGH収束の定量化、実際のquasi-coordinate estimates。

## 文献と検証の注意
Part IはRochon–Zhangのrecursive facewise estimatesを入力とする。Part IIIのTian–Yau/Yau・Datar–Fu–Song・Dumas–Wolfの利用は一次資料の仮定精査が必要であり、移行操作だけでは検証したことにならない。既存Libraryの `Multiscale_KE_Arrangements_post_trilogy_research_note_ja_v21.tex` から現在有効な問題を整理したが、Part III v1.2で解決した固定nodeの定性的localizationを再び未解決と記してはいけない。
