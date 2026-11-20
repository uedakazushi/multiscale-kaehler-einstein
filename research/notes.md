# 研究ノート：多重スケールKE（配置補空間）
更新：2026-11-20 / v1.1

## 現行稿の仮定（2026-08-31統合稿を回収）
Part IIの一般WP completionはcontrolled parallel push-off付き。Part IIIのactual localization・pGHは(H_loc)+(H_anc)付き。旧草稿の強い記述より現行原稿とsource-audit.mdを優先する。

## Actual global pGHの障害
Part IIIの条件付きpGH theoremでは、全central/lateral/ordinary/tie wall layersでtemplate lifts・kernel connectors・zero-cost quotient directionsが整合するtracked liftingを仮定する。actual KE metricでこの誤差を一様 \(o(R)\) に抑える部分は未証明。fixed nodeのqualitative local localizationとは別問題である。

## Jacobiとscattering
Canonical tube modelのphase-zero normal operatorで現れる形式的な正の分枝は
\[
B_\square=\sqrt{\tfrac{33}{4}+3\mathcal L_{\mathcal H}}-\tfrac32,
\quad \mathcal L_{\mathcal H}=-\Delta_{\mathcal H}.
\]
連続スペクトル閾値は \((\sqrt{33}-3)/2\) と計算される。Global geometryのcanonical coefficientを得るにはcentral/lateral Poisson–Calderón matchingが必要。Boundary tracesの任意の右逆による補正だけではcanonical scalarは定義できない。

## Family-uniformityとgeneral matroid
\(M_{0,5}\) の判別式 \(\lambda\mu(\lambda-1)(\mu-1)(\lambda-\mu)\to0\) でresidual plumbing scaleが出現する。Fixed-realization localizationとfamily-uniform theoremを混同しない。一般matroidのmetrized Bergman quotient、singular face masses、secondary WP branchesも独立した重要課題。

## 入力の監査
Part Iのrecursive uniformity（Rochon–Zhang）とPart IIIのTian–Yau/Yau、Datar–Fu–Song、Dumas–Wolf等は一次資料と適用条件の比較が必要。post-trilogy v2.2の本文をpapers/research-directions.texへ保持した。最新版ではactual localization自体も(H_loc)へ分離されており、旧稿の証明済みという状態を維持しない。
