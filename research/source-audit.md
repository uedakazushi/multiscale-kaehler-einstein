# 現行原稿と回収元の監査範囲

2026-11-22 / v1.5。回収元の2026-08-31統合改訂稿v1.0の監査事項と、現行稿で有効な判定を整理する。実行済み組版・限定的内部点検の正本は `validation.json`。原稿に証明があることと今回その証明を点検したことを区別する。

## 結論

旧稿に含まれていた「証明済み」と「証明に追加入力が必要」の混在を解消しました。代数幾何、有限複体、抽象 metric gluing の無条件部分は維持し、未閉鎖の解析段階は次の三仮定へ分離しています。

1. Part II: controlled parallel push-off
2. Part III: `(H_loc)` と `(H_anc)`
3. Part IV–V: actual大域適用に `(CP)_d` と `(PBE)_d`。五次coarseを引用Part IVから得る経路にも `(TC)_5` が必要。

したがって、統合稿は未証明事項を無条件定理として提示しません。

## 篇別判定

| 篇 | 無条件で保持した中核 | 明示仮定下へ変更した部分 |
|---|---|---|
| I | 距離錐、全変動・測度付きtranslation、LDP、face mass、exact tail、一様Mellin recursion | 通常の全face volume-IRFAで上記は成立。複素Mellin continuationには残余L1で制御したjoint polyhomogeneity |
| II | oriented/full/generic Torelli、finite period closure、branch separation、全四点 metric、minimal-excess completion | 一般 secondary WP completion |
| III | algebraic models、canonical cell、positive model pGH、abstract scalar gluing、residual Torelli/WP | actual localization、anchors、portal transport、actual global pGH |
| IV | 明記した局所模型・full-triple/closed-corner比較、source packing、固定次数の代数・残差 package | 五次exterior粗比較は(TC)5、moving-window product exhaustionとsharp co-GramはPBE |
| V | abstract pruning–transport、`diam(C_5)=sqrt(13)` | actual degree-`d` GH application |

## 具体的に修正した誤り・過剰主張

### Part I

- `lem:SNC-compatible-collars`、`lem:fc-collar-transfer`、`lem:RZ-collar-tensor`：固定Hermitian normsを保つ実有向カラーとproduct connectionを同時構成し、RZ延長Ξからexact collarへの全残余一様比較と再帰的tensor評価を証明。RZ 1106.0873v2およびAlbin–Melrose 1012.5765v1の指定一次箇所を照合し、この入力鎖を複数担当で点検した。詳細は `notes.md` と主稿付録。
- `lem:fibres`→`prop:lifting` はambient endpoint接続として点検。`prop:cogram`→`thm:contract` の全逆計量評価・共通の深い閾値・局所一セルの長さ評価を補強し、properな1-Lipschitz全射を得た。`cor:based-ball-approximation` は全中心・全半径の閉球GH距離≤3K/(2R)を証明。指定compact集合を潰す場合のKの依存も明記し、同範囲を複数担当で点検した。
- `lem:cellwise-LDP` の下界はfull face collarの正質量compact residual集合からambient open setへ入れる形で成立する。Exact-supportへ制限した測度の正質量は一般に従わず、clean product二端cuspの反例を研究ノートに置く。`lem:deep-sector-partition` は浅い座標を残余側へ含め、追加仮定なしでglobal LDPを保つ。
- `lem:level`→`thm:tail`→`thm:joint`→`cor:Laplace` は一面比較・全faceからのconditional moment評価・直接指数積分・距離上界から閉じ、LDP/co-Gramの下界に依存しない。一般重みの角分布の分母は最小entropyのverticesの重み総和。Actual conditional residual measuresの指数tailにより、volume remainderの指数減衰も不要である。KE規格化の分布は不変である。限られた鎖の点検と、全Part Iの包括的再検証・外部査読・新規性確認を区別する。
- Mellin recursion の `(2π)^{|I|}` は normal torus を二重計上していたため削除。
- `thm:translation` は任意のnormal深さ列の最小値が発散する場合を扱い、全残余を含むstripの全変動収束、ambient短経路の退出防止、水平liftとtorus収縮から、各半径の閉球のpmGHと押出し測度の全変動収束を得る。通常のvolume-IRFAで十分であり、基点のnormal offsetと残余点の収束を明示する。
- 一様Mellinでは、全deeper faceの実際の密度からconditional residual measuresのsubcritical指数momentsを一様に評価し、全変動収束との補間からweighted convergenceを導く。任意に選んだL1 dominator自身のweighted momentは要求しない。一面だけの支配では不足する反例と、normal cutoff transition・chart partitionの違いを本文に明記する。
- 単独のmass一覧からincidenceを復元する主張を、mixed localized transformsの最高Abel係数による検出へ精密化した。通常のLaurent変数(s_i−1)に対する係数には符号(−1)^|I|が付く。
- `lem:CW` は滑らかな基準曲率と有界primitiveから直接Stokesで証明する。KE適用の背景形・potential・normal circle規格化はRochon–Zhang第2・5節の一次資料に照合し、face massの数値式は維持する。指数的shell評価やMumfordのsingular Chern–Weil theoremを主証明の入力としない。
- Chern–Weil の Stokes 符号、LDP lower bound、properness/net/fibre control を修正または展開。
- `prop:cone-limits` は正のface領域とincidence linkの積、壁までの距離が2Aを超える場合のambient閉球同定を使う。閉star全体の大域積は一般に成り立たず、三辺cycleの短絡と重複edge copiesの境界同一視をノートに保持する。全極限の分類と実現を内部点検した。
- `prop:link` はcoarse sectionに一様なO(1/r)誤差と、非連結成分間∞を許すlength metricの回復を示す。Metric linkのisometry typeを復元対象とし、labels・depth weights・genuine geodesic-ray boundaryは主張しない。Bridson–Haefliger I.5.6–7とLeuzinger Lemma5.1/Theorem5.2/Corollary6.3の一次箇所を照合し、標準事項を独自成果として扱わない。

