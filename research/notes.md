# 研究ノート：多重スケールKE（配置補空間）
更新：2026-11-22 / v1.17（Part I v1.9、総説v1.13）

## 現行稿の仮定
Part IIの一般WP completionはcontrolled parallel push-off付き。Part IIIのactual localization・pGHは(H_loc)+(H_anc)付き。旧草稿の強い記述より現行原稿とsource-audit.mdを優先する。

## 三研究の定理接続と正本

研究・編集・証明監査は共同で進め、各証明は次の正本に保持する。現行接続先は[KE Part IV v1.12・Part V v1.10・研究資料v1.24](https://github.com/uedakazushi/kaehler-einstein-degeneration/tree/11910259dd1628d542df57d370123d0a40b08d61)と[曲面改訂43・保存commit 1716a17](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/tree/1716a175dddbccf23e86027c34fba239c0cf527b)。資料確認日は2026-11-22。今回の数学的点検はPart Iの積の複素対数germと距離分布回収、および総説への現在有効な三研究の結果の統合である。既存のPart Iの全face/tail/Abel鎖、Part IVのcapped下界と固定end、曲面のactual両端period・全moment・作用接続・確率体積極限の指定点検は有効な範囲で保持する。全原稿・P0全体・外部解析原著の全面再監査ではない。

Part I v1.9は73頁、総説v1.13は20頁にLuaLaTeXで組版し、両稿とも未定義参照・引用、重複label、欠字、LaTeX error、overfull/underfullの主要6分類は零である。Part Iの指定13頁、総説の指定14頁を150 dpiで実表示し、切れ・重なり・欠字を認めなかった。Part Iの命題・再和式の頁跨ぎは連続性を保ち判読できる。全頁の逐頁表示ではない。Part II–III・研究素材のTeXと有効な既存検証記録は変更しない。数学的点検・組版・表示範囲の正本は `research/validation.json`。 総説v1.13の科学的入力は上記の曲面改訂43とPart IV v1.12である。

| 正本・定理ラベル | 入力・出力と利用範囲 |
| --- | --- |
| Part I `thm:intro-metric`, `thm:contract`, `thm:rough`, `cor:based-ball-approximation`, `prop:RZ` | 固定ample SNC対のcomplete KE metric。Clean collar＋metric-IRFAからproperな1-Lipschitz全射と加法誤差K。対応する中心を持つ閉球のGH誤差≤3K/(2R)は中心・半径に一様。退化族のmoving領域の一様性は含まない。 |
| Part II `thm:intro-star`, `thm:intro-general-completion`, `hyp:controlled-pushoff` | Marked residual複素・双曲曲線のperiodsとTorelli。一般WP completionにはcontrolled push-off。曲面の第二作用積分との同一視はない。 |
| Part III `hyp:Hloc`, `hyp:Hanc`, `thm:actual-global-pgh` | Ordinary/conifold whole-end比較とtracked anchors等を追加仮定とする。対象・positive square模型・空間的blow-downを曲面退化と区別する。 |
| Part IV `coarse:thm:boundary-to-triple`, `coarse:cor:degree-d-volume-lower`, `coarse:thm:full-triple-tensor` | Fixed-face density下界と各固定parameterでradial閉包近傍まで滑らかな負KE metricから、全phase quotient上のcomplete比較により全深部tensor安定性を得る。Parameter一様な境界上界を仮定しない。Capped volume下界が全固定d≥5の族でこの入力を供給する。証明の正本は `papers/sections/full_triple_comparison.tex`。 |
| Part IV `simplex:cor:actual-closed-corner-metric`, `pair:thm:fixed-end-moment` | Closed tripleの内在・protected距離、および固定source-free residual compact上のmoment入力。全曲面ambient距離や任意のmoving exhaustionへの一様性へ拡張しない。 |
| Part IV `coarse:hyp:TC5`, `coarse:thm:main`; Part V `hyp:CPd`, `hyp:PBEd`, `thm:degree-d-limit` | Part IVの五次coarse定理は(TC)5付き。Part Vの大域適用は(CP)d＋(PBE)d付き。有限targetの直径 `thm:intro-diameter-C5` は独立。 |
| 曲面 `ke:global-metric-realization` | 一つの固定族・固定d≥5についてactual Lagrangian πと同じf=pπの全域ambient distortion消失を原稿に証明。局所入力＋直接scalar/portal比較を用い、外部CP/PBE/TC自体を検証しない。 |
| 曲面 `ke:global-volume-measure` | 全固定d≥5、同じf=pπによる正規化KE体積の押出しは成分頂点上の等重み1/dの原子測度へ収束。固定成分体積と全体積の一致、固定compact収束を用いる。πの固定位相底空間にも成立し、五次の作用指定射影へ移せる。全台の極限測度やmoving-neck体積速度は結論しない。 |
| 曲面 `ke:moment-relative-replacement`, `ke:relative-replacement-gh` | 同じcanonical moment・anchor cuts・保持corner全葉・source nodal neighborhoods・component領域、marked product/cone商、whole-fiber接着を保つ候補の射影値差≤Cη。C1小ささは不要。固定木系の候補がslow diagonalに沿って存在すればGHを移せる。Atlas候補の存在は入力。 |
| 曲面 `ng8:fixed-fiber-relative-dh`, `ng8:source-dh-wall` | 固定tのfree compact bandのinvariant primitiveとaffine boundary actionsからStokes面積式。Source固定点を横切る(1,−1)模型では周期2πで面積π(c−|μ|)。Actual全P0の面積公式ではない。 |
| 曲面 `ng8:componentwise-critical-area`, `ng8:strict-area-cuts`, `ng8:p0-small-area-flexibility` | Rel-Kのmarked初期familyを入力とし、critical areasの指定は自由成分への正行列配分と同値。成分別総量＋strict cutsで判定。Actual sourceの全近傍を固定した小さい総和零の変更を構成する。この微小定理自体から所定大targetは結論せず、五次の初期葉選択による全moment構成を別に用いる。 |
| 曲面 `ke:anchor-liouville-actions`, `ke:actual-anchor-fan-criterion`, `ke:anchor-stokes-budget` | Actual anchorの有限period条件からK4/Petersen core chartを構成する十分条件。Liouville homogeneityは実係数affine性を与え、整数勾配・neck切片一致は別条件。Clutchingを入力にStokes総量を計算し、relative輸送や両端matchingの存在を推論しない。 |
| 曲面 `ke:k4-protected-anchor-selection`, `ke:k4-actual-end-anchor` | 同系の仮定を満たす保持end collarsと飽和annuliにはprotected periodsによる有限判定。標準P0で全K2 end collarsだけをanchor上に保持し、source全飽和近傍をδ決定後に離す選択では、Qの負値性とactual clutchingを証明し、任意有向四角形のactual局所K4 chartを同じdomain・primitive・skeleton上に構成する。有限非零bandで元neckへ戻せるが、全neck action・反対端・全域atlas整合は含まない。 |
| 曲面 `ke:k4-actual-neck-periods`, `ke:k4-equal-weight-periods` | Actual共通primitive・transported cyclesで両端整合をresidueとsource countsの有限等式へ帰着。等重みでは対称六系と(3,1,1) allocationで満たす。自由なprimitive定数の変更は用いない。 |
| 曲面 `ng8:uniform-k2-end-periods`, `ng8:thin-source-tail-choice`, `ng8:quintic-full-moment` | 同じK2全moment評価と初期source葉の全tail選択からstrict cutsを満たし、affine critical actionsと両coreへの全開collar接着を実現。Full nodal neighborhoodsは選択後に固定する。 |
| 曲面 `ke:quintic-simultaneous-realization` | 五次の有限compatible dataから各tの同じactual πに作用適合matroidal atlasとf=pπの全曲面GHを同時実現。全平行移動付きGL(3,Z)式は非対称正weightsにも成立。Focus値は穿孔扱い。Atlasのt極限、極限integral affine構造、Hessian・Monge–Ampère性、六次・任意先指定の大source tails・t連続性・速度は含まない。 |
| 曲面 `ke:source-inclusive-fixed-shell`, `ke:global-clipped-cogram-lower` | Sourceを含む固定残余compact・固定rでの同一frameのmomentとshell横断下界。有限stageのco-Gram不等式を極限操作から分ける。異なるnormal formsのprimitive一致、任意moving exhaustionは含まない。 |
| 曲面 `topo:cubical-local-models`, `topo:cubical-moving-blowups` | 全targetのambient局所閉球から成分錐、book、角3π/2の錐、平面を得る。全moving拡大極限と任意拡大列での各有限基点の実現。 |
| 曲面 `ke:distortion-to-pointed-balls`, `ke:intermediate-moving-classification` | 全射の歪みδから同半径閉球の基点付きGH距離≤3δ/2。同じfによるa→∞、a/R→0、Rε/a→0の下でactual全移動基点の四型分類と実現。 |

曲面側の入力一覧・適用証明の正本は同repoの `research/ke-dependencies.md`。P0はPart Iのfull rough-isometry theorem全体を入力にせず、固定成分のSNC cusp評価とfixed-compact収束を用いる。本repoの総説は上の接続と条件を要約し、本文の証明を複製しない。依存定理が変わったら正本を先に保存し、利用先・総説・research-hubを追随させる。

## 同じ曲面射影の体積測度極限

正本は曲面改訂43の `papers/sections/paper/ke_global_metric_realization.tex`、`ke:global-volume-measure`。固定d≥5と既存の同じf_t=p_Tπ_tを用い、ν_t=dV_t/[2π²d(d−4)²]とすると
\[
(f_t)_*\nu_t\rightharpoonup \frac1d\sum_i\delta_{e_i},\qquad
(\pi_t)_*\nu_t\rightharpoonup \frac1d\sum_i\delta_{v_i}.
\]
Part Iの `lem:CW` と体積公式から各固定成分W_iの質量はV_*=2π²(d−4)²であり、smooth fiberの全体積dV_*と一致する。固定compact K_i⊂W_iではgraph embeddingによる体積収束と、clipped-depth mapの値が最終的にe_iとなることから、f_tの像もe_iへ一様に近づく。各K_iを先に大きく取れば、互いに素なgraph像の補集合のlimsup質量を任意に小さくできる。p_T^−1(e_i)={v_i}と底空間のcompact性からπ_tにも移る。五次の作用指定射影は一様な値比較で同じ極限を持つ。

今回この証明と固定compact→全質量の極限順序を直接読んだ。Moving coreへの包含、対角列の選び直し、moving neckの一様体積漸近、追加の収束速度は要しない。極限測度は頂点に集中するが、GH極限の辺とsquareは距離として残るため、全台性を要求しないcompact measured GHの意味で述べる。これはPart Iの固定空間のscaled体積が錐頂点へ集中するLDPとは対象・写像・極限parameterが異なる。

## Part IVのcapped volume下界と監査範囲

Part IV v1.11の正本は `papers/kaehler-einstein-degeneration.tex`。`coarse:lem:capped-positivity` → `coarse:lem:weighted-cap-lower` → capped pair/triple → `coarse:thm:global-determinant`（六局所型）→ `coarse:lem:one-sided-volume` → `coarse:cor:degree-d-volume-lower` の鎖を担当が実読した。別担当は変更式・定数・量化を独立に確認した。固定d≥5、一般位置planes、三重点で非零・各double line上で単純零の固定F、small smooth fibers、固定Hermitian dataが入力であり、定数はtに一様だがdに一様とはしない。

公表補強のラベルは `coarse:eq:residue-density-normalization`、`coarse:eq:intrinsic-cap-curvature`、`coarse:eq:cap-absorption-budget`、`coarse:rem:capped-global-potential`。Adjunctionの固定residueによるcanonical densityを用い、t依存scalarを挿入しない。Chern微分の全点式でsource軸を含む正値性を示し、α_*≥4Σk_iと追加frame budgetを分ける。固定有限cover → A_0 → 各型の共通定数 → 最後にt閾値の順に選ぶ。Compact最小値原理は全smooth fiber上の一つのpotentialに適用する。この下界からactual tensorの二側比較、moving buffer、TC/CP/PBEの検証は導かない。

本ノートの編集担当は上の新式・corollary・potentialの本文を読み、全六型の実読は担当の報告として区別する。新しい外部解析定理の適用や証明書の再実行はなく、旧一次文献確認を保持する。組版120頁と指定12頁の実画像確認は退化repo側の検証記録であり、本repoでの再組版ではない。

## 固定成分・尺度・periodの辞書

全平面退化 $\prod_{i=1}^dL_i+tF_d=0$ で $H_i=\{L_i=0\}$ と置く。成分の開部分は
\[
H_i^\circ=H_i\setminus\bigcup_{j\ne i}(H_i\cap H_j)
\cong\mathbf P^2\setminus\{d-1\text{ 本の直線}\}.
\]
従ってPart Iのパラメータは $(n,m)=(2,d-1)$、log-canonical classは $(d-4)H$、固定成分の錐は $C_{2,d-1}$。Ambient $\mathbf P^3$ のd平面補空間なら $(n,m)=(3,d)$ であり別対象である。五次の成分は四直線補空間、Part Iの五直線の例は六次の成分に対応する。二重線の残余曲線は $\mathbf P^1$ から $d-2$ 個の三重点を除く。五次ではM0,3、六次以上では一般にmoduliを持つが、F_dの零点を含むsource markingの情報とは区別する。

固定補空間の $R^{-1}d_{\rm KE}$ と退化族の $R_t^{-1}d_{g_t}$、$R_t=\log(-\log|t|^2)$ は異なる極限である。固定空間の定数の存在だけから、tに依存するcutを越える一様比較を得ることはできない。Ric=-ωからω/(d−4)へ変える場合、距離は1/√(d−4)、tensorは1/(d−4)、co-Gramは(d−4)倍となる。Secondary complex periodsは残余曲線のmarked複素・双曲幾何であり、Lagrangian torusの第二symplectic actionではない。

### 主定理の適用範囲と残余の標識

Part Iの共通対象は連結smooth projective n-fold、n≥1、reduced SNC divisor D、ample L=K+Dである。Dが空なら距離coneは一点、定値写像とK=diam(X)で距離定理は成立し、faceの主張は空、tailは十分大きい半径で0となる。非空境界のBusemann/tail定理と区別する。抽象clean構造にはX=int(tilde X)、各残余の連結完備計量、deeper facesで同じ構造とnormal weightsを引き継ぐことを明記する。

一般多次数SNC配置のdual complexでは交叉の連結成分を保持する。例えばP²の横断する二つの滑らかなconicsはK+D=Hがampleで、dual complexは2頂点と4本の異なる辺を持つ。一本の辺を持つ超平面型のC₂,₂ではない。主稿 `cor:multidegree` は各connected faceの次数・質量を使う。

Part II `prop:partI-translation` の標識はcomponent-labelled collarとdeeper-face labelsから運ぶ付加構造である。`lem:metric-conjugation` により、fully marked oriented hyperbolic curveはordered complex moduli pointを決め、向きを忘れれば複素共役の曖昧さが残る。`thm:intro-star` はn本のoriented periods、`thm:intro-unoriented` は全curve factors・全cusp labelsを保ち向きだけを忘れたgeneric reconstructionを扱い、後者は配置全体の共役までの結論である。裸のmetric limitからlabelsを復元するとは主張しない。

## Part Iの端点接続で確認した論理

主稿の `lem:fibres` の直径はambient距離である。帰納仮定から得るのは同じresidual fibreに属する二点を**残余空間内で**結ぶ長さ≤B+1の曲線であり、fibre内の曲線ではない。Full collarは固定depthで全残余空間上のprincipal torus束をなすので、compactな曲線像の上で指定初期点からhorizontal liftが全区間存在する。Full-sectorのtensor比較は残余depthsに一様であるため、曲線がresidual fibreを離れても長さ評価を保つ。終端のnormal torus補正はO(exp(−t_i))である。

このendpoint版を `prop:lifting` と `cor:upper`、付録 `app:lifting` に統一した。必要なのは始点・終点のskeletal値の一致と加法長さ誤差であり、全曲線のexact trackingやfibreの内在径ではない。Finite itinerary、product synchronization、可積分誤差を使う帰納順は維持する。入力側のfull sector・exact collar構造とRochon–Zhangからのtensor翻訳は、後述の三補題が正本である。距離下界・全射性、移動基点・link、測度側の点検範囲は以下で区別する。

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

## 移動基点の分類とmetric linkの復元

正本は主稿 `thm:moving`、`prop:cone-limits`、`prop:link`。移動基点については、先に固定した粗い錐写像Sの加法定数Kを用い、scaled centers y_j=S(x_j)/R_j を有限orthant coneで分類する。有限個のcell copiesから一つを選び、座標ごとに有界／無限大へ発散する部分列を取る。発散座標のface copy α と、残る座標の極限 z により、全ての部分列極限は (C,y) または (R^α×C(Lk α),(0,z)) となる。空linkのconeは一点とする。各型はSの全射性を使って任意のR_j→∞に対して実現できるが、同じunmarked pointed isometry typeを複数のfaceが与えることはある。

積構造には、αを含むcoface copiesをαを保つface mapsだけで貼るincidence linkを使う。α座標が全て正の領域は内在長さについて積である。中心yから各α-wallまでの距離の最小値をmとすると、m>2Aで、閉A球はambient距離を含めて対応するEuclidean factor×link coneの閉球と等長になる。球内の二点から壁までの距離は各々m−A以上なので、退出・再進入する経路は2(m−A)>2Aとなる。これがambient距離の短絡を排除する。残余中心zの大きさに条件はなく、z_j→zなら球GH誤差は3K/(2R_j)+d(z_j,z)で抑えられる。

**閉starを大域積と扱えない例。** 三頂点a,b,cの三辺cycleからなるall-right linkで、aの閉starは二つのquadrantsである。b,cの半径rの点のstar内距離は2rだが、第三のquadrantを通るambient距離は√2 rになる。さらに同じ二頂点a,bを結ぶ二つのedge copiesでは、aを保つincidence linkは二点であり、abstract productのa=0上の二本のb-axisがambient coneでは同一視される。従って境界を含むclosed-star productの単射性にも注意が必要である。正のα領域と壁距離の評価は両方の障害を避ける。

Metric linkでは、各連結成分のspherical path distanceを使い、異なる成分間は∞とする。Equal-radius chord distanceからまずmin(π,d_len)を回収し、そのpath metricを取ると元のextended length distanceになる。この標準cone幾何をSのcoarse sectionへ移せばradial divergenceはO(1/r)の誤差で成立する。決まるのは固定基点blow-downのpointed isometry typeとlinkのisometry typeであり、元のdivisor labelsや選ばれたcell分割ではない。v_i=√c_i u_iという座標変更はface gluingと両立するので、metric coneだけから元のdepth規格化c_iも復元しない。Component-labelled Mellin transformsによるincidenceの検出は、このmetric dataに標識付きの観測系を加えた主張である。

**Radial familiesと一般rough rays。** 第一象限のγ(t)=(t,√t)は |t−s|≤d(γ(t),γ(s))≤|t−s|+1/2 を満たすが、どのradial rayとも有界距離にない。従ってcoarse sectionで選んだradial familiesの結果を、全rough raysのbounded-distance商やgenuine geodesic-ray boundaryへ読み替えない。Sublinear同値による方向空間は別の検討課題であり、現行主定理に含めない。

**一次文献との比較。** [Bridson–Haefliger原著](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/bridsonhaefligerx.pdf), Chapter I, Definition 5.6・Remarks 5.7（印刷pp.59–60）のcone metricとlength-metric recoveryを確認した。同書Theorem 7.39（p.115）・Lemma 7.56（p.120）はpolyhedral local modelsの入力で、無限遠の移動基点分類を直接述べる結果ではない。[Leuzinger 2004出版社版](https://www.heldermann-verlag.de/jlt/jlt14/leuzams.pdf), Lemma 5.1（pp.330–331）、Theorem 5.2（pp.331–332）、Corollary 6.3（p.336）は局所対称空間のnet上の有界加法誤差・asymptotic cone・radial公式を与える。Corollary 5.5（p.332）はそのconeをCAT(0)とする。本稿の五直線のall-right K5 coneはCAT(0)でない。`rem:K5-not-CAT0` では、頂点と反対辺中点を結ぶ二つの長さ3π/4のangular最短路から、cone内の異なる最短chordを作って直接証明する。標準cone原理自体を本研究の新規性とせず、ample SNCのKE metricからの構成と残余測度への接続を比較対象とする。指定箇所の照合であり、全関連文献の網羅的な優先権確認は未了である。

[Datar–Fu–Song, arXiv:2106.05486v2](https://arxiv.org/abs/2106.05486v2), Corollary 1.1（pp.3–4）は孤立log canonical表面特異点のcomplete負KE metricについて、無縮小の移動基点pGH極限を直線またはflat cylinderと記述する。[Engberg博士論文](https://data.math.au.dk/publications/phd/2022/math-phd-2022-lbe.pdf), Definition 1.2.12・Proposition 1.2.13（pp.25–27）は二次元Hilbert modular cuspのcharacteristic linkの非崩壊baseとexceptional dual complexのhomeomorphismを構成する。Isometryや一般ample SNC対の大域加法比較を述べる結果ではない。両者の指定本文を照合し、固定補空間のspatial blow-downとの対象・尺度の違いをIntroductionへ記した。DFSの定理番号は確認したarXiv v2に固定し、出版版の番号は未照合である。

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

## 実距離球から回復する裾係数

正本は Part I `cor:tail-intrinsic-uniform`。非空境界、metric-IRFAと全faceの通常volume-IRFAの下で、h_*は実球外体積のexponential decay rate、W(o)はその正規化極限であり、pointed metric–measure spaceの内在量である。D=d(o,o')として
\[
e^{-h_*D}W(o)\le W(o')\le e^{h_*D}W(o).
\]
したがってlog Wはh_*-Lipschitz、KE規格化では1-Lipschitzである。有限δ-netと球の包含から、e^(h_*R) μ(X∖B(o,R))→W(o)は任意の固定compact基点集合上で一様となる。非compactな全基点や退化族のparameter一様性へ読み替えない。

`prop:depth-gauge` は、許されるHermitian norm変更 ρ'_i=e^(ψ_i)ρ_i、ψ_i smooth on the compactificationに対し、t'_i−t_i=O(e^(−t_i))を全残余に一様に使う。旧normal flowに沿うlevel setsのambient Hausdorff差もO(e^(−T))となるのでb'_i=b_i。幾何学的face massは交点数として不変であり、各重みm_i exp(b_i(o))も不変である。形式的な定数shift t'_i=t_i+a_iでは新density係数はe^(a_i)m_i、Busemann offsetはb_i−√c_i a_iとなり積は保たれるが、この新係数を幾何学的交点質量と呼ばない。Circle模型の係数も変わるため、同じ正規化のmetric-IRFAへの自動適用ではない。

`ex:nonintegrable-cusp-tail` は非KEの滑らかな回転曲面であり、t≥0の端に g_a=(1+a/(1+t))²dt²+e^(−2t)dθ²、a≥0を置き、compact capのpoleからの距離をr=ℓ+t+a log(1+t)とする。全aで距離錐はray、leading normal massは2πであり、通常volume-IRFAを満たす。一方、裾は2πe^ℓ R^a e^(−R)と漸近する。a>0の非可積分metric誤差では有限なexact-tail係数が失われる。a=0でもℓを変えると同じrayとnormal massのままWが変わる。これはcoreの距離offsetの必要性を示す解析例であり、KEクラスの反例でも、rough cone比較一般への反例でもない。

先行研究との比較では、Chambert-Loir–Tschinkel §4.2式(4.1)のalgebraic height sublevelsと本稿の有限体積の実距離球外側を区別する。一面でlog H≈λe^tとなるheightとt+b_i(o)で較正される距離は異なるobservableである。実球のBusemann較正と全faceのconditional momentsが本稿のWへ接続する。一般的な基点比較・有限netの原理やresidue-measure原理自体の新規性を主張せず、一次資料の指定箇所と未確認点は `source-audit.md` を参照する。


## KE積の実球裾と距離Laplace変換の対数項

証明の正本は Part I `lem:hyperbolic-curve-tail` と `ex:KE-product-distance-log`。尖点付き有限面積双曲曲線Sの固定基点pについて、各cuspを上半平面のparabolic quotientで表す。pのdeck orbitの最大高さv_c(p)は、cusp外での高さの上界とparabolic translationで割ったorbitの局所有限性から達成される。垂直方向の距離下界と一つの最大高さのliftによる上界は、角に一様なO(v^−2)誤差を与える。従ってA(p)=Σ_cℓ_c/v_c(p)>0として、F_S(R)=A(p)e^−R+O(e^−3R)。最大高さ以外とのgapや最近liftの一意性は要らない。

種数2以上のcompact双曲曲線Yとの積X=S×Yは、ample SNC対のactual負KE曲面である。o=(p,y_0)、V_Y=vol(Y)として
\[
\begin{aligned}
F_X(R)&=e^{-R}\left(W(o)+\frac{C_o}{R}+O(R^{-2})\right),\\
W(o)&=A(p)V_Y,\qquad
C_o=\frac{A(p)}2\int_Y d_Y(y_0,y)^2\,dV_Y>0,\\
\mathcal Z_o(1-\epsilon)&=\frac{W(o)}\epsilon+C_o\log(1/\epsilon)+O(1)
\quad(\epsilon\downarrow0).
\end{aligned}
\]
この二次項は厳密な積距離d_X²=d_S²+d_Y²から生じる。Cusp coordinate qでt=log(−log|q|)とすればnormal densityは厳密にe^−t dt dθ dV_Yであり、normal-depth transformは2πV_Y/(1−s)+entireである。従ってpolyhomogeneousなnormal densityから実距離Laplaceの有理型性や実球裾の指数的な誤差改善は導けない。この初等的な一側漸近を、以下の積の命題は複素領域へ強める。

これは既存の非KE回転cusp例（metric誤差の非可積分性）および抽象測度の `ex:Abel-not-meromorphic`（通常volume-IRFAの弱いremainder）とは別の障害を示す。標準双曲cuspと積距離による直接計算であり、先行例の網羅的調査・優先権確認は未了。作成担当と統合担当がこの指定証明を点検し、cusp表示の一次資料は `source-audit.md` に記す。

### 複素対数germとradial分布

正本は Part I v1.9 `prop:compact-product-logarithmic-germ` と `cor:compact-radial-recovery`。Yは任意の閉コンパクト連結Riemann多様体でよく、b=d_Y(y_0,y)、M_k=∫_Y b^k dV_Yと置くと
\[
\begin{aligned}
\mathcal Z_o(s)&=\frac{W}{1-s}-H_o(s)\operatorname{Log}(1-s)+G_o(s),\qquad W=A(p)M_0,\\
H_o(s)&=\frac{A(p)s}{2}\sum_{m\ge0}\frac{M_{2m+2}(s^2-1)^m}{4^m m!(m+1)!}.
\end{aligned}
\]
解析接続域は {Re s<3}∖[1,3)、H_oはentire、G_oはRe s<3全体で正則である。曲線側のO(e^−3r)はStieltjes部分積分で処理し、その微分評価を追加しない。厳密な積距離からu=r+√(r²+b²)へ変数変換し、指数積分の対数項とentire剰余を一様絶対収束で分離する。詳細な証明をノートに重複させず、本文の `eq:product-stieltjes-remainder`、`eq:product-kernel-holomorphic-bound` を参照する。

正向き一周のmonodromyは−2πiH_o。z=0で値1の平方根を使い、Φ(z)=2H_o(√(1+4z))/(W√(1+4z)) と置けば、M_(2m+2)/M_0=(m+1)!Φ^(m)(0)。総質量1と全偶数momentsからコンパクト台上の多項式稠密性により確率的な基点距離分布ρを回収する。有限個の係数からの回収や安定性は主張しない。Yが一点ならH_o=0。正次元のコンパクト負KE因子ならH_o(1)>0で、総複素次元2以上のactual負KE積に適用できる。一般volume-IRFAからの複素解析接続ではない。

付随する幾何学的情報として、smooth正次元因子のρ([0,r])は小球漸近ω_n r^n/vol(Y)に従うため、全距離分布から実次元nとvol(Y)も決まる。この短い帰結は研究ノート内の観察であり、本文の系は距離分布の復元を主張単位とする。これでも以下の例の通り等長型は決まらない。

### 一つの基点で全半径の球体積が一致する非等長なコンパクト因子

これは一般Riemann因子における限界の明示例であり、負KE因子に限定した剛性の反例ではない。球面S²の極座標r∈[0,π]、θ∈R/2πZで、零でないχ∈C_c^∞((0,π))と0<|ε|‖χ‖_∞<1を選び、
\[
a_\epsilon(r,\theta)=\sin r\,(1+\epsilon\chi(r)\cos2\theta),\qquad
 g_\epsilon=dr^2+a_\epsilon^2d\theta^2
\]
とする。両極の近くではround計量と一致するので滑らかな正定値計量へ延びる。北極oからは|dr|≤dsであり、radial曲線が長さrを実現するからd(o,(r,θ))=rである。面積要素a_ε dr dθのθ平均により、全0≤R≤πについて
\[
 \operatorname{area}_{g_\epsilon}B(o,R)=2\pi(1-\cos R),\qquad
 \operatorname{area}_{g_\epsilon}(S^2)=4\pi.
\]
他方、Gauss曲率K=−∂_r²a/aは
\[
K_\epsilon=1-
\frac{\epsilon(\chi''+2\cot r\,\chi')\cos2\theta}
{1+\epsilon\chi\cos2\theta}.
\]
非零のcompact-supported χについてχ''+2cot rχ'が恒等的に零になることはない。実際、それが零なら(sin²r χ')'=0で、支持の外でχ'=0だからχ'=0、さらにχ=0となる。従ってε≠0では曲率は定数1でなく、round球面と等長ではない。

同じSとのRiemann積では、全rでの距離分布が一致するのでRe s<1で距離Laplace変換の全体が一致する。対数germだけでなく変換全体からも一般の基点付き等長型は復元できない。上の距離・面積・曲率の直接計算は統合担当と独立担当が照合した。形式証明器による検証ではない。

### 一次比較と残る拡張の核心

DLMF 6.6.2、8.19.7–8、8.19.12、10.25.2に対応するexponential-integral/Besselの仕組みは古典的である。Golubev–Kamberの有限面積双曲曲面の距離集中は同じ実距離observableを扱うが、面積で定まるR_X付近の族一様評価であり、固定SのR→∞のcusp裾係数と積のgermとは漸近の領域が異なる。Grieserの通常のpolyhomogeneousクラスに対し、実距離変数x=e^−RのR^−1は−1/log xに対応する。Normal-depth側のpolyhomogeneityと実距離側の分岐を同一視しない。確認版・頁・仮定は `source-audit.md` に集約する。

非積のKE空間へ進めるには、実距離又は距離pushforwardの高次誤差をどの解析入力が制御するかを先に特定する。厳密な積距離を失ったとき、通常volume-IRFAとleading tensor比較のみから今回のH_oやRe s<3の正則剰余は出ない。これは次の研究課題であり、現行の証明済み命題の適用範囲へ混ぜない。

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

LDPの確率測度μ/μ(X)から面極限を取れば、λ_Fとm_Fを共に全体積で割る。主稿 `rem:probability-face-mass` の式は、hat m_F=n!/(n−k)!·(L^(n−k)·F)/L^nである。異なるfaceの拡大極限は確率分割ではないため、その質量和は1と限らない。五直線P²では全体積8π²、各divisor face 8π²、各intersection point 4π²なので、確率規格化の面質量はそれぞれ1、1/2となる。

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

**Abel residueとmeromorphic continuationの違い。** 証明は主稿 `ex:Abel-not-meromorphic` に置く。Exact cusp上の抽象有限測度 dμ=(2π)⁻¹e⁻ᵗ(1+1/t)dt dθ（t≥T>1）ではordinary volume-IRFAと面質量1を持つが、ε=1−sに対するlocalized transformは M(1−ε)=ε⁻¹+log(1/ε)+O(1) となる。Abel係数は1でも、simple poleを引いた対数発散により臨界点近傍への有理型延長は存在しない。これはKE体積そのものの反例ではない。

全faceのconditional moments→vertex tightness→actual-ball tailとweighted total variation→一様Abel recursionを今回対象限定で再読し、新たなgapを認めなかった。一般Borel densityでのa.e. disintegration、全残余での深いsector分割、compact subcritical parameter集合、法cutoffとchart partitionの違いを確認した。SNCカラーとRochon–Zhang入力の全面再監査、全文の外部査読・形式証明・網羅的新規性確認とは区別する。

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

## 曲面側の固定段階入力と全域ambient接続

証明の正本は曲面原稿。`ke:source-inclusive-fixed-shell` では、三重点を避けsourceを含んでよい固定残余compact P⊂int P+上で、同じ射影正規形 x′y′=t h_t(p)と非零正則体積frame Ω_t=dlog x′∧dp=−dlog y′∧dpを用いる。Ω_tはsourceにも延びる。先にPとrを固定し、s_r=−log r²と置くと、全base points・phaseについてmomentは±4π/s_r+O(s_r^(−1−δ))+o_t(1)。O定数は小rに共通だが、tの閾値はrに依存してよい。r²≤|x′|≤rのshell横断費用はc_P log2以上となる。Songのfixed-smooth-locus収束とRochon–Zhangの成分cusp評価を用い、任意の小さい複素tを扱う。別normal formのprimitiveとの差はclosed項として保持し、同一性や残余period消滅を追加しない。

`ke:global-clipped-cogram-lower` は一つのt,m,Kを固定し、S=R−log m−log K∈(0,R]、ε≥0とする。Strictにactiveな共変ベクトルの全co-Gram matrixが(1+ε)Id以下なら、任意のrectifiable curve γについて
\[
L_\square(\Theta_t\gamma)\le \frac{R\sqrt{1+\epsilon}}S L_{R^{-2}g_t}(\gamma).
\]
これは有限parameterの不等式で、εの小ささやε→0を補題の仮定にしない。q=S/(R√(1+ε))には1−q≤(log m+log K)/R+ε/2が成り立ち、固定targetの直径から加法誤差へ移せる。誤差消失は全局所定数・core深度・clipping parametersを選んだ後のslow diagonalでのみ課す。

全域上界は `ke:same-moment-corner-reference`、`ke:coherent-corner-portals`、`ke:point-to-corner-portal`、`ke:global-ambient-upper` のendpoint比較で得る。旧full corner内の経路は除去capを通ってもambient経路として有効で、保持領域内に閉じ込めない。同じmoment上の異なる葉とsource・saddleを含む全fiber合併を接続し、成分側は一つの成分ごとに拡大固定compact内で接続する。固定PとC_j^neckをN_j前に選び、C_j^neck≤1+log(N_j+1)で吸収する。M本のgalleryにはM−1のjunctionと両端の二接続が必要で、合計(M+1)Hとなる。Anchor等号境界、support二元の旧corner辺、同じanchorを持つ両端点まで点検した。Strictなtarget曲線の持上げやfiber内の経路は入力にしない。

## Canonical momentを保つ相対変更と面積の障害

曲面 `ke:moment-relative-replacement` の入力は、同じ保持cornerとK2交わりを含むend collarsの全葉、sourceのcompact nodal neighborhoods、同じactual normal circle・向き・加法定数を持つcanonical moment・anchor levels、同じcomponent coreと変更collarである。候補のneck商にはd−2個のlabelled endsを持つ許容三価木の実際のmarked productが必要で、core商は対応するlabelled linkのconeとする。全局所商をcompact Hausdorffとし、全交わりを双方の全fiberの合併とし、そのpartitionを一致させる。木の抽象同型、局所座標だけの一致、normal momentだけの保存では入力を満たさない。

この条件で先にwhole-fiber閉商を作り、同じcorner parameter化と共通profile σ_t(μ)を用いて新しいmarked底空間へ同定すると、保持corner上では厳密に同じ射影値を持ち、全域では
\[
\sup_{x\in X_t}d_\square(f_{j,t}(x),\widehat f_{j,t}(x))
\le C\eta_{j,t},\qquad \eta_{j,t}=\frac{1+\log(N_j+1)}{R_t}.
\]
両像が同じ小さなcomponent cap内にあることと、neckで同じμの辺像を比較するだけで足り、reduced葉のdiffeomorphismのC1小ささは不要である。`ke:relative-replacement-gh` は一つの固定木系の候補がslow diagonalに沿って存在する場合に、dis(fhat)≤dis(f)+Cη→0を得る。全coarse fiber、すなわち一つのp_T-fiber上のLagrangian fibersの合併もambientに一様収縮する。Atlas候補はこの安定性定理への入力であり、五次では下記の全moment構成が実現する。六次での同時実現は未解決である。

`ke:raw-moment-error-insufficient` は固定stageと0<α<β<1に対し、μ_t=−L_t^(−α)、ν_t=−L_t^(−β)を使う。Raw momentの差は零へ向かうが、σ_t(μ_t)→α、σ_t(ν_t)→βなのでtargetの辺距離は消えない。近似matchingにはprofile値の一様誤差を制御する必要がある。この例はatlas不存在を結論しない。

`ng8:fixed-fiber-relative-dh` は固定t≠0、自由な周期2πのcircle作用、E_t/S1≅J×P（Pは境界を持つcompact connected surface）、作用不変primitive λ_t(V)=μを仮定する。Boundary framingとcutsを固定し、向き付き第二作用R_ℓ,t(μ)がaffineなら、Stokesにより面積は2πΣ_ℓ(R_ℓ,t(μ)+k_ℓ,t μ)、k_ℓ,t∈Zでaffineとなる。Reference constantsのt依存を許し、t=0へのsmooth extensionや族一様性を入力にしない。

現行曲面稿では `neck_action_matching.tex` 前半の `ng8:central-criterion` までを、compact nodal fibersとその飽和近傍から離したsource-free neckに明示的に限定する。固定t≠0でもactual source-inclusive neckのμ=0には固定点があるため、その全intervalへ自由作用の自明化又は面積affine性を流用しない。

`ng8:source-dh-wall` の標準C²、I_k=|z_k|²/2、weights(1,−1)、μ=I_1−I_2、I_1+I_2≤cでは、周期2πのreduced angleにより面積はπ(c−|μ|)となる。固定点μ=0で折れるため、free-bandの式をsource横断intervalに流用できない。これはactual P0全体の面積公式ではない。相対Moserではsource近傍を保持して支持を離し、以下の成分別条件と端germs・marked identificationsを検証する。

### Sourceを固定した有限面積輸送

固定集合K、自由成分U_α、初期critical regions D_hとその実際のsmooth marked trivializationを与える。IncidenceはE={(h,α):D_h∩U_α≠∅}、protected massはκ_h、自由要求量はr_h=a_h−κ_h、自由成分の面積はM_αとする。`ng8:componentwise-critical-area` は、初期familyと同じDiff₀(P rel K)-orbitでの実現が
\[
x_{h\alpha}>0\ ((h,\alpha)\in E),\quad x_{h\alpha}=0\ ((h,\alpha)\notin E),
\qquad\sum_\alpha x_{h\alpha}=r_h,\quad\sum_hx_{h\alpha}=M_\alpha
\]
と同値であることを示す。自由部分の形式とr_hがsmoothならよく、κ_h自体のsmoothnessは不要。Pointwiseな正解を固定線型right inverseとpartition of unityでsmoothに選び、密度のcell積分を指定してから、各U_αの零積分差に固定支持primitiveを作ってMoserを行う。ρ=1をcritical leavesの近傍にも課せるが、Moser写像がその葉を固定するという意味ではない。

`ng8:strict-area-cuts` では、非孤立rowの要求量r_hを正、孤立rowを零、全M_αを正とする。その下で二部graphの各連結成分ごとの総量一致と、非空properなregion集合Sに対するΣ_{h∈S}r_h<Σ_{α∈N(S)}M_αが必要十分である。Graphとmarginsがcompact parameter上で連続ならstrictな余裕は一様となる。Marginsが全てaffineのintervalでは端点確認で足りるが、smoothだけでは足りない。固定annulusの内側U₀が一つのbasinだけに接すると、そのbasinには少なくともκ₁+M₀を配分する必要がある。`ng8:annular-protection-obstruction` と `ng8:interior-area-cut-obstruction` は、総量と個別margin、又は両端の正配分だけでは不十分な実面積模型を与える。Actual KE族に所定の障害が生じることを証明した例ではない。

`ng8:p0-source-protected-reduction` は各sourceを通るregular closed leafの選んだ飽和annulusを保持し、その逆像にfull compact pinched torusと飽和近傍を含める。外側のreductionはμ=0を跨いでsmoothである。`ng8:p0-small-area-flexibility` ではend collarsとこれらのannuliがcritical leavesを避けるためincidence graphが連結となり、元の正配分の周りで小さい総和零のsmooth増分をspanning-tree flowで実現する。増分を両端で零とすればsource全近傍・canonical moment・normal circle・marked tree・whole-fiber overlapsを保つ。Sourceを含むprotected massがnonsmoothでもよい。これは局所的な自由度であり、所定の大targetまで反復できることや、全区間で切片を直線化できることは示さない。

### Actual anchorからcore action chartへの条件

周期1のnormal cycleを用い、actual invariant primitiveのperiodをM_a=q_a−ρ_a、anchorをq_a=δ_a<ρ_aとする。`ke:anchor-liouville-actions` により、anchorのcritical period AはLiouville filling上で
\[
I_\beta(q_a)=\frac{A}{\delta_a-\rho_a}(q_a-\rho_a)
\]
となる。同じprimitive/frameのneck直線c+pq_aとの一致にはA=p(δ_a−ρ_a)、c=−pρ_aが必要十分である。Neckとのclosed primitive差のperiod κ、cycleの符号εと整数shear kを用いる場合はp=k+εA/(δ_a−ρ_a)、c+ρ_a(p−k)=εκとなる。Exactなprimitive補正は固定cycleのperiodを変えない。元のcanonical circleとの厳密一致は共通collarでの主張であり、全coreへの元のcircle actionの延長を主張しない。

`ke:actual-anchor-fan-criterion` は、五次では有向四角形fに対しcritical meridian periodsを−M_a·1_{b=f(a)}、六次Petersenではexternal periodsを0、internal annulusの端periodsを0と−M_aにする十分条件を与える。Actual annulusのStokes単調性とcornerの負のmeridian periodsから、既存のunimodular face matricesの係数の正値性が従う。Liouville homogeneityでcore値の近傍へchartを延ばし、各branch starのnormal actionもambient integer affineとなる。同じdomain・skeleton・等方的strata・保持cap葉を保ち、比例曲率模型への移植を新たに仮定しない。

`ke:anchor-stokes-budget` は、実際のclutching Σ[β_b]=−[α]を入力とし、normal period M<0とpuncture reference periods c_bに対してArea(P)=−Σc_b−Mを示す。非閉primitiveをhomology関係へ直接積分せず、global sectionと整数windingからStokesを適用する。K4のbasin areas A_b−c_b、Petersenのexternal areas−c_bとinternal area−Mは総量と一致する。保持集合がend collarsだけで内側境界periodも負ならmarginを得るが、追加source annuliには上の有限輸送条件が要る。

比A/(δ_a−ρ_a)が無理数なら、その固定Liouville fillingのbranchを有理作用方向へ変える整数座標変換はない。これもatlas候補全体の不存在ではない。五次の `ke:k4-actual-end-anchor` は、全K2交わりを含むend collarsのみを保持し、source全飽和近傍をδ決定後に $|\widehat\mu_N|<\delta/2$ へ選ぶ標準P0選択で、$Q_{ab}=\nu_b-\rho_b< -\rho_b/2$ と同じactual meridiansの $\sum_{b\ne a}[\beta_{ab}]=-[\alpha_a]$ を確認する。三basinの全strict marginが正なので、元のmarked relative class内で任意有向四角形のtargetsを実現し、同一coreの局所K4 chartを得る。大きいanchor isotopyをmoment cutoffで先に入れ、その後で同じanchorを共有する二族にsmall interpolationを用いることで、有限非零bandで元neckへ戻せる。この局所系を全neckへ接続する有限period条件と全moment構成は次節にまとめる。追加のanchor保持annuliや先指定した大source近傍は一般のprotected-period判定で別に扱う。数学的正本は曲面repoであり、有限輸送・Moser・Stokes・GH移送・cone extensionの一般原理を独自成果とは扱わない。

## 五次の両端period・全moment・同じπのatlas/GH

現行曲面稿の `ke:k4-actual-neck-periods` を正本とする。正weightsのrow sumsを1とし、ρ_ij=2πw_ij、x_i;jk=1_{k=f_i(j)}と置く。実際の両端affine critical periodsの整合は
\[
n_{ij;k}=1+x_{i;jk}+x_{j;ik},\qquad
\rho_{i,k}+x_{i;jk}\rho_{i,j}=\rho_{j,k}+x_{j;ik}\rho_{j,i}
\]
と必要十分に同値である。共通neck primitiveとの差はκ_i;k=χ_k+ρ_i,k、κ_j;k=χ_k+ρ_j,kで、Σχ=−2π。K2 endのshearは−1、sourceを含むcritical境界のshearはn_k−1である。Normal O(1)の正meridiansを同じ実同定で運び、閉差にだけclutchingを適用する。Source windingはbasin disk上で実normal bundlesを自明化して計算する。独立primitiveの自由な定数変更で整合させない。

等重み1/4ではf_i(j)=f_j(i)が必要十分となり、六つの対称四角形系と(3,1,1) allocationを使える。`ke:k4-cyclic-weight-periods` は有向5cycleのsuccessor sと正a_i、Σa_i=1からw_i,j=a_j+a_i 1_{j=s(i)}を取り、隣接pairは(3,1,1)、非隣接pairは(2,2,1)となるcompatible非対称族を与える。全cycle系の新しい分類は主張しない。Source identities・basin・順序・relative classは初期に選び、full source neighborhoods固定後には変えない。

`ng8:quintic-full-moment` では、共通左frameのJ_k=χ_k+ρ_i,k+x_iρ_i,j−x_iμに対する面積要求をa_k=ρ_i,k+x_iρ_i,j−x_iμ−ν_k(μ)+n_k min(μ,0)とする。全量は−ΣR_k−μ+5min(μ,0)で、ΣJ_k=−μから一致する。K2全momentの|ν_k|≤C/b_jにより正marginを得る。Analytic cutsとP_jを先に固定し、その内部のrooted-tree neighborhoodsで初期source葉の全tailをDini一様に小さくしてから飽和annuliを固定する。Targetとprotected massの同じsource wallを引いた自由需要はsmoothで、三つのexternal-basin strict cutsが成分別相対Moserを可能にする。

Thin葉はsource同定S_tとend補正Dの引戻し座標で選び、その像を用いる。S_tが新しいannuliを集合として固定することや、sourceの全円葉がDの支持外にあることは要求しない。Saddleは先に確保した内側小円板へ置き、sourceとsaddleの点近傍ではDが恒等なので、固定tで必要な局所葉はμに依存しない。S_t・D、core primitive・domain、clipped-depth mapは葉の形と独立に先に定まる。Reference foliationからの表示には同じmarked classのμ非依存H_{j,t}を前合成すればよく、そのC^k定数を仮定しない。Connector boundsはP_jの全同一moment集合に対するため、thin widthsの選択後にGH定数又は追加t閾値を持ち込まない。

最後のfree bandでは、同じanchorを持つLiouville/neck二族のmarked interpolation後に、同じtarget面積へのMoserを再実行する。両open germsは既にtargetを持ち、有限source sectionsのfirst jetsも固定する。中央full nodal neighborhoodsと全K2 partitionsを保ち、全開collarで作用と全葉を一致させる。通常P0と作用指定構成を同じ初期葉から別々に作るので、既固定のP0のsource fibersを無断で取り替えない。固定Tと解析的接続予算は保たれ、葉の一様微分評価は不要である。

`ke:quintic-simultaneous-realization` は、この構成からrelative-replacementの四条件・whole-fiber閉商・denominator 1のbranch charts・整数star transitionsを確認し、各tの同じactual πの大域作用atlasとf=p_Tπの全域ambient歪み消失を得る。Raw periodsはcore/branchとも一斉に2πで割ってatlas規約へ換算する。Focus値は通常chartから除き穿孔近傍のactual affine構造を保つ。

全平行移動を含む接続の正本は `ke:eq:quintic-branch-action-coordinates`、`ke:eq:quintic-core-branch-extension`、`ke:eq:quintic-affine-full-transition`。二重線ijに対しy_k=1_{f_i(k)=j}、y'_k=1_{f_j(k)=i}、core face座標を(s,ζ)、(s',ζ')とすると
\[
\zeta'=\zeta,\qquad
s'=-s+(y_k+y'_k)\zeta+w_{i,j}+w_{j,i}.
\]
三面の平行移動は同じ(w_i,j+w_j,i)r_jiである。各四角形のpredecessorの一意性Σy=Σy'=1がK4のrelationを保ち、線形部分はGL(3,Z)に属する。共通χの相殺には同じneck primitiveを使い、非対称な正weightsにも成立する。Normal covectorはprimitiveで、枝の分母は1。計算は既に一致する全open collarsの実際の葉と作用を入力とする。

各tで同じ射影に二つの性質を持たせる主張であり、作用atlasのt方向の収束、極限基底のintegral affine構造、d_□の作用座標に関するHessian・Monge–Ampère性は結論しない。任意先指定の大source tailsではtarget>Lが破れ得るため別に有限cut判定を要する。t方向の連続性・速度も含まない。六次Petersenの同時実現はinternal annuliの二端cuts、actual periodsと全overlapsが未解決である。

Actual period命題、全moment定理・統合定理と指定依存の独立内部点検を保持する。作用atlasの指定点検ではqone・gluing・actual-anchor・endpointから平行移動付き式を逆向きに読み、主担当も別に式を確認した。Source-free限定とthin葉・解析定数の量化は曲面側の対象限定監査として同期済みである。この範囲で新たなgapは認めなかったが、一般成分別面積定理・P0全体・外部解析原著の全面再監査、形式証明、外部査読、網羅的新規性確認とは区別する。

## 曲面の全移動基点と選択した中間尺度

曲面repoの `topo:component-cone-germ` は、成分頂点e_iの半径0<r<1/2の閉球がC_{2,d−1}の同半径球とambient距離で等長であることを示す。`topo:cubical-local-models` は全target点を次の四型に分類する。

| targetの中心 | 局所模型 |
| --- | --- |
| 成分頂点e_i | C_{2,d−1} |
| Support二元、e_i+e_jを含む | R×Y_{d−2}。Y_mは原点で貼ったm本の半直線 |
| e_i+e_j+e_k | 全角3π/2のEuclidean cone K_{3π/2} |
| 残るsupport三元の点 | R² |

`topo:cubical-moving-blowups` は任意のλ_ν→∞とtarget移動基点に対する全部分列極限を、これらの空間の任意の有限基点として記述し、任意のλ_νで全型を実現する。Bookのspine方向は平行移動で除ける。固定局所球のfull-ambient等長を使い、成分錐から逃げる基点はpositive-starを出る経路の2(m_ν−A)>2Aという費用でbook又は平面へ分類する。角3π/2の錐から逃げる場合は平面となる。閉star全体のambient積を仮定せず、標準的な有限cone幾何の新規性を主張しない。

`ke:distortion-to-pointed-balls` は、compact geodesic spaces間の全射Fの歪みがδ以下なら、任意の中心x・同じ半径Aのambient閉球の間に、基点対を含む歪み3δ以下の対応を与える。従って基点付きGH距離は3δ/2以下である。全射の逆像が球からはみ出す分をsource最短路で戻すため、F自体が球から同半径球への全射である必要はない。

正規化global distortionをε_t=dis(f_t)と置く。同じf=p_Tπについて `ke:intermediate-moving-classification` は
\[
a_t\to\infty,\qquad a_t/R_t\to0,\qquad R_t\varepsilon_t/a_t\to0
\]
の下で、任意のt_ν→0とx_ν∈X_{t_ν}のpointed GH部分列極限を上の四型に分類する。λ_t=R_t/a_t、δ_t=λ_tε_tとすれば、actual曲面と拡大targetの同半径閉球を全中心に一様に3δ_t/2で比較できる。任意の許容尺度と退化列でtarget基点を選び、f_tの任意の逆像を取ると各型を実現する。a_t=R_t√(ε_t+1/R_t)は一つの許容尺度である。速度を評価していないε_tの条件を除いた任意の中間尺度、tensor収束、標識の復元、二つの極限の交換は結論しない。

既存の `ke:intermediate-component-cone` も保持する。一般に $\eta_t=\sup_{y\in A_t}d_\square(f_t(y),e_i)\to0$ なら、$R_t(\varepsilon_t+\eta_t)/a_t\to0$ により全基点 $y_t\in A_t$ に一様な成分錐を得る。同じfibrationのcomponent coreと変更collarの合併には $\eta_t\le Cq_t$、$q_t=(1+\log(N_{j(t)}+1))/R_t\to0$ を使い、$a_t=R_t\sqrt{\varepsilon_t+q_t}$ を選べる。これらはsurface側の同じglobal mapからの帰結であり、Part Iの固定空間の極限を族一様に読み替える証明ではない。

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

