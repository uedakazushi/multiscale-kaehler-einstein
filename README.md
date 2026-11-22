# Multiscale Kähler–Einstein geometry

固定配置補空間の多重尺度KE幾何。現行研究一式：2026-11-22 / v1.16（Part I v1.8、総説v1.12）。最初に[研究方針](00_research_plan.md)を読む。主たる公表用原稿は `papers/multiscale-kaehler-einstein.tex`。

**公表計画：** 数学的価値の最大化を基準に、曲面P0・Part IVの最小局所解析・Part Iの距離と実球体積漸近を優先する。[研究方針](00_research_plan.md)に実行順序・達成基準・担当を記した。まず中心定理の構成、入力の範囲、先行研究との差を確定し、五次の同時atlas/GHを中心成果へ統合し、六次と条件付き解析の拡張は独立した完成基準で進める。

**三研究の共同編集：** 本repoは固定補空間のPart I–IIIと総説、[kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration)は退化族の局所一様解析Part IVと条件付き大域枠組Part V、[surface-lagrangian-torus-fibration](https://github.com/uedakazushi/surface-lagrangian-torus-fibration)はactual曲面fibrationと同じ射影による全域GH実現を担当する。方針・記法・定理の依存関係・監査は一体で進め、repoと独立論文は役割別に保つ。詳細の定理ラベル・入力条件・確認版は[研究ノート](research/notes.md)に置く。

| 原稿 | 頁数 | 状態 |
| --- | ---: | --- |
| [Part I](papers/multiscale-kaehler-einstein.tex) | 69 | 距離錐・測度漸近・一様Mellin recursion、KE積の実球裾の二次項と距離Laplace変換の対数発散 |
| [Part II](papers/secondary-periods-torelli.tex) | 28 | 一般WP completionはcontrolled push-off付き |
| [Part III](papers/conifold-localization.tex) | 57 | Actual localization/pGHは(H_loc)+(H_anc)付き |
| [総説](papers/series-overview.tex) | 18 | 五篇と曲面実現の共同方針、五次の同一πによる作用atlas/GH、有限面積輸送、全移動基点の中間尺度 |
| [研究素材](papers/research-directions.tex) | 10 | Jacobi/scattering・一般matroid等。現行仮定の注意を付記 |

**公表準備で具体化した成果：** `cor:tail-intrinsic-uniform` により実球裾係数Wは内在量で、KE規格化ではlog Wが1-Lipschitz、裾漸近が任意のcompact基点集合上で一様となる。許されるnorm変更での不変性とdepth定数shiftの補償を区別した。非KE回転cuspの明示例では非可積分なo(1)誤差からR^a因子が現れ、coneとleading normal massだけでは実球裾係数を決められない。五直線のK5 linkのconeが非CAT(0)であることも証明し、Leuzingerの局所対称coneと具体的に比較した。これら四項は担当と別担当が証明を読んで点検した。

**KE積に残る実距離の対数項：** `lem:hyperbolic-curve-tail` と `ex:KE-product-distance-log` は有限面積双曲曲線Sとコンパクト双曲曲線Yの積で、実球裾をe^−R(W+C/R+O(R^−2))、距離Laplace変換をW/ε+C log(1/ε)+O(1)（ε=1−s↓0）と計算する。CはSの裾係数とYの距離二乗積分の積の半分で正である。Normal densityが厳密な積型でも、実距離変換は臨界点近傍へ有理型に延長できず、実球の誤差を指数的に改善することも一般にはできない。深さ変数のMellin変換はこの例で有理型である。指定証明の内部点検とHaas・Chambert-Loir–Tschinkel・Grieserの一次資料照合を行ったが、slit domainへの解析接続やこの例の優先権は主張しない。

**現行の数学的到達点：** Part Iでは、固定SNCの整合的カラー・Ξ延長比較・全残余一様tensor評価に加え、co-Gramから全射な距離収縮への証明を点検した。加法誤差をKとすると、対応する中心を持つ閉球のGH誤差は全中心・全半径に一様に3K/(2R)以下となる。指定compact集合を原点へ送る選択も可能で、この場合Kはその集合に依存する。

体積LDPの下界はfull face collarのcompact残余集合からambient open setへ入れる形で証明し、exact-supportだけへの制限測度の正質量を要求しない。Busemann→exact tail→joint lawは一面の計量・体積比較と距離上界から直接閉じる形に整理した。一般重みの角分布は最小entropyを持つverticesの重み総和で正規化する。これらは限定的な内部証明点検を伴う固定空間の結果であり、全Part Iの独立検証・退化族の一様評価・網羅的新規性確認の完了を意味しない。

**移動基点とlink：** Component incidencesを保つ正のface領域を用い、壁までの距離が2Aを超える閉A球でambient距離の積同定を証明した。これにより全moving-basepoint極限とその実現を記述する。閉star全体の短絡・境界同一視の障害はノートへ置く。Linkは非連結の場合も含めてmetric isometry typeを復元し、divisor labelsやdepth規格化、genuine geodesic-ray boundaryの復元とは区別する。Leuzingerの有界加法誤差・radial公式と、Bridson–Haefligerの標準cone復元を一次資料で確認し、Introductionの貢献範囲を明確化した。

**測度側の精密化：** 任意のnormal深さ列の最小値が無限大へ向かうとき、全残余空間を含むbounded normal strip上の全変動収束を証明する。通常のvolume-IRFAとmetric-IRFAで各ambient閉球の測度付きGH収束まで従い、smooth volume-IRFAは不要である。面質量の交点数公式は滑らかな基準曲率との直接Stokes計算で示し、normal circleの周期2πと全体積の階乗係数を確認した。全deeper faceの体積評価から残余指数momentsを一様に抑え、一様Abel–Mellin recursionの追加weighted-dominator仮定も不要にした。同じ評価はactual residual measuresの逃避を直接制御し、厳密な裾漸近・joint law・距離Laplace変換も通常の全face volume-IRFAで成立する。面の包含関係はmixed localized transformsから検出し、単独のface mass一覧からは結論しない。

Smooth divisorに限るRochon–ZhangのTheorems 7.4・7.6と、滑らかな次数e超曲面のlog共鳴係数・可積分tailは既存の有効な結果として保持する。

**曲面正本との接続：** [現行曲面稿（改訂43・数学確認commit 102ae9a）](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/tree/102ae9a382406bcd14755c216d2bc0ca8bc84321)は、同じ全射 $f_t=p_T\pi_t$ の正規化歪みを $\varepsilon_t$ として、$a_t\to\infty$、$a_t/R_t\to0$、$R_t\varepsilon_t/a_t\to0$ の下で全移動基点の中間尺度極限を分類する。型は成分錐 $C_{2,d-1}$、book $\mathbb R\times\mathcal Y_{d-2}$、全角 $3\pi/2$ の錐、平面で、対応する任意の有限基点を許す。$\mathcal Y_m$ は原点で貼ったm本の半直線。全射の歪みが $\delta$ 以下なら、対応する中心・同じ半径のambient閉球の基点付きGH距離は $3\delta/2$ 以下である。これにより任意の許容尺度・退化列で全型を実現できる。誤差条件を除いた任意の中間尺度やtensor収束は結論しない。

`ke:global-volume-measure` は全固定d≥5で、同じfとπによる正規化KE体積の押出しが各成分頂点に質量1/dを置く原子測度へ収束することを示す。Part Iの固定成分の体積公式、全体積の一致、固定compact収束とexhaustionから得られ、moving neckの体積漸近や追加速度は要しない。GH極限の辺・squareは距離として残るが、極限測度は頂点に集中する。全台性を要求しないcompact measured GHの意味での結論であり、五次の同じ作用atlas/GH射影にも適用する。

曲面側のsource-inclusive固定shellは、sourceを含む固定残余compactと半径rを先に固定し、全複素parameterの小さいtで同じ正則体積frameのmomentとshell横断費用を制御する。Co-Gram下界の補題は固定parameterの有限不等式として扱い、誤差消失は最後のslow diagonalで用いる。同じfの全域上界・下界と有限targetの指定鎖を共同点検した範囲、core・変更collarの任意基点への適用、証明の正本は[研究ノート](research/notes.md)を参照する。標準的な局所錐幾何やGH移送の一般原理を新規成果とは扱わない。

**同じfibrationの相対変更：** 曲面の `ke:moment-relative-replacement` は、同じcanonical normal moment・anchor cuts・保持cornerの全葉・source nodal neighborhoods・component領域と、実際のmarked product/cone商・全交わりのwhole-fiber partitionを保つ候補変更に対し、射影値の差を $C(1+\log(N_j+1))/R_t$ 以下に抑える。Reduced diffeomorphismの $C^1$ 小ささは不要であり、一つの固定木系に沿うslow diagonalで同じ新しい射影のGH実現を得る。この安定性への入力となる作用atlas候補を、五次では以下の全moment構成で実現した。六次の同時実現は未解決である。Raw momentの $o(1)$ だけではprofile値を制御できない例と、source wallによる面積の折れは[ノート](research/notes.md)に保持する。

FBPのTheorem 6.14(b)は部分fibration、(c)はproperな場合の全fiberの構成Kähler計量によるGH収束である。選択部分複体、admissible path、直径正規化を一次本文で照合し、actual負KE計量との比較を総説で明確化した。Evans–MauriとChakravarthy–Gromanの指定箇所も確認したが、全原著の再検証や網羅的新規性調査の完了とはしない。確認範囲は[一次資料の監査](research/source-audit.md)に集約する。

**五次の作用atlasとGHの同時実現：** 現行曲面稿の `ke:k4-actual-neck-periods` は、同じcanonical primitiveとactual transported cyclesから両端整合をresidue weightsとsource countsの有限等式へ帰着する。`ng8:quintic-full-moment` は、解析的cuts・source同定・end補正を先に固定して初期のthin source葉を選び、wall項を含む全momentのstrict area cutsを満たす。Source-free bandの面積affine性は固定点を横切るneckへ流用しない。GH比較は全同一moment集合のconnectorと同じclipped-depth mapを使い、thin葉の幅・微分に依存する定数や追加t閾値を必要としない。Core–neckの全開collarでは同じtargetへの二段階補正で作用と全葉を合わせる。

`ke:quintic-simultaneous-realization` は各tの同じactual Lagrangian $\widehat\pi_t$ に大域matroidal atlasと $p_T\widehat\pi_t$ の全域GH実現を与える。全平行移動を含む三面共通のGL(3,Z)式を明示し、非対称な正weightsにも適用できる。等重み・対称六系・source allocation (3,1,1)は存在を保証する。Focus値には通常のmatroidal chartを要求せず穿孔近傍のactual affine構造を使う。作用atlasのt方向の収束、極限基底のintegral affine構造、cubical距離のHessian・Monge–Ampère性、任意先指定のfull source tailsを保つ相対存在、t連続性・速度は結論しない。六次Petersenの同時atlas/GHは未解決である。今回の独立内部点検は指定されたatlas接続と修正箇所に限り、一般成分別面積定理・P0全体・外部解析の全面再監査とは区別する。

**公表用の仮定と正規化：** Part I v1.8はIntroductionの各結論を本文の入力・証明へ対応させ、測度平行移動の基点条件と残余parameterのcompact subcritical範囲を明示する。面質量は非正規化KE体積に対する交点数であり、確率正規化時の交点数比も記す。通常のvolume-IRFAでAbel係数が存在しても有理型延長が従わない抽象測度の例と、actual KE積の実距離変換の例を区別する。Kobayashi・Guenancia–Wu・Jiang–Shiの適用範囲と、Chambert-Loir–Tschinkelの既存Igusa/residue theoryとの比較を加えた。網羅的新規性の確認は未了である。

Part II v2.1では、複素periodに必要なfactor/cusp labelsとKähler orientationを明記し、Part Iの測度付き平行移動への参照を定理ラベルに揃えた。Fully markedな全curve factorsで向きだけを忘れるgeneric Torelliは、配置全体の複素共役までの結論である。今回の点検はこの接続の範囲であり、Part IIの全証明再監査ではない。

Part IV v1.11（保存commit `a6cf38a`）では、capped densityのresidue規格化、Chern曲率とframe誤差の吸収予算、source軸を含む六局所型からcompact最小値原理までの下界鎖を公表用に補強し、担当が実読・別担当が変更式と量化を点検した。固定d≥5・固定族でtに一様なvolume下界であり、次数一様性や二側tensor比較は結論しない。五次の(CP)をPart IVから得る別経路には(TC)、Part Vのactual直径帰結には(CP)＋(PBE)が必要なことも保持する。曲面側の直接scalar/portal経路はこれらのpackage自体を検証しない。固定成分は $d-1$ 本の直線の補空間であり、固定補空間のblow-downを退化族の一様比較へ読み替えない。

最初に[研究方針](00_research_plan.md)、次に[研究ノート](research/notes.md)を読む。[移行・検証範囲](research/migration.md)と[ソース対応](research/source-manifest.json)を確認する。短い再構成稿は全文へ置換済み。旧稿独自資産の網羅的照合は残る。

ルートで `latexmk`。PDF/SyncTeXはbuild/。現行の[検証状態](research/validation.json)で数学的点検・組版・表示確認を分ける。正本はmain。[research-hub](https://github.com/uedakazushi/research-hub)。

組版にはLuaLaTeX/latexmk、LuaTeX-ja（ltjsarticleとHaranoAjiフォント）、TikZ、AMS、mathrsfs等の標準TeXパッケージと有効なformat/font mapが必要。Part I v1.8は69頁に組版し、主要6分類の警告・errorは零、指定10頁を150 dpiで実表示して切れ・重なり・欠字のないことを確認した。Part II v2.1（28頁）・Part III（57頁）・研究素材・総説TEXは変更しない。総説v1.12は曲面改訂41を引用する18頁のチェック済み版であり、今回のPart I追加や曲面改訂43を本文へ反映済みとはしない。これらの入力pin・組版hash・指定表示範囲と軽微な既存警告は保持する。数学的点検・組版・視覚確認・GitHub保存の各状態の正本は[検証状態](research/validation.json)とする。
