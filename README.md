# Multiscale Kähler–Einstein geometry

固定配置補空間の多重尺度KE幾何。現行研究一式：2026-11-22 / v1.13（Part I v1.7、総説v1.11）。最初に[研究方針](00_research_plan.md)を読む。主たる公表用原稿は `papers/multiscale-kaehler-einstein.tex`。

**公表計画：** 数学的価値の最大化を基準に、曲面P0・Part IVの最小局所解析・Part Iの距離と実球体積漸近を優先する。[研究方針](00_research_plan.md)に実行順序・達成基準・担当を記した。まず中心定理の構成、入力の範囲、先行研究との差を確定し、同時atlasと条件付き拡張は独立した完成基準で進める。

**三研究の共同編集：** 本repoは固定補空間のPart I–IIIと総説、[kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration)は退化族の局所一様解析Part IVと条件付き大域枠組Part V、[surface-lagrangian-torus-fibration](https://github.com/uedakazushi/surface-lagrangian-torus-fibration)はactual曲面fibrationと同じ射影による全域GH実現を担当する。方針・記法・定理の依存関係・監査は一体で進め、repoと独立論文は役割別に保つ。詳細の定理ラベル・入力条件・確認版は[研究ノート](research/notes.md)に置く。

| 原稿 | 頁数 | 状態 |
| --- | ---: | --- |
| [Part I](papers/multiscale-kaehler-einstein.tex) | 67 | 距離錐・移動基点・metric link、LDP・裾漸近、測度付き平行移動、面質量、一様Mellin recursion |
| [Part II](papers/secondary-periods-torelli.tex) | 28 | 一般WP completionはcontrolled push-off付き |
| [Part III](papers/conifold-localization.tex) | 57 | Actual localization/pGHは(H_loc)+(H_anc)付き |
| [総説](papers/series-overview.tex) | 16 | 五篇と曲面実現の共同方針、有限面積輸送とcore接続、相対変更のGH安定性、全移動基点の中間尺度 |
| [研究素材](papers/research-directions.tex) | 10 | Jacobi/scattering・一般matroid等。現行仮定の注意を付記 |

**公表準備で具体化した成果：** `cor:tail-intrinsic-uniform` により実球裾係数Wは内在量で、KE規格化ではlog Wが1-Lipschitz、裾漸近が任意のcompact基点集合上で一様となる。許されるnorm変更での不変性とdepth定数shiftの補償を区別した。非KE回転cuspの明示例では非可積分なo(1)誤差からR^a因子が現れ、coneとleading normal massだけでは実球裾係数を決められない。五直線のK5 linkのconeが非CAT(0)であることも証明し、Leuzingerの局所対称coneと具体的に比較した。これら四項は担当と別担当が証明を読んで点検した。

**現行の数学的到達点：** Part Iでは、固定SNCの整合的カラー・Ξ延長比較・全残余一様tensor評価に加え、co-Gramから全射な距離収縮への証明を点検した。加法誤差をKとすると、対応する中心を持つ閉球のGH誤差は全中心・全半径に一様に3K/(2R)以下となる。指定compact集合を原点へ送る選択も可能で、この場合Kはその集合に依存する。

体積LDPの下界はfull face collarのcompact残余集合からambient open setへ入れる形で証明し、exact-supportだけへの制限測度の正質量を要求しない。Busemann→exact tail→joint lawは一面の計量・体積比較と距離上界から直接閉じる形に整理した。一般重みの角分布は最小entropyを持つverticesの重み総和で正規化する。これらは限定的な内部証明点検を伴う固定空間の結果であり、全Part Iの独立検証・退化族の一様評価・網羅的新規性確認の完了を意味しない。

**移動基点とlink：** Component incidencesを保つ正のface領域を用い、壁までの距離が2Aを超える閉A球でambient距離の積同定を証明した。これにより全moving-basepoint極限とその実現を記述する。閉star全体の短絡・境界同一視の障害はノートへ置く。Linkは非連結の場合も含めてmetric isometry typeを復元し、divisor labelsやdepth規格化、genuine geodesic-ray boundaryの復元とは区別する。Leuzingerの有界加法誤差・radial公式と、Bridson–Haefligerの標準cone復元を一次資料で確認し、Introductionの貢献範囲を明確化した。

**測度側の精密化：** 任意のnormal深さ列の最小値が無限大へ向かうとき、全残余空間を含むbounded normal strip上の全変動収束を証明する。通常のvolume-IRFAとmetric-IRFAで各ambient閉球の測度付きGH収束まで従い、smooth volume-IRFAは不要である。面質量の交点数公式は滑らかな基準曲率との直接Stokes計算で示し、normal circleの周期2πと全体積の階乗係数を確認した。全deeper faceの体積評価から残余指数momentsを一様に抑え、一様Abel–Mellin recursionの追加weighted-dominator仮定も不要にした。同じ評価はactual residual measuresの逃避を直接制御し、厳密な裾漸近・joint law・距離Laplace変換も通常の全face volume-IRFAで成立する。面の包含関係はmixed localized transformsから検出し、単独のface mass一覧からは結論しない。

Smooth divisorに限るRochon–ZhangのTheorems 7.4・7.6と、滑らかな次数e超曲面のlog共鳴係数・可積分tailは既存の有効な結果として保持する。

**曲面正本との接続：** [現行曲面稿（改訂39）](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/tree/main)は、同じ全射 $f_t=p_T\pi_t$ の正規化歪みを $\varepsilon_t$ として、$a_t\to\infty$、$a_t/R_t\to0$、$R_t\varepsilon_t/a_t\to0$ の下で全移動基点の中間尺度極限を分類する。型は成分錐 $C_{2,d-1}$、book $\mathbb R\times\mathcal Y_{d-2}$、全角 $3\pi/2$ の錐、平面で、対応する任意の有限基点を許す。$\mathcal Y_m$ は原点で貼ったm本の半直線。全射の歪みが $\delta$ 以下なら、対応する中心・同じ半径のambient閉球の基点付きGH距離は $3\delta/2$ 以下である。これにより任意の許容尺度・退化列で全型を実現できる。誤差条件を除いた任意の中間尺度やtensor収束は結論しない。

曲面側のsource-inclusive固定shellは、sourceを含む固定残余compactと半径rを先に固定し、全複素parameterの小さいtで同じ正則体積frameのmomentとshell横断費用を制御する。Co-Gram下界の補題は固定parameterの有限不等式として扱い、誤差消失は最後のslow diagonalで用いる。同じfの全域上界・下界と有限targetの指定鎖を共同点検した範囲、core・変更collarの任意基点への適用、証明の正本は[研究ノート](research/notes.md)を参照する。標準的な局所錐幾何やGH移送の一般原理を新規成果とは扱わない。

**同じfibrationの相対変更：** 曲面の `ke:moment-relative-replacement` は、同じcanonical normal moment・anchor cuts・保持cornerの全葉・source nodal neighborhoods・component領域と、実際のmarked product/cone商・全交わりのwhole-fiber partitionを保つ候補変更に対し、射影値の差を $C(1+\log(N_j+1))/R_t$ 以下に抑える。Reduced diffeomorphismの $C^1$ 小ささは不要であり、固定木系の候補がslow diagonalに沿って構成できれば同じ新しい射影のGH実現を得る。作用適合atlasを持つ候補の実構成は未解決である。Raw momentの $o(1)$ だけではprofile値を制御できない例と、fixed-fiber free-bandのStokes面積式・sourceを横切る模型 $\pi(c-|\mu|)$ の折れを、曲面正本への参照とともに[ノート](research/notes.md)へ置く。

FBPのTheorem 6.14(b)は部分fibration、(c)はproperな場合の全fiberの構成Kähler計量によるGH収束である。選択部分複体、admissible path、直径正規化を一次本文で照合し、actual負KE計量との比較を総説で明確化した。Evans–MauriとChakravarthy–Gromanの指定箇所も確認したが、全原著の再検証や網羅的新規性調査の完了とはしない。確認範囲は[一次資料の監査](research/source-audit.md)に集約する。

**相対構成の具体的な進展：** 保存する領域Kの補集合が分断される場合、critical-region面積の指定は、regionと可動成分のincidence上の正行列が指定row/column sumsを持つことと同値になる。成分別総量とstrict cut条件で判定でき、総量・各regionの余裕・両端の確認だけでは足りない例もある。Actual P0ではsourceの全nodal neighborhoodsを固定した小さい総和零の面積変更を実現できる。さらにanchorの有限period条件から、actual Liouville fillingに五次のK4／六次のPetersen作用chartを与える十分条件を得た。`ke:k4-protected-anchor-selection` は同系の仮定を満たす保持end collarsと飽和annuliに対する有限判定を与える。改訂39の `ke:k4-actual-end-anchor` では、標準P0のanchor上で全K2交わりを含むend collarsだけを保持し、sourceの全飽和近傍をanchor決定後の $|\widehat\mu_N|<\delta/2$ に選ぶ場合、actual protected periodsの負値性とmeridian clutchingを証明した。従って任意の有向四角形について同じactual domain・primitive・skeletonに局所K4 chartを構成し、有限の非零moment bandで元neckへ復帰できる。Sourceを跨ぐ全momentの作用条件、両端の切片・整数shear、全域作用atlasの全overlap整合は未解決である。同じπでのatlas/GHの完成とはしない。証明は曲面正本に保持し、有限輸送・Moser・cone extensionの一般原理の新規性は主張しない。

**公表用の仮定と正規化：** Part I v1.7はIntroductionの各結論を本文の入力・証明へ対応させ、測度平行移動の基点条件と残余parameterのcompact subcritical範囲を明示する。面質量は非正規化KE体積に対する交点数であり、確率正規化時の交点数比も記す。通常のvolume-IRFAでAbel係数が存在しても有理型延長が従わない具体例を、証明付きで主稿へ統合した。Kobayashi・Guenancia–Wu・Jiang–Shiの適用範囲と、Chambert-Loir–Tschinkelの既存Igusa/residue theoryとの比較を加えた。網羅的新規性の確認は未了である。

Part II v2.1では、複素periodに必要なfactor/cusp labelsとKähler orientationを明記し、Part Iの測度付き平行移動への参照を定理ラベルに揃えた。Fully markedな全curve factorsで向きだけを忘れるgeneric Torelliは、配置全体の複素共役までの結論である。今回の点検はこの接続の範囲であり、Part IIの全証明再監査ではない。

三repoの照合では、五次の(CP)をPart IVから得る経路に(TC)が必要で、Part Vのactual直径帰結には(CP)＋(PBE)が必要なことを総説へ反映した。曲面側の直接scalar/portal経路はこれらのpackage自体を検証しない。Part Iの接続は同じfiberの端点をambient空間内で結ぶものであり、fiber内の長さ評価と区別した。固定成分は $d-1$ 本の直線の補空間であり、固定補空間のblow-downを退化族の一様比較へ読み替えない。

最初に[研究方針](00_research_plan.md)、次に[研究ノート](research/notes.md)を読む。[移行・検証範囲](research/migration.md)と[ソース対応](research/source-manifest.json)を確認する。短い再構成稿は全文へ置換済み。旧稿独自資産の網羅的照合は残る。

ルートで `latexmk`。PDF/SyncTeXはbuild/。現行の[検証状態](research/validation.json)で数学的点検・組版・表示確認を分ける。正本はmain。[research-hub](https://github.com/uedakazushi/research-hub)。

組版にはLuaLaTeX/latexmk、LuaTeX-ja（ltjsarticleとHaranoAjiフォント）、TikZ、AMS、mathrsfs等の原稿で指定した標準TeXパッケージが必要。lualatex.fmtとrsfsのフォントmapが有効なTeX環境で上記コマンドを実行する。現行研究一式v1.13では総説v1.11を16頁に再組版した。Part I v1.7（67頁）は本文を変更せず、同日の成功組版と表示確認の記録を保持する。Part Iの1–11・44・45・56・57・66・67頁、総説の1–4・8–10・15–16頁を約150dpiで実際に表示確認し、欠け・重なり・欠字を認めなかった。両原稿の未解決参照・引用、重複label、missing character、overfull/underfull、LaTeX errorは0。字体サイズの代替等の軽微な警告は残る。新しい裾係数・gauge・cusp例・K5比較は別担当も独立に証明を読んだ。これは全頁の視覚検査や全稿の独立数学監査ではない。Part II–IIIと研究素材は今回変更・再組版していない。各確認日・hash・実施範囲は[検証状態](research/validation.json)を参照する。
