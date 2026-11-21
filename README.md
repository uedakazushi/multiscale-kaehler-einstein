# Multiscale Kähler–Einstein geometry

固定配置補空間の多重尺度KE幾何。現行研究一式：2026-11-22 / v1.3（Part I v1.2）。最初に[研究方針](00_research_plan.md)を読む。主たる公表用原稿は `papers/multiscale-kaehler-einstein.tex`。

**三研究の共同編集：** 本repoは固定補空間のPart I–IIIと総説、[kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration)は退化族の局所一様解析Part IVと条件付き大域枠組Part V、[surface-lagrangian-torus-fibration](https://github.com/uedakazushi/surface-lagrangian-torus-fibration)はactual曲面fibrationと同じ射影による全域GH実現を担当する。方針・記法・定理の依存関係・監査は一体で進め、repoと独立論文は役割別に保つ。詳細の定理ラベル・入力条件・確認版は[研究ノート](research/notes.md)に置く。

| 原稿 | 頁数 | 状態 |
| --- | ---: | --- |
| [Part I](papers/multiscale-kaehler-einstein.tex) | 46 | 固定補空間の距離錐・測度漸近。整合的カラー・Ξ延長比較・全残余一様tensor評価を証明 |
| [Part II](papers/secondary-periods-torelli.tex) | 28 | 一般WP completionはcontrolled push-off付き |
| [Part III](papers/conifold-localization.tex) | 57 | Actual localization/pGHは(H_loc)+(H_anc)付き |
| [総説](papers/series-overview.tex) | 11 | 五篇と曲面実現の共同方針、定理の条件・正規化 |
| [研究素材](papers/research-directions.tex) | 10 | Jacobi/scattering・一般matroid等。現行仮定の注意を付記 |

**現行の数学的到達点：** Part I付録に、固定Hermitian depthsを保つ整合的カラーの構成、Rochon–Zhangの延長Ξとcollar pullbackの全残余一様比較、一面tensor評価の三補題を統合した。Theorem 5.1からmetric-IRFAとsmooth/exponential volume-IRFAへ渡す段階を、全残余depths・全有限階fc微分を含めて証明し、複数担当で限定的に点検した。一般log-smooth collarと残余normを保存しないrho-smooth射影ではこの翻訳が破れる例も記載した。固定SNC対の結果であり、退化族の一様比較やPart Iの他の全証明を今回検証したとはしない。

Smooth divisorに限るRochon–ZhangのTheorems 7.4・7.6と、滑らかな次数e超曲面のlog共鳴係数・可積分tailは既存の有効な結果として保持する。曲面側の選択した中間尺度は、同じglobal写像の歪みと基点のtarget変位に条件を課すことで、component core・変更collar内の全基点に一様となる。詳細の定理ラベルと未点検範囲は[研究ノート](research/notes.md)を参照。

三repoの照合では、五次の(CP)をPart IVから得る経路に(TC)が必要で、Part Vのactual直径帰結には(CP)＋(PBE)が必要なことを総説へ反映した。曲面側の直接scalar/portal経路はこれらのpackage自体を検証しない。Part Iの接続は同じfiberの端点をambient空間内で結ぶものであり、fiber内の長さ評価と区別した。固定成分は $d-1$ 本の直線の補空間であり、固定補空間のblow-downを退化族の一様比較へ読み替えない。

最初に[研究方針](00_research_plan.md)、次に[研究ノート](research/notes.md)を読む。[移行・検証範囲](research/migration.md)と[ソース対応](research/source-manifest.json)を確認する。短い再構成稿は全文へ置換済み。旧稿独自資産の網羅的照合は残る。

ルートで `latexmk`。PDF/SyncTeXはbuild/。現行の[検証状態](research/validation.json)で数学的点検・組版・表示確認を分ける。正本はmain。[research-hub](https://github.com/uedakazushi/research-hub)。

組版にはLuaLaTeX/latexmk、LuaTeX-ja（ltjsarticleとHaranoAjiフォント）、TikZ、AMS、mathrsfs等の原稿で指定した標準TeXパッケージが必要。lualatex.fmtとrsfsのフォントmapが有効なTeX環境で上記コマンドを実行する。変更した2稿の再組版・表示確認の状態と、変更していない3稿の既存検証記録は区別する。