### Part II

- Exceptional fibre 内の paths を SNC divisor の補集合へ一様に押し出す議論は、compactness と path-connectedness だけでは不足する。この controlled push-off を仮定として明示。
- 異なる finite sheets の正距離 barrier は上の仮定に依存しないため、独立の無条件命題に分離。
- Schaffler–Tevelev の直接入力を Theorem 1.2 ではなく Corollary 3.5 に訂正。
- `m=n+2` は全対象が一点になる端点として直接処理。
- Plumbing neighborhood は二側比較でなく、証明される `O(ε)` 直径上界のみを主張。

### Part III

- Local coordinate product metric を非自明な normal bundle 上の global exact KE metric とみなす表現を撤回。
- Whole-end localization と parent/refined compatibility を `(H_loc)` に分離。
- Unrecorded depths、finite-depth anchors、指定端点 transport、radial density を `(H_anc)` に分離。
- Actual global pGH は `(H_loc)+(H_anc)` の下の条件付き定理へ変更。
- `P^3` の null 条件 `r_a+r_b=m+2` と一般 `P^n` の交点数公式を追加し、高次元局所模型が conifold ではなく Segre cone になることを明記。

### Part IV–V

- Terminal cusp で order zero の gauge は fast-cusp shear を除くが、growing chart chains の product exhaustion までは自動的に与えない。
- 必要事項を `(PBE)_d` の四項目に分割:
  quantitative terminal trivialization、protected rectangular inclusion、uniform local/global/actual comparison、compatible exhaustion with two-metric escape。
- 一般次数の大域 GH 適用には coarse realization/connectors package `(CP)_d` も必要と明記。
- Part V の抽象 pruning–transport theorem と `C_5` の有限直径証明は、上記解析仮定と独立な無条件定理として保持。

## 固定次数 `d ≥ 5` の検算

`X_t = {∏_{i=1}^d L_i + tF_d = 0} ⊂ P^3` に対して次を照合しました。

- maximal squares: `d * binom(d-1,2)`
- double-line sources: `d * binom(d,2)`
- residual curve: `(d-2)`-punctured sphere
- relative section: `O(d) ⊗ O(-(d-2)) = O(2)`
- divisor degree: `d-(d-2)=2`
- canonical class: `K_X = O(d-4)`
- `K_X^2 = d(d-4)^2`
- `Ric(ω)=-ω` で `Vol = 2π^2 d(d-4)^2`
- この Ricci 規格化では co-Gram leading coefficient は `1`
- primitive normalization では距離が `1/sqrt(d-4)` 倍、co-Gram が `(d-4)I`

定数は固定した `d` に依存してよく、`d → ∞` に一様とは主張していません。

## 高次元の安全な射程

Degree `d` hypersurface `X ⊂ P^N` について、次は確定部分として記載しました。

- `K_X = O(d-N-1)`
- `K_X^{N-1} = d(d-N-1)^{N-1}`
- `Vol = (2π)^{N-1} d(d-N-1)^{N-1}/(N-1)!`
- 候補 `C_{d,N} = {max w_i=1, |supp w|≤N}`
- `C_{d,N} ≅ sk_{N-1} Δ^{d-1}`
- pure normal-crossing determinant package

一方 `N ≥ 4` では double stratum 上の source locus が正次元で triple strata と交わるため、`x_1…x_r=tz` 型の mixed cores が不可避です。また residual factor は高次元 arrangement complement になります。このため高次元 GH 極限は予想に留めています。

## 回収元に記載された機械・視覚検査

以下は回収元の記録であり、現行変更後の再実行ではない。現行版は `validation.json` を参照。

- LuaLaTeX: 全六ソース成功
- Cross-reference/citation: 未解決なし
- Box warnings: overfull/underfull ともになし
- PDF: 全篇 A4、統合版233頁
- Raster QA: 各篇全ページの contact sheet、統合版の各篇境界を確認
- Exact gallery certificate: PASS、30 squares、465 unordered pairs、9 symmetry orbits
- Intrinsic complete-window numerical audit: PASS
- Slow-box frame-shear audit: PASS
- Terminal-cusp adapted gauge audit: PASS
- Relative Bishop–Gromov bookkeeping audit: PASS

補助数値検査は解析証明の代わりではありません。定理状態は本文の仮定表示を最終的な基準としてください。

