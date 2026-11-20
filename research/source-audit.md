# 数学的再監査報告

日付: 2026-08-31  
対象: `Multiscale Kähler–Einstein Geometry I–V` 統合改訂稿 v1.0

## 結論

旧稿に含まれていた「証明済み」と「証明に追加入力が必要」の混在を解消しました。代数幾何、有限複体、抽象 metric gluing の無条件部分は維持し、未閉鎖の解析段階は次の三仮定へ分離しています。

1. Part II: controlled parallel push-off
2. Part III: `(H_loc)` と `(H_anc)`
3. Part IV–V: `(PBE)_d`、および一般次数の大域適用では `(CP)_d`

したがって、統合稿は未証明事項を無条件定理として提示しません。

## 篇別判定

| 篇 | 無条件で保持した中核 | 明示仮定下へ変更した部分 |
|---|---|---|
| I | 距離錐、facewise translation、LDP、face mass、exact tail | 一様 Mellin 極限に weighted uniform integrability を追加 |
| II | oriented/full/generic Torelli、finite period closure、branch separation、全四点 metric、minimal-excess completion | 一般 secondary WP completion |
| III | algebraic models、canonical cell、positive model pGH、abstract scalar gluing、residual Torelli/WP | actual localization、anchors、portal transport、actual global pGH |
| IV | quintic coarse geometry、局所模型、source packing、固定次数の代数・残差 package | moving-window product exhaustion、sharp co-Gram |
| V | abstract pruning–transport、`diam(C_5)=sqrt(13)` | actual degree-`d` GH application |

## 具体的に修正した誤り・過剰主張

### Part I

- Mellin recursion の `(2π)^{|I|}` は normal torus を二重計上していたため削除。
- 一様 dominated convergence に必要な error-weighted exponential terms の uniform integrability を追加。
- Chern–Weil の Stokes 符号、LDP lower bound、properness/net/fibre control を修正または展開。
- link の復元を、追加 marking なしの強すぎる表現から isometry type の決定へ弱めた。

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

## 機械・視覚検査

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

