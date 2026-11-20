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

## 一次資料を直接確認した入力と数値規格化
Rochon–Zhang, *Asymptotics of complete Kähler metrics of finite volume on quasiprojective manifolds* (Adv. Math. 231 (2012)) の Theorem 5.1 は **SNC pair** の全 strata にわたる共通指数 \(\nu>0\) の \(x_i^\nu C^\infty_{\rm fc}\) 漸近を扱う。Theorem 7.4 の full polyhomogeneous expansion は **smooth divisor** を仮定する。一般 SNC へ Theorem 7.4 をそのまま適用しない。主原稿の `rem:RZ-primary-scope` に一次資料との対応を統合した。この照合はTheorem 5.1からmetric-IRFAへの翻訳や大域的path-lifting全体の独立証明ではない。

一般位置の五直線の規格化では \(L=2H\), \((L^2)=4\) なので、主稿のface mass formulaを代入すると
\[
\mathfrak m_\varnothing=8\pi^2,\qquad
\mathfrak m_{\{i\}}=8\pi^2,\qquad
\mathfrak m_{\{i,j\}}=4\pi^2.
\]
四点除去球面のcurvature \(-1\) metricの面積は \(4\pi\)（Gauss–Bonnet）で、normal circleの \(2\pi\) と合わせて一階面mass \(8\pi^2\) を得る。この計算は記法と体積係数の検算であって、漸近公式の解析的証明ではない。

## 入力の監査
Part Iのrecursive uniformity（Rochon–Zhang）とPart IIIのTian–Yau/Yau、Datar–Fu–Song、Dumas–Wolf等は一次資料と適用条件の比較が必要。post-trilogy v2.2の本文をpapers/research-directions.texへ保持した。最新版ではactual localization自体も(H_loc)へ分離されており、旧稿の証明済みという状態を維持しない。
