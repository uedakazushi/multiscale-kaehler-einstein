# 研究ノート：多重スケールKE（配置補空間）
更新：2026-11-22 / v1.5（Part I v1.4）

## 現行稿の仮定（2026-08-31統合稿を回収）
Part IIの一般WP completionはcontrolled parallel push-off付き。Part IIIのactual localization・pGHは(H_loc)+(H_anc)付き。旧草稿の強い記述より現行原稿とsource-audit.mdを優先する。

## 三研究の定理接続と正本

研究・編集・証明監査は共同で進め、各結果の証明は次の正本に保持する。外部確認版は[KE研究資料v1.11・commit e965c78](https://github.com/uedakazushi/kaehler-einstein-degeneration/tree/e965c780ed777d190b880831a556e57d39ab5bf0)と[曲面改訂33・研究資料v3.14・commit f62d862](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/tree/f62d86253aba0c477a1f9988624c0ca5a1d245f5)。確認日2026-11-22。KEの数学本文は総説に固定した[Part IV v1.9・Part V commit b2180e5](https://github.com/uedakazushi/kaehler-einstein-degeneration/tree/b2180e553b73d3a9dfd5d1146c4146c67f2055e7)から不変である。表の照合は定理と仮定・適用先の照合であり、外部の全証明の独立再検証ではない。

| 正本・定理ラベル | 入力・出力と利用範囲 |
| --- | --- |
| Part I `thm:intro-metric`, `thm:contract`, `thm:rough`, `cor:based-ball-approximation`, `prop:RZ` | 固定ample SNC対のcomplete KE metric。Clean collar＋metric-IRFAからproperな1-Lipschitz全射と加法誤差K。対応する中心を持つ閉球のGH誤差≤3K/(2R)は中心・半径に一様。退化族のmoving領域の一様性は含まない。 |
| Part II `thm:intro-star`, `thm:intro-general-completion`, `hyp:controlled-pushoff` | Marked residual複素・双曲曲線のperiodsとTorelli。一般WP completionにはcontrolled push-off。曲面の第二作用積分との同一視はない。 |
| Part III `hyp:Hloc`, `hyp:Hanc`, `thm:actual-global-pgh` | Ordinary/conifold whole-end比較とtracked anchors等を追加仮定とする。対象・positive square模型・空間的blow-downを曲面退化と区別する。 |
| Part IV `coarse:cor:degree-d-volume-lower`, `coarse:thm:full-triple-tensor` | 全固定d≥5のcapped volume下界と深部triple比較。後者の詳細証明は `papers/sections/full_triple_comparison.tex`。 |
| Part IV `simplex:cor:actual-closed-corner-metric`, `pair:thm:fixed-end-moment` | Closed tripleの内在・protected距離、および固定source-free residual compact上のmoment入力。全曲面ambient距離や任意のmoving exhaustionへの一様性へ拡張しない。 |
| Part IV `coarse:hyp:TC5`, `coarse:thm:main`; Part V `hyp:CPd`, `hyp:PBEd`, `thm:degree-d-limit` | Part IVの五次coarse定理は(TC)5付き。Part Vの大域適用は(CP)d＋(PBE)d付き。有限targetの直径 `thm:intro-diameter-C5` は独立。 |
| 曲面 `ke:global-metric-realization` | 一つの固定族・固定d≥5についてactual Lagrangian πと同じf=pπの全域ambient distortion消失を原稿に証明。局所入力＋直接scalar/portal比較を用い、外部CP/PBE/TC自体を検証しない。 |

曲面側の入力一覧・適用証明の正本は同repoの `research/ke-dependencies.md`。P0はPart Iのfull rough-isometry theorem全体を入力にせず、固定成分のSNC cusp評価とfixed-compact収束を用いる。本repoの総説は上の接続と条件を要約し、本文の証明を複製しない。依存定理が変わったら正本を先に保存し、利用先・総説・research-hubを追随させる。

## 固定成分・尺度・periodの辞書

全平面退化 $\prod_{i=1}^dL_i+tF_d=0$ で $H_i=\{L_i=0\}$ と置く。成分の開部分は
\[
H_i^\circ=H_i\setminus\bigcup_{j\ne i}(H_i\cap H_j)
\cong\mathbf P^2\setminus\{d-1\text{ 本の直線}\}.
\]
従ってPart Iのパラメータは $(n,m)=(2,d-1)$、log-canonical classは $(d-4)H$、固定成分の錐は $C_{2,d-1}$。Ambient $\mathbf P^3$ のd平面補空間なら $(n,m)=(3,d)$ であり別対象である。五次の成分は四直線補空間、Part Iの五直線の例は六次の成分に対応する。二重線の残余曲線は $\mathbf P^1$ から $d-2$ 個の三重点を除く。五次ではM0,3、六次以上では一般にmoduliを持つが、F_dの零点を含むsource markingの情報とは区別する。

固定補空間の $R^{-1}d_{\rm KE}$ と退化族の $R_t^{-1}d_{g_t}$、$R_t=\log(-\log|t|^2)$ は異なる極限である。固定空間の定数の存在だけから、tに依存するcutを越える一様比較を得ることはできない。Ric=-ωからω/(d−4)へ変える場合、距離は1/√(d−4)、tensorは1/(d−4)、co-Gramは(d−4)倍となる。Secondary complex periodsは残余曲線のmarked複素・双曲幾何であり、Lagrangian torusの第二symplectic actionではない。

## Part Iの端点接続で確認した論理

主稿の `lem:fibres` の直径はambient距離である。帰納仮定から得るのは同じresidual fibreに属する二点を**残余空間内で**結ぶ長さ≤B+1の曲線であり、fibre内の曲線ではない。Full collarは固定depthで全残余空間上のprincipal torus束をなすので、compactな曲線像の上で指定初期点からhorizontal liftが全区間存在する。Full-sectorのtensor比較は残余depthsに一様であるため、曲線がresidual fibreを離れても長さ評価を保つ。終端のnormal torus補正はO(exp(−t_i))である。

このendpoint版を `prop:lifting` と `cor:upper`、付録 `app:lifting` に統一した。必要なのは始点・終点のskeletal値の一致と加法長さ誤差であり、全曲線のexact trackingやfibreの内在径ではない。Finite itinerary、product synchronization、可積分誤差を使う帰納順は維持する。入力側のfull sector・exact collar構造とRochon–Zhangからのtensor翻訳は、後述の三補題が正本である。距離下界・全射性と測度側の点検範囲は次の三節に分ける。

## 全射収縮と中心・半径に一様な閉球近似

正本は主稿 `prop:cogram`→`lem:lambda-choice`→`thm:contract`→`thm:rough` と `cor:based-ball-approximation`。共通の深い閾値T_geomを全残余空間で先に固定し、そこで同じface collarに入るactive labelsだけを余計量行列に用いる。一面product metric h_iに対し、残余j面のIRFAから正規化共変ベクトルのノルムは |α_j|²_(h_i⁻¹)≤4/3。全逆計量の摂動を評価するので、normal blockを先に反転して混合項を落とす操作はない。

Row error εの左向き畳み込みからsmoothな非増加・可積分majorantを作る。これはεと同時刻で定数倍比較できるとは限らない。十分深いところまでλ=0とし、その先でλ≤1−2εかつ∫(1−λ)<∞となるよう選ぶ。f=∫λとh(u)=f(T0+u)を使えば、cellごとにhを作用させるproper全射Hを通じてS=HΨと書ける。Gershgorin評価と、各点近傍の像が一つの閉cellへ入る事実から大域1-Lipschitz性を得る。曲線がcutを無限回横切ってもよい。Fiber径は既証のambient上界から直接抑える。

指定compact K0のraw座標の上界を越えてcutを選べばS(K0)={0}となる。このとき加法定数KはK0に依存する。いったんS,Kを固定すると、任意の中心oとA,R>0について
\[
d_{\rm GH}\!\left(
\overline B_{(X,R^{-1}d_g)}(o,A),
\overline B_{\mathcal C}(R^{-1}S(o),A)
\right)\le\frac{3K}{2R}.
\]
両球はambient距離の制限を持つ。全射性でtarget点の逆像を取り、source球からはみ出す分を最短路上で戻すとK/R-denseな像を得る。基点対を含む対応の歪みが3K/R以下になるのでpointed収束も従う。中心・半径への一様性は一つの固定空間内の主張で、退化族のparameterや変動するcollarの定数を制御しない。

## LDP下界とexact-support制限の違い

正本は `lem:deep-sector-partition`、`lem:cellwise-LDP`、`lem:exp-tight`、`thm:LDP`。上界では十分深い座標の集合とface copyによる有限分割を使い、残るbounded座標を残余側へ含める。一部の座標だけがtransition内にある領域全体をcompactとは扱わない。下界ではfull face collarの正質量compact残余集合C_Fを取り、そのraw残余座標がRで割るとO(R⁻¹)となることを用いて、cone全体のopen setへ入れる。Exact-supportだけへの制限測度の正質量もraw zero fibreの正質量も不要であり、global LDPのrate function Σu_iは既存のvolume-IRFAで成立する。

**制限測度の下界が成立しないclean product cuspの例。** Y=ℝ_s×S¹_θで0<δ<1/16とし、|s|を台[−δ,δ]のeven smooth probability kernelで畳み込んだφ_δを取る。φ_δ=|s|（|s|≥δ）、0≤φ_δ−|s|≤δである。
\[
g_Y=ds^2+e^{-2T_0-2\varphi_\delta(s)}d\theta^2,\qquad
t_\pm=T_0\pm s\quad(\pm s\ge0).
\]
この計量は完備・有限体積で、両端のproduct cuspからの誤差はη(t)=4δe^{−(t−T0)}≤1/4で抑えられ、|s|≥δではexactである。体積誤差もcompactなnormal区間に支えを持つのでexponential volume-IRFAを満たす。標準の二端compactificationとproduct circle dataを使えばclean構造を持つ。

χ(T0)=0、χ(t)>0（t>T0）、深部でχ(t)=t−T0と選び、Ψ_Y(s,θ)=sgn(s)χ(T0+|s|)とする。これは二本のraysからなるℝへのproper全射だが、零fiber {s=0}×S¹の面積は0である。X=Y×Yはdepth2のclean product spaceで、Ψ_X=(Ψ_Y,Ψ_Y)。第一因子の正rayだけをexact supportとする集合は{s₁>0,s₂=0}×(S¹)²であり、体積0である。一方、一面のleading残余測度2π dV_Yはfull supportを持つ。従って、このexact-supportへ制限した測度について、ray内のopen intervalに対するfinite-rate下界は得られない。Ambient open setのLDP下界は上のfull-collar証明で成立する。

## Busemannからexact tailへの依存

`lem:level`→`thm:Busemann`→`lem:calibration` は一面metric-IRFAだけを用いる。深さt_iに対する関数√c_i∫√(1−η)をcollar外へ定数延長すると1-Lipschitzになり、level間の距離下界を直接与える。Calibrationでは最初のlevel Aを固定して終端T→∞、次にA→∞とする。近似最近点の残余位置がAとともに逃げても、この順序なら問題にならない。

`lem:residual-exp` は共通の `lem:Mellin-conditional-moments` から、actual conditional residual measures ν_i,tとleading measureの双方に一様な指数momentを与える。`lem:vertex-tightness` ではraw残余半径r=|Ψ_i|のshell m≤r<m+1について、ν_i,t(shell)≤Ce^−κmと狭いvertex sectorのnormal下界t≥h_iR−C−κ(m+1)/2を合わせる。Normal積分はCe^−h_iR e^−κm/2以下となり、shellの和が収束する。従って通常の全face volume-IRFAだけで十分で、leading/errorの分割もvolume remainderの指数減衰も不要である。まずR→∞のlimsupを取り、次に残余cut M→∞。Minimizing vertices外のangular gapは有限sectorの直接積分で処理する。`thm:tail` のnormal thresholdは二つの集合包含で挟み、actual距離のnormal単調性を仮定しない。`thm:joint` はmodel excessとの一様差と狭いthreshold stripを用い、excessのtightnessはF(R+Q)/F(R)→e^(−h_*Q)から得る。この鎖はLDP下界・co-Gram下界を用いない。

一般重みh_i=c_i^(−1/2)ではV_*={i:h_i=h_*}だけがleading tailを担い、角分布の重みはw_i/W、W=Σ_{j∈V_*}w_jである。全verticesの総和を分母に使うと、非minimizing vertexがある場合に確率の総和が1にならない。KE規格化は全c_i=1なのでV_*が全verticesとなる。Boundary空のcompact caseでは大きいRでtailは0であり、min_i h_iを定義しない。

以上の距離収縮・LDP・tailの鎖は複数担当で限定的に独立点検した。現在の原稿の全証明、外部査読、形式証明、先行研究との網羅的な新規性比較が完了したとの意味ではない。


## 全残余上の測度付き平行移動

正本は `thm:translation`。非空のnormal label集合Iとconnected face Fを固定し、normal深さのベクトルTについて min_i T_i→∞だけを課す。固定方向Rvへ比例させる必要はない。Cutoffは全残余空間上で、min_i t_iが十分深ければ1となるnormal cutoffである。Π_T=(t_I−T,π_F)と置くと
\[
\left\|\left[e^{\sum T_i}(\Pi_T)_*(\chi_F\mu)
-e^{-\sum s_i}ds_I\otimes\lambda_F\right]
\big|_{[-A,A]^I\times X_F}\right\|_{\mathrm{TV}}
\le (2\sinh A)^{|I|}\bar\omega_F(\min T_i-A)\|b_F\|_1.
\]
ここでbarωは非増加tail envelopeである。Residual compactへ切ることなく全X_Fで成り立つ。

Metric-IRFAの一面比較をexact quotient-in-stagesに沿って反復すると、全normal torusを潰すRiemannian submersion modelが得られる。短いambient経路はnormalの有限側境界へ戻れず、残余の完備性により無限遠へも退出できない。水平liftの終端をcircle内で補正すると、全torus fibreの径はO(Σe^−t_i)となる。これにより、normal offsetと残余基点が収束すれば、通常のvolume-IRFAだけでpmGH収束まで従う。

各固定半径のambient閉球をtargetの半径A±o(1)の全逆像で挟む。Target sphereのnormal sliceはEuclidean球面・一点・空集合なので、I非空ならnormal Lebesgue measureは0。従ってλ_Fにatomがあっても全ての半径で球面測度は0となり、球制限の押出し測度も全変動収束する。Smooth volume-IRFA、co-Gram、rough-isometry、LDP、exact-tail theoremはこの証明に不要である。この固定空間の基点移動は、退化族での一様tensor比較や極限交換を与えない。

## 有界primitiveとface massの規格化

`lem:CW` は滑らかなHermitian line bundle L→Yの実曲率Θに対し、M=Y∖B上でω−Θ=dβ、βとωのPoincaré normが有界なら
\[
\int_M\omega^m=\int_Y\Theta^m=(2\pi)^m\int_Yc_1(L)^m
\]
を示す。有限体積と有界勾配のcompact cutoffからStokes境界項が0へ行くため、指数的shell評価は不要である。β=dᶜψの場合もψの有界性は要求しない。

Rochon–Zhangのbackgroundではq_i=−log(ε‖s_i‖²)、ω₀=Θ−2Σddᶜlog q_i、ω_KE=ω₀+ddᶜuなので、β=dᶜ(u−2Σlog q_i)を取れる。u∈C∞_fcと局所式q_i=−log|z_i|²+O(1)からβの有界性を直接確認できる。主稿の `app:CW` にこの適用を展開した。

実計量とKähler formはω(v,w)=g(Jv,w)、dV_g=ω^m/m!、曲率はΘ/(2π)=c₁(L)とする。Normal depth t=log(−log|z|)・circle周期2πに対してg_P=dt²+e^−2t dθ²であり、λ_F=(2π)^k dV_gF。Adjunctionと合わせて、`thm:facemass` の係数は (2π)^n/(n−k)! となる。Residual次元0は一点の体積1、boundary空はcompact Chern–Weilとして処理する。

**一次資料の確認範囲。** [Rochon–Zhang 1106.0873v2](https://arxiv.org/html/1106.0873v2) の (2.26)–(2.30)、Definition 2.10、(2.69)–(2.70)、(5.1)–(5.9)、Lemma 5.2冒頭を照合した。Monge–Ampère potentialのbounded derivativesは(5.6)直後に記載され、ここではTheorem 5.1の残余減衰を使わない。[Mumfordの著者版](https://www.dam.brown.edu/people/mumford/alg_geom/papers/1977b--HirzProp-GT.pdf)、第1節・Theorem 1.4の定義とstatementは検索索引で確認したが、PDF本文の取得・全証明の精読は未了。Good metricsは比較remarkに留め、直接Stokes証明の依存入力にしない。

## 全faceの体積評価と一様Abel–Mellin recursion

I-normal depthsをTに固定し、normal torusを積分した残余測度をν_F,Tとする。一般Borel densityではconditional measureはa.e. Tで定まり、以下の上限はessential supremumで解釈する。Exact quotient-in-stagesを使い、残余の深いlabel集合JごとにI∪Jのvolume-IRFAを適用すると、r_αを残余depth、χ(r_α)を非負raw depthとして、全q<1に対し
\[
\mathop{\mathrm{ess\,sup}}_{\min T_i\ge L}
\int e^{qH_F}\,d\nu_{F,T}<\infty,\qquad
H_F=\sum_\alpha\chi(r_\alpha).
\]
同じ評価はleading measure λ_Fにも成立する。これは実際の密度を評価した結果であり、任意に選んだdominator b_F自体にweighted momentがあるとは主張しない。

Compact subcritical parameter集合でτ_*<q<1を選び、σ_T=|ν_F,T−λ_F|とする。Hölderにより
\[
\sup_{\tau\in K}\int e^{\sum_\alpha\tau_\alpha r_\alpha}\,d\sigma_T
\le C_K\sigma_T(X_F)^{1-\tau_*/q}
\left(\int e^{qH_F}\,d\sigma_T\right)^{\tau_*/q}\longrightarrow0.
\]
これをnormal product Abel kernelへ適用すると、`thm:Mellin-recursion` のparameter一様性が通常の全face volume-IRFAから従う。Normal torusはλ_Fに含まれるため、右辺に再度(2π)^|I|を掛けない。Normal cutoffのtransitionは一つのnormal depthが有界となる領域だが、chart partitionの重なりは深部にもあり得る。後者ではpartitionの和が1であることを使う。

**一面だけの支配の限界。** Normal anglesを積分したquadrant densityとして、t,r≥0、0<α<1で
\[
d\mu=e^{-t}(e^{-r}+e^{-t}e^{-\alpha r})\,dt\,dr
\]
を考える。t方向のconditional measureはν_t=(e^−r+e^−t e^−αr)dr、leading measureはe^−r drで、全変動誤差はe^−t/αである。しかしα<τ<1なら各ν_tのτ指数momentは無限大になる。この密度はfull r-face/cornerのvolume-IRFAを満たさないので、全face版定理の反例ではない。全ての深い面を制御する必要を示す。

**Dominationの選択は固有でない。** Exact product $d\mu=e^{-t-r}dt\,dr$ ではerrorが0なので、$b=e^{-\alpha r}$ も形式上dominatorに選べる。そのbのweighted momentは発散し得るが、b=0という別の良い選択もある。したがって、任意のchosen bの可積分性と、実際の測度の一様momentを区別する。

単独のface mass一覧からは面のincidenceを確定しない。I⊂J、F⊂D_I、G⊂D_Jについてχ_Fχ_Gを使ったmixed localized transformのJ-Abel係数は、G⊂Fならm_G、そうでなければ0である。正質量により、このlabel付きmixed観測の集合からconnected faceの包含関係を検出する。

複素meromorphic continuationは、normal変数x_i=e^−t_iについて、係数・conormal remaindersが残余L1で制御されるjoint polyhomogeneous展開を別途仮定する。通常のLaurent変数(s_i−1)では最高係数は(−1)^|I|m_Fであり、Abel規約の(1−s_i)ではm_Fである。一般SNCにfull polyhomogeneityが既知とは扱わない。比較資料はDaniel Grieser, [Polyhomogeneous functions, regularized integrals, push-forward theorem etc.](https://uol.de/f/5/inst/mathe/personen/daniel.grieser/Lehre/Singular_Analysis_2020/literature/Gri_phg-fcns_2019_03_25.pdf), 2019-03-25、第2.1.2節・Theorem 2.12・(29)–(31), pp.18–20。通常の一変数Mellin変換と極・係数の対応を確認し、本稿の多変数・残余L1の条件は本文で明示する。

**Abel residueとmeromorphic continuationの違い。** 一面density dμ=e^−t(1+(1+t)^−1)dt、t≥0は通常のvolume-IRFAを満たす。ε=1−sに対して
\[
\mathscr M(s)=\varepsilon^{-1}
+e^\varepsilon\int_\varepsilon^\infty e^{-u}\frac{du}{u}
=\varepsilon^{-1}-\log\varepsilon+O(1).
\]
従ってεM(s)→1だが、ε=0でmeromorphicではない。二つの結論を同一視できない具体例である。

以上の三つの鎖は担当ごとの独立点検と統合時の再読を行った。全文の外部査読・形式証明・網羅的新規性確認を終えたとの意味ではない。

## SNCカラーとRochon–Zhang入力の翻訳

証明の正本は主稿付録 `app:SNC` の三補題である。

| ラベル | 内容と必要な制御 |
| --- | --- |
| `lem:SNC-compatible-collars` | 元の実有向blow-upの $\rho_i=\|s_i\|$ を固定。全残余strataを次元順に、collars→全normal line bundleのproduct connectionsの順で構成。可換性は既設flowでの相対延長から得て、可換なfieldsを後から平均しない。 |
| `lem:fc-collar-transfer` | 残余norm保存と各faceでのcircle-equivarianceにより、局所正則射影との差の係数は $\rho_i A$ となり、Aの残余face traceはbasic。全fc角微分に必要な残余 $\rho_j$ 因子が生じる。Ξとexact collar pullbackの差は任意Nに対し $x_i^N C^\infty_{\rm fc}$。 |
| `lem:RZ-collar-tensor` | RZ Theorem 5.1の共通νと背景形(5.3)を組み合わせ、全微分を含め $g_{\rm KE,I}-g_i^\times\in x_i^{\nu_0}C^\infty_{\rm fc}$、ν0=min(1,ν)。残余depths全域で一様。 |

Connectionの残余角係数は対応faceで消え、通常接方向の係数はcircle-basicである。法一形式 $d\rho_j$ 自体もfc coframeで急減衰するため、connectionと全有限階fc微分は一様有界になる。Hessian比較には局所正則射影を介し、非正則collar射影とddᶜが可換だとは仮定しない。RZの残余potentialがlog compactificationまでsmoothであることも仮定しない。有限face反復とdeterminantのsmooth性からsmooth/exponential volume-IRFAを得る。

**カラー条件を省略できない理由。** 主稿 `rem:log-collar-obstruction` に二つの例を置く。Product cuspでlog-smooth変更 $(x,\theta,y)\mapsto(x,\theta,y+x\sin\theta)$ を行うと、unit angular vectorへのtensor誤差は $\cos^2\theta$ となり消えない。またrho-smoothな残余射影 $p_i(r_i,r_j,\theta_j)=(r_je^{r_i\sin\theta_j},\theta_j)$ はface上circle-equivariantでも残余normを保存せず、$f=x_j^\alpha$（0<α<1）のpullback差の二回fc角微分に $-\alpha r_i\sin\theta_j x_j^{\alpha-1}$ が現れる。後者はboundary値0のconormal関数でも破れる。いずれも任意のカラー変更についての障害であり、適切に選んだカラーでのKE定理の反例ではない。

**一次入力と監査範囲。** Rochon–Zhang, [arXiv:1106.0873v2](https://arxiv.org/html/1106.0873v2), Lemma 1.1・(1.10)–(1.15)、Lemma 2.4・(2.25)–(2.29)、Ξの(2.43)–(2.46)、背景形(5.3)、(5.10)、Theorem 5.1を直接照合した。Albin–Melrose, *Resolution of smooth group actions*, [arXiv:1012.5765v1](https://arxiv.org/pdf/1012.5765), Definition 1.1・Proposition 1.2・(1.3)–(1.4), pp.4–5の固定defining functionsに対するboundary product constructionを用い、SNCのtorus図式に必要な相対boundary条件を本文で証明した。全S¹の交わりへ、異なるfiber次元を要求する一般iterated-fibration theoremをそのまま引用していない。三補題と適用鎖は複数担当で独立に読み合わせた。Part Iの他の全証明や、退化族のparameter一様性、Part IIIのactual localizationはこの点検範囲に含めない。

## 成分の距離錐と選択した中間尺度

曲面repoの `topo:component-cone-germ` では、成分頂点 e_i の半径0<r<1/2の閉球が C_{2,d−1} の同半径球とambient距離で等長であることを証明する。正規化global distortionを ε_t=dis(f_t) と置くと、同repoの `ke:intermediate-component-cone` は
\[
a_t\to\infty,\qquad a_t/R_t\to0,\qquad R_t\varepsilon_t/a_t\to0
\]
の下で、x_{i,t}∈f_t^{-1}(e_i)を基点とする (X_t,a_t^{-1}d_{g_t},x_{i,t}) のpointed GH極限が同じ錐になることを示す。a_t=R_t√(ε_t+1/R_t)は一つの許容選択である。一般に $\eta_t=\sup_{y\in A_t}d_\square(f_t(y),e_i)\to0$ なら、誤差条件を $R_t(\varepsilon_t+\eta_t)/a_t\to0$ とすることで全基点 $y_t\in A_t$ に一様となる。同じfibrationのcomponent coreと変更collarの合併には $\eta_t\le Cq_t$、$q_t=(1+\log(N_{j(t)}+1))/R_t\to0$ を使い、$a_t=R_t\sqrt{\varepsilon_t+q_t}$ を選べる。二つの証明の正本は[曲面repo](https://github.com/uedakazushi/surface-lagrangian-torus-fibration)の現行主稿。これは同じglobal mapとtarget小球の幾何から得る帰結で、Part Iの固定空間の極限との任意の極限交換や、任意指定尺度での収束は述べない。

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
Rochon–Zhang, *Asymptotics of complete Kähler metrics of finite volume on quasiprojective manifolds* (Adv. Math. 231 (2012)) の Theorem 5.1 は **SNC pair** の全 strata にわたる共通指数 \(\nu>0\) の \(x_i^\nu C^\infty_{\rm fc}\) 漸近を扱う。Theorem 7.4 の full polyhomogeneous expansion は **smooth divisor** を仮定する。一般 SNC へ Theorem 7.4 をそのまま適用しない。主原稿の `rem:RZ-primary-scope` に一次資料との対応を統合した。Theorem 5.1からmetric-IRFAへの翻訳は上記三補題に展開した。大域距離・LDP・tailは上記の鎖を別に点検しており、これらの限定点検と全Part I–IIIの包括的再監査は区別する。

一般位置の五直線の規格化では \(L=2H\), \((L^2)=4\) なので、主稿のface mass formulaを代入すると
\[
\mathfrak m_\varnothing=8\pi^2,\qquad
\mathfrak m_{\{i\}}=8\pi^2,\qquad
\mathfrak m_{\{i,j\}}=4\pi^2.
\]
四点除去球面のcurvature \(-1\) metricの面積は \(4\pi\)（Gauss–Bonnet）で、normal circleの \(2\pi\) と合わせて一階面mass \(8\pi^2\) を得る。この計算は記法と体積係数の検算であって、漸近公式の解析的証明ではない。

## 入力の監査
Part IのRochon–Zhangからのrecursive uniformityは上記の範囲で照合した。Part IIIのTian–Yau/Yau、Datar–Fu–Song、Dumas–Wolf等の適用条件は引き続き個別照合を要する。post-trilogy v2.2の本文をpapers/research-directions.texへ保持した。最新版ではactual localization自体も(H_loc)へ分離されており、旧稿の証明済みという状態を維持しない。
## Smooth-divisor の x log x 共鳴と有効な減衰指数
Rochon--Zhang の Theorem 7.6 を、smooth degree e>n+1 hypersurface D_e⊂P^n (n≥2) に直接特殊化すると、同論文 Theorem 7.4 の背景計量・体積形の規格化で KE ポテンシャルの x log x 係数は
\[
\widetilde b_e
=-\frac{2(n-1)}3
\frac{c_1(TD_e)^{n-2}\cdot c_1(N_{D_e/\mathbf P^n})}
     {c_1(TD_e)^{n-1}}
=\frac{2(n-1)e}{3(e-n-1)}.
\]
n=2では2e/[3(e-3)]で、原論文 Example 7.7 と一致する。t=-log x なら x log x=-t e^{-t} であり、O(e^{-\nu t}) は任意 \nu<1 で成立するが、O(e^{-t}) とは一般にいえない。一般のmetric-IRFAにlog-free指数1を入力しない。t e^{-t}自身は可積分で \(\int_T^\infty t e^{-t}\,dt=(T+1)e^{-T}\)。大域粗等長性の全証明に代わらない。数式の証明は主原稿 papers/multiscale-kaehler-einstein.tex の prop:RZ-smooth-hypersurface-coefficient。一次資料：Rochon--Zhang, Adv. Math. 231 (2012), 2892–2952, Theorems 5.1, 7.4, 7.6, Example 7.7, DOI 10.1016/j.aim.2012.08.005。smooth divisorとSNCを混同しない。

