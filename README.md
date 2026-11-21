# Multiscale Kähler–Einstein geometry

固定配置補空間の多重尺度KE幾何。現行研究一式：2026-11-22 / v1.5（Part I v1.4）。最初に[研究方針](00_research_plan.md)を読む。主たる公表用原稿は `papers/multiscale-kaehler-einstein.tex`。

**三研究の共同編集：** 本repoは固定補空間のPart I–IIIと総説、[kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration)は退化族の局所一様解析Part IVと条件付き大域枠組Part V、[surface-lagrangian-torus-fibration](https://github.com/uedakazushi/surface-lagrangian-torus-fibration)はactual曲面fibrationと同じ射影による全域GH実現を担当する。方針・記法・定理の依存関係・監査は一体で進め、repoと独立論文は役割別に保つ。詳細の定理ラベル・入力条件・確認版は[研究ノート](research/notes.md)に置く。

| 原稿 | 頁数 | 状態 |
| --- | ---: | --- |
| [Part I](papers/multiscale-kaehler-einstein.tex) | 57 | 距離錐・LDP・裾漸近、測度付き平行移動、面質量、一様Mellin recursion |
| [Part II](papers/secondary-periods-torelli.tex) | 28 | 一般WP completionはcontrolled push-off付き |
| [Part III](papers/conifold-localization.tex) | 57 | Actual localization/pGHは(H_loc)+(H_anc)付き |
| [総説](papers/series-overview.tex) | 11 | 五篇と曲面実現の共同方針、定理の条件・正規化 |
| [研究素材](papers/research-directions.tex) | 10 | Jacobi/scattering・一般matroid等。現行仮定の注意を付記 |

**現行の数学的到達点：** Part Iでは、固定SNCの整合的カラー・Ξ延長比較・全残余一様tensor評価に加え、co-Gramから全射な距離収縮への証明を点検した。加法誤差をKとすると、対応する中心を持つ閉球のGH誤差は全中心・全半径に一様に3K/(2R)以下となる。指定compact集合を原点へ送る選択も可能で、この場合Kはその集合に依存する。

体積LDPの下界はfull face collarのcompact残余集合からambient open setへ入れる形で証明し、exact-supportだけへの制限測度の正質量を要求しない。Busemann→exact tail→joint lawは一面の計量・体積比較と距離上界から直接閉じる形に整理した。一般重みの角分布は最小entropyを持つverticesの重み総和で正規化する。これらは限定的な内部証明点検を伴う固定空間の結果であり、全Part Iの独立検証・退化族の一様評価・網羅的新規性確認の完了を意味しない。

**測度側の精密化：** 任意のnormal深さ列の最小値が無限大へ向かうとき、全残余空間を含むbounded normal strip上の全変動収束を証明する。通常のvolume-IRFAとmetric-IRFAで各ambient閉球の測度付きGH収束まで従い、smooth volume-IRFAは不要である。面質量の交点数公式は滑らかな基準曲率との直接Stokes計算で示し、normal circleの周期2πと全体積の階乗係数を確認した。全deeper faceの体積評価から残余指数momentsを一様に抑え、一様Abel–Mellin recursionの追加weighted-dominator仮定も不要にした。同じ評価はactual residual measuresの逃避を直接制御し、厳密な裾漸近・joint law・距離Laplace変換も通常の全face volume-IRFAで成立する。面の包含関係はmixed localized transformsから検出し、単独のface mass一覧からは結論しない。

Smooth divisorに限るRochon–ZhangのTheorems 7.4・7.6と、滑らかな次数e超曲面のlog共鳴係数・可積分tailは既存の有効な結果として保持する。曲面側の選択した中間尺度は、同じglobal写像の歪みと基点のtarget変位に条件を課すことで、component core・変更collar内の全基点に一様となる。詳細の定理ラベルと未点検範囲は[研究ノート](research/notes.md)を参照。

三repoの照合では、五次の(CP)をPart IVから得る経路に(TC)が必要で、Part Vのactual直径帰結には(CP)＋(PBE)が必要なことを総説へ反映した。曲面側の直接scalar/portal経路はこれらのpackage自体を検証しない。Part Iの接続は同じfiberの端点をambient空間内で結ぶものであり、fiber内の長さ評価と区別した。固定成分は $d-1$ 本の直線の補空間であり、固定補空間のblow-downを退化族の一様比較へ読み替えない。

最初に[研究方針](00_research_plan.md)、次に[研究ノート](research/notes.md)を読む。[移行・検証範囲](research/migration.md)と[ソース対応](research/source-manifest.json)を確認する。短い再構成稿は全文へ置換済み。旧稿独自資産の網羅的照合は残る。

ルートで `latexmk`。PDF/SyncTeXはbuild/。現行の[検証状態](research/validation.json)で数学的点検・組版・表示確認を分ける。正本はmain。[research-hub](https://github.com/uedakazushi/research-hub)。

組版にはLuaLaTeX/latexmk、LuaTeX-ja（ltjsarticleとHaranoAjiフォント）、TikZ、AMS、mathrsfs等の原稿で指定した標準TeXパッケージが必要。lualatex.fmtとrsfsのフォントmapが有効なTeX環境で上記コマンドを実行する。変更した2稿の再組版・表示確認の状態と、変更していない3稿の既存検証記録は区別する。
