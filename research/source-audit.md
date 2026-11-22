# 現行原稿と回収元の監査範囲

2026-11-22 / v1.18（Part I v1.9、総説v1.14）。現行稿の仮定・依存入力・一次資料の確認範囲を整理する。実行済み組版・対象限定の内部点検の正本は `validation.json` とする。原稿に証明があること、指定箇所を今回点検したこと、外部原著の全証明を検証したことを区別する。Part I v1.9の既存の73頁の組版と指定13頁・150 dpiの実表示記録を保持する。今回はPart I–III・研究素材を再組版せず、そのTeX本文を変更していない。総説v1.14はLuaLaTeX/latexmkで22頁に組版し、主要log六分類は全て0。変更頁と隣接頁1–5、9–10、13–15、20–22の計13頁を150 dpiで実表示確認した。全頁の目視確認や全証明の再検証を意味しない。頁数・source/PDF hash・log分類・実表示範囲は `research/validation.json` に記録する。 総説はPart Iの有効な命題・系とPart IV v1.12を保持し、曲面改訂44の標準六次同時実現とPille-Schneiderの先行性を反映する。

## 今回の六次同時実現とhybrid測度の照合

曲面改訂44の `ke:petersen-actual-neck-periods`、`ke:petersen-full-moment`、`ke:sextic-simultaneous-realization` の指定証明鎖を作成担当・統合担当・独立担当が実読した。全ρ=4π/5とsource allocation (1,1,1,1;2)のfinite-t period整合、内部Euler framingの符号、十一entryの正配分、内部二端cuts、両側三sourcesのseparator、source wallの相殺、Dini、中央parameter freeze後のfull source保持を確認した。Core domains・primitivesの先固定とanchor葉の後選び、free anchor bandsでの全open germs相対の再補正、三面共通の平行移動2ρr'_vとprimitive normal covector、同じ射影へのGH・測度移送にも具体的な欠落を認めなかった。この限定点検は全P0・一般面積定理・全原著の全面再監査ではない。

L. Pille-Schneider, *Hybrid convergence of Kähler–Einstein measures*, Ann. Inst. Fourier **72** (2022), no.2, 587–615、[DOI 10.5802/aif.3455](https://doi.org/10.5802/aif.3455)、[刊行版本文](https://www.numdam.org/item/10.5802/aif.3455.pdf)を実読した。Theorem A（pp.589–590）は半安定還元を持つ正準偏極退化、Theorem B（p.590）はnormalなreduced中央fiber模型と、特異locusに質量を置かない解析的測度極限を仮定する。Theorem 2.1（p.604）のcanonical model、Remark 2.4（p.605）とProposition 3.1（p.607）の成分交点数、Definition 1.2（p.593）の重複度付きmodel MA、およびp.600のdivisorial付値の規格化を照合した。標準的な付値はord_D/m_Dであり、reduced canonical modelではm_D=1。本族のnormal canonical全空間・reduced slc中央fiber・相対正準束O(d−4)は既存の曲面証明と整合する。

原典の[ω̂]=c_1(K)、μ=ω̂²と本稿のω=2πω̂、dV=ω²/2の差を確認した。成分交点数(d−4)²は本稿の質量2π²(d−4)²と確率重み1/dを与える。従って原子化・等重み自体を新規成果とはしない。Hybrid中央fiberはBerkovich空間であり、cubical計量基底や細分化されたfibration基底と同一視する比較写像は構成していない。本稿で追加されるのは、同じactual Lagrangian射影上での全域GH近似・作用atlas・測度収束の同時実現である。

2024–2026年の関連検索も含めた限定探索では、これら三条件を同時に扱う追加の一次結果は確定できなかった。この不検出を新規性・優先権の証明とせず、既存のEM・Mikhalkin・Ruan・FBP・Zhang・Mandel等の対象別比較を保持する。

## 結論

旧稿に含まれていた「証明済み」と「証明に追加入力が必要」の混在を解消しました。代数幾何、有限複体、抽象 metric gluing の無条件部分は維持し、未閉鎖の解析段階は次の三仮定へ分離しています。

1. Part II: controlled parallel push-off
2. Part III: `(H_loc)` と `(H_anc)`
3. Part IV–V: actual大域適用に `(CP)_d` と `(PBE)_d`。五次coarseを引用Part IVから得る経路にも `(TC)_5` が必要。

したがって、統合稿は未証明事項を無条件定理として提示しません。

## 篇別判定

| 篇 | 無条件で保持した中核 | 明示仮定下へ変更した部分 |
|---|---|---|
| I | 距離錐、測度付きtranslation、LDP、face mass、exact tail、一様Mellin recursion、積の距離Laplaceの複素対数germと基点距離分布の復元 | 通常の全face volume-IRFA。距離を用いる結論にはmetric-IRFA。複素normal-depth Mellin continuationには残余L1で制御したjoint polyhomogeneity。実距離LaplaceはKE積でも非有理型の例を持つ |
| II | oriented/full/generic Torelli、finite period closure、branch separation、全四点 metric、minimal-excess completion | 一般 secondary WP completion |
| III | algebraic models、canonical cell、positive model pGH、abstract scalar gluing、residual Torelli/WP | actual localization、anchors、portal transport、actual global pGH |
| IV | 明記した局所模型・full-triple/closed-corner比較、source packing、固定次数の代数・残差 package | 五次exterior粗比較は(TC)5、moving-window product exhaustionとsharp co-GramはPBE |
| V | abstract pruning–transport、`diam(C_5)=sqrt(13)` | actual degree-`d` GH application |

## Part I の一次文献と適用範囲

以下の定理番号・頁は明記した確認版による。一次本文の指定箇所を読み、仮定と結論を本稿の入力に照合した。各原著の全証明の再検証や、網羅的な優先権調査の完了を意味しない。実際の資料確認日は2026-11-22（日本時間）。

| 一次資料・確認版 | 確認した仮定・結果 | 本稿に対する役割と限界 |
|---|---|---|
| R. Kobayashi, *Kähler–Einstein metric on an open algebraic manifold*, Osaka J. Math. **21** (1984), 399–418。[公刊本文](https://ir.library.osaka-u.ac.jp/repo/ouka/all/6442/ojm21_02_12.pdf)、[公式書誌](https://doi.org/10.18910/6442) | Theorem 1, pp.399–400：滑らかな射影多様体、SNC divisor、ample log canonical class から完備負 KE metric の存在と定数倍を除く一意性。直後に有限体積と曲率の全共変微分の有界性。p.409 に一般位置超平面補空間の例 | 本稿の reduced SNC pair における存在・規格化後の一意性の直接入力。bounded-additive 距離比較や再帰的減衰率の出典にはしない。出版年は公式本文・書誌の **1984** に従う |
| S.-Y. Cheng–S.-T. Yau, Comm. Pure Appl. Math. **33** (1980), 507–544。[出版社書誌](https://onlinelibrary.wiley.com/doi/10.1002/cpa.3160330404) | 書誌を確認。本文全体は取得できず、特定の定理番号は未確認。Kobayashi p.400 は存在証明の deformation method の出典として同論文を挙げる | 解析的方法の歴史的参照に留める。未確認の定理番号・一般 SNC での精密漸近を補わない |
| H. Guenancia–D. Wu, Math. Ann. **366** (2016), 101–120。[arXiv:1410.5366v1](https://arxiv.org/pdf/1410.5366v1)、[出版社](https://link.springer.com/article/10.1007/s00208-015-1306-9) | Theorem A, p.3：SNC support、係数が1以下、ample log canonical class における potential の cusp 主項と有界 remainder。Theorem B, p.4：projective log canonical pair の SNC locus で mixed cone/cusp singularities。§4.1, p.13 はこの語を標準模型との局所 quasi-isometry と定義 | より広い境界挙動の比較。残余全域に一様な可積分 tensor 誤差の直接入力ではない。A が許す負係数と、B の effective boundary を区別する |
| X. Jiang–Y. Shi, Sci. China Math. **65** (2022), 1953–1974。[arXiv:1809.06504v1](https://arxiv.org/pdf/1809.06504v1)、[出版社](https://link.springer.com/article/10.1007/s11425-021-1903-7) | setup p.2、Theorem 1.1, pp.2–3：**smooth hypersurface** と ample log canonical class。inverse-log normal variable による potential の polyhomogeneous expansion。§2 の Theorem 2.1 は既知の存在結果の再掲 | Rochon–Zhang の smooth-divisor 展開の別証明。一般 SNC crossing の joint expansion を与える文献としては使わない |
| F. Rochon–Z. Zhang, Adv. Math. **231** (2012), 2892–2952。[arXiv:1106.0873v2](https://arxiv.org/html/1106.0873v2) | §5 (5.1)–(5.10)、Theorem 5.1, p.39：adjunction により residual positivity を保ち、全 compatible `(I,i)` に共通の指数で `u_I−Ξ_{I,i}u_{I∪i} ∈ x_i^ν C∞_fc(D_I)`。標準模型の係数 `c_i=1` は (5.8) の前に明記 | 全 residual faces を含む再帰的解析の直接入力。著者の extension `Ξ` と本稿の exact collar pullback の比較は、本稿の3補題で別途行う。Theorems 7.4/7.6 の smooth-divisor phg を一般 SNC へ拡大しない |
| A. Haas, *Geodesic cusp excursions and metric diophantine approximation*, Math. Res. Lett. **16** (2009), no.1, 67–85。[出版社本文](https://intlpress.com/api/bgcloud-front/resource/pdf/volume/1806604938178359298-1806604938178359298-47d35ef29e172eaacb043bc0cbef26f3.pdf)、[arXiv:0709.0313](https://arxiv.org/abs/0709.0313) | 公刊版§1.1, p.68：parabolic stabilizer z↦z+1、horoball y>1/kの商と面積k。§2.1：embedded cuspとhoroball translates | `lem:hyperbolic-curve-tail` の標準cusp表示の参照。最大orbit高さからの実球距離O(v^−2)評価、積距離によるe^−R/R補正は本稿内で直接証明し、同原著のexcursion定理を適用しない |

### Residue measures と Mellin 係数の先行研究

A. Chambert-Loir–Y. Tschinkel, *Igusa integrals and volume asymptotics in analytic and adelic geometry*, Confluentes Math. **2**(3) (2010), 351–429、[公刊一次本文](https://www.numdam.org/item/CML_2010__2_3_351_0.pdf)、[DOI](https://doi.org/10.1142/S1793744210000223) を確認した。

- §§2.1.12–13, pp.361–363 は metrized canonical/normal bundles と adjunction から residue measures を定義する。§3.1.3, pp.378–379 の geometric Clemens complex は divisor labels と交わりの irreducible component の対を持ち、component incidence を記録する。
- Proposition 4.2, p.388 は smooth metrics と test functions による多変数 Igusa integral の正則化を、Propositions 4.3/4.6, pp.389/394 は主要係数の残余面積分表示を与える。Theorem 4.7 と Corollary 4.8, pp.395–396 は archimedean height balls の体積漸近と面上の測度極限を扱う。
- §4.2式(4.1), p.393でV(B)は `{||f_L||≥1/B}` の体積と定義される。Theorem 4.7はσ≥0でB^σ P(log B)とpower-saving remainderを与え、Corollary 4.8はσ>0の正規化height-ball measuresを扱う。これらの指定箇所をPart Iの実距離比較にあたり本文で再確認した。本稿の有限体積の実距離球外側やBusemann offsetを、このheight-ball定理の形式的な代入とは扱わない。
- 本稿の変数は `t_i=log(−log ρ_i)` であり、入力は全faceで整合する通常の `L1` volume-IRFA である。各normal parameterが独立に境界へ近付く一側Abel極限・残余parameter一様性と、residual KE mass・実距離球のBusemann phaseへの接続を主張範囲とする。元の algebraic defining norm のべきから作る height balls と実距離球は区別する。
- 「面測度が Mellin 主要係数に現れる」という一般原理や Clemens incidence の構成そのものを独自成果として扱わない。通常の `L1` IRFA から複素 meromorphic continuation は導かず、本文の joint polyhomogeneity と residual integrability の追加条件を保つ。`prop:Mellin-incidence` は与えられた labelled mixed observables の係数から非空incidenceを検出するものであり、metric link単独からlabelsやmassを回復する主張ではない。

- Grieserの[著者版セミナーノート](https://uol.de/f/5/inst/mathe/personen/daniel.grieser/Lehre/Singular_Analysis_2020/literature/Gri_phg-fcns_2019_03_25.pdf)、§2.1.2、Theorem 2.12・(29)–(31), pp.18–20を再読した。One-variableのpolyhomogeneous expansionとMellin極の次数・係数の対応、有限次数remainderが与える正則半平面を確認した。本稿の多変数化は全partial facesの残余L1 boundsを追加した反復減算として明示し、通常volume-IRFAからの有理型延長や実距離変換への適用は主張しない。

上記は既存の Bridson–Haefliger、Leuzinger、Datar–Fu–Song、Engberg との距離側比較を補う。Exact finite-volume metric-ball tail の同一仮定・同一係数式について網羅的な文献比較は未完であり、検索で直接一致する定理を確定できなかったことを優先権の根拠にはしない。

### 実距離germ・特殊関数・moment一意性の一次比較

- K. Golubev–A. Kamber, *Cutoff on hyperbolic surfaces*, Geom. Dedicata **203** (2019), 225–255。[著者版arXiv:1712.10149v1](https://arxiv.org/pdf/1712.10149v1)、[公刊書誌](https://link.springer.com/article/10.1007/s10711-019-00433-5)。著者版Theorem 1.1、pp.1–2を実読。実際の商距離d_X(x_0,x)と有限面積測度を扱い、R_X=arcosh(volX/(2π)+1)付近への集中を曲面に一様な定数で評価する。上側評価はRamanujan条件と基点のinjectivity radius下界を課す。固定曲面のcusp裾R→∞やコンパクト因子との積のgermを述べる定理ではない。本文確認は著者版に限り、公刊版全文を取得したとはしない。
- [NIST DLMF §6.6, (6.6.2)](https://dlmf.nist.gov/6.6.E2)、[§8.19, (8.19.7)–(8.19.8), (8.19.12)](https://dlmf.nist.gov/8.19)、[§10.25, (10.25.2)](https://dlmf.nist.gov/10.25.E2)を実読。E_1の−log zとentire剰余、整数次数の対数係数と漸化式、I_1級数を確認した。h(s,b)=sb I_1(b√(s²−1))/√(s²−1)は可除点を級数で補った古典的表示である。[§10.31, (10.31.1)](https://dlmf.nist.gov/10.31.E1)でもK_nの対数係数がI_nとなることを確認した。これらの特殊関数原理の優先権は主張しない。
- P. Diaconis–D. Freedman, *The Markov moment problem and de Finetti’s theorem: Part I*, Math. Z. **247** (2004), 183–199、[著者版](https://www.stat.berkeley.edu/~aldous/206-Exch/Papers/diaconis_2004.pdf)、Theorem 1、p.184は文献担当が実読した。コンパクト区間の確率測度の全momentsによる一意性を述べ、Hausdorff (1921) に帰属させる。Hausdorff原著の実読は未実施。本稿は多項式稠密性から直接証明し、この標準原理を新規成果に含めない。

積の新命題で個別に検証したのは、実際の積距離からのkernel導出、cusp裾誤差をRe s<3の正則項へ分離する範囲、および幾何学的momentsとの係数同定である。指定文献で同一の積・observable・係数式の既存定理を確定できなかったことは、新規性・優先権の証明ではない。

### Part Iの公表単位と比較の焦点

[Leuzinger, J. Lie Theory 14 (2004), 317–338の一次本文](https://www.heldermann-verlag.de/jlt/jlt14/leuzams.pdf)では、実rank≥2の対称空間のirreducible nonuniform arithmetic quotientを対象とする。Lemma 5.1（pp.330–331）のnet上の加法比較、Theorem 5.2（pp.331–332）の有限Tits quotient上のcone、Corollary 6.3（p.336）のgeodesic-ray divergenceを本稿の一般原理に対する先行結果として扱う。Corollary 5.5（p.332）のCAT(0)結論も一次本文で確認した。Part I `rem:K5-not-CAT0` は五直線のall-right K5 coneに二つの異なる最短chordを直接構成するので、このKE側のconeが同じCAT(0)クラスに入るとは限らない。原著の全証明を独立に再検証したという意味ではない。

公表準備で保持する補足結果と、その確認範囲は次の通りである。

- `cor:tail-intrinsic-uniform`：既証のexact tailからh_*とW(o)の内在的な回復、log Wのh_*-Lipschitz性、有限δ-netによるcompact基点集合上の一様性を証明する。新しい解析入力や族一様評価は加えない。
- `prop:depth-gauge`：smoothなHermitian norm比が与えるt'_i−t_i=O(e^(−t_i))から、非compact level setsの全残余一様なHausdorff差を評価し、b_iと各幾何学的重みの不変性を証明する。任意定数shiftによるdensity係数の変換は別の規格化恒等式として区別する。
- `ex:nonintegrable-cusp-tail`：pole距離と面積積分を直接計算し、非KEの回転曲面で同じray/normal massと2πe^ℓ R^a e^(−R)の裾を得る。可積分性を落とすと有限な正規化裾係数が失われる例であり、KE metricやrough cone比較一般の反例ではない。

- `lem:hyperbolic-curve-tail` と `ex:KE-product-distance-log`：finite-area双曲曲線のdeck orbitの最大高さはparabolic translationで割った局所有限性により達成される。垂直距離下界と一つの最大高さのliftの距離公式から、角一様O(v^−2)、曲線裾A(p)e^−R+O(e^−3R)を得る。Compact双曲曲線Yとのactual KE積では、C_o=A(p)∫d_Y²/2>0として実球裾e^−R(W+C_o/R+O(R^−2))、実距離Laplace W/ε+C_o log(1/ε)+O(1)を証明した。Normal densityは厳密な積型で、その深さMellin変換は有理型である。作成担当と統合担当が指定証明を読んだ。この一側漸近の証明を保持し、次の命題が積の場合の複素解析接続を与える。例の優先権の網羅的確認は未了。

- `prop:compact-product-logarithmic-germ` と `cor:compact-radial-recovery`：任意の閉コンパクト連結Riemann因子Yについて Re s<3 の切断半平面への対数分岐を証明する。作成担当・統合担当・独立担当が実装された本文を読み、Stieltjes下端の正符号、裾誤差の微分を使わない正則剰余、b=0を含む一様支配、Q_nの明示上界、entireなH_o、monodromyの符号、Φの導関数の階乗、compact moment一意性と高次元KE適用を照合した。具体的なgapを認めなかった。研究ノートの球面変形の距離・面積・曲率も独立に照合した。一般KEの等長型・安定性・族一様性を含意しない。

全faceのconditional moments・vertex tightness・actual-ball tailと、weighted total variation・Abel recursionの指定証明には既存の対象限定点検を保持する。a.e. conditional measures、exact depth/quotient compatibility、全深い面の密度評価、二つの極限順序、compact subcritical範囲を確認し、この鎖で新たなgapを認めなかった。SNCカラー構成・Rochon–Zhang原著や全Part Iの再監査とは区別する。

一般的な球包含・有限net・residue-measure原理は独自成果として数えない。公表上の中心は、固定ample SNCのKE tensor入力から全域の距離錐を構成し、残余測度と実距離球のBusemann位相へ接続する定理の組合せである。追加本文の内部点検・組版・表示確認はそれぞれ `validation.json` の実施範囲に従い、網羅的な優先権確認・外部査読・投稿完了とは区別する。

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

### 全深部triple比較の最小入力

Part IV v1.10で抽出され現行v1.11にも保持する `coarse:thm:boundary-to-triple` と `coarse:thm:full-triple-tensor` への適用を、2026-11-22 の現行作業版 `papers/sections/full_triple_comparison.tex` で直接点検した。Fixed-face density下界はparameterに一様であり、上界は各固定parameterのradial閉包上の滑らかさから得る有限値だけで足りる。Radial simplexと全角phaseのcompact quotientで先に最大値原理を使い、complete inner comparisonの境界発散で上側比を閉じる。Outer translated modelとの比較は境界下界を用いる。角被覆へのpullbackはこの後の局所正則性にのみ用い、被覆上の非compact最大値原理や一様な境界上界を追加しない。

Relative windows の最小深さ、shiftの定数、Savin閾値の後に深さを選ぶ順序、actual capped densityからfixed-face入力を得る有限chartの量化を照合した。`coarse:lem:small-volume-tensor` の証明も読み、[Savinの著者版](https://www.math.columbia.edu/~savin/Small_pert.pdf) の(H1)–(H2), p.558、(H4), p.559、Theorem 1.3, p.560 と対応させた。この局所安定性の指定点検で新たなgapは認めなかった。Capped determinant鎖の担当別の実読は次節に区別し、Cheng–Yau原著全証明や全exteriorのTC/CP/PBEの検証は含まない。局所結果を全曲面ambient距離へ拡張する主張でもない。

### Capped densityから全smooth fiberの下界まで

[Part IV v1.11・commit a6cf38a](https://github.com/uedakazushi/kaehler-einstein-degeneration/tree/a6cf38a417a9c5707cc06cf25d8b9faf94e58725)の `coarse:lem:capped-positivity` → `coarse:lem:weighted-cap-lower` → capped pair/triple → `coarse:thm:global-determinant`（六型）→ `coarse:lem:one-sided-volume` → `coarse:cor:degree-d-volume-lower` を退化担当が実読した。固定d≥5・固定族・固定Hermitian dataに対してt一様であり、一般位置planes、Fのtriple非零・double上単純零、small fibersの滑らかさを入力とする。

公表用に明示した `coarse:eq:residue-density-normalization`、`coarse:eq:intrinsic-cap-curvature`、`coarse:eq:cap-absorption-budget`、`coarse:rem:capped-global-potential` は、固定residueとHermitian weight、Chern微分によるsource軸を含む全点式、α_*≥4Σk_iとframe error budget、全fiber上の片側potentialを区別する。有限cover → A_0 → 比較定数 → t閾値の順も明示した。変更式・定数・量化は別担当も独立に点検した。本資料の編集担当はこの新式と任意次数corollary・potentialの原文を読み、旧六型全証明の再監査を自ら行ったとはしない。

新しい外部解析定理の適用、原著全証明の再読、形式証明、既存証明書の再実行はない。二側actual tensor比較、次数一様性、moving buffer、TC/CP/PBEの検証は含まない。Part IVの120頁組版と指定12頁の実表示は退化repo側の検証記録で、本repoでの再組版ではない。

## 曲面正本の大域距離・相対変更の確認範囲

現行接続先は[曲面改訂44・確認済み保存commit 1088f86](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/tree/1088f86cf8f0c70c74a1e4caa3b90393ff627067)（資料確認日2026-11-22）。定理と証明の正本は同repoであり、本repoのPart I–III本文の新しい退化族入力にはしない。総説v1.14はこの確認版とPart IV v1.12（commit `11910259dd1628d542df57d370123d0a40b08d61`）を引用する。以下に保持する対象限定監査は、各指定証明の範囲で有効であり、現行曲面全稿の全面再監査ではない。曲面改訂44の外部組版は321頁、主要log六分類0、指定22頁の150 dpi実表示確認を統合担当から受領した。最終PDFの10・321頁を再表示し、他20頁は確認済み画像とbyte一致である。これは本repoでの再組版ではなく、具体的なhash・表示頁・保存先は `research/validation.json` の外部参照記録に分ける。

- **同じ射影の体積測度極限の直接点検。** 改訂44 `ke:global-volume-measure` の証明を読み、Part Iのbounded-primitive Chern–Weilを用いる各成分質量V_*=2π²(d−4)²と全体積dV_*、固定compactのgraph像の互いの素性・体積収束・clipped-depth値、exhaustionによる残り質量の抑制を確認した。同じfの押出しは成分頂点に質量1/dを置く。p_T^−1(e_i)が一点であることとcompact性によりπの固定位相底空間にも移り、五次と標準等重み六次の作用指定射影は一様な値比較で同じ結論を持つ。Moving neckの体積評価・追加速度・対角列の変更は用いず、極限測度の全台性を要求しない。

- **Actual両端periodの独立内部点検。** `ke:k4-actual-neck-periods`、等重み系 `ke:k4-equal-weight-periods`、非対称例 `ke:k4-cyclic-weight-periods` の全証明を作成担当と別の二担当が読んだ。全K2 tube上のnormal period零の閉差からχの共通性を、clutchingからΣχ=−2πを得る。Basinsのdisk上のactual normal framesとsource zero/puncture poleのwindingを使い、end shear −1とcritical shear n−1を区別する。有限整合式、等重みの必要十分条件、非対称5cycle例の隣接・非隣接二ケースを確認した。独立primitiveの任意定数による合わせ込みはない。既固定allocationに対する障害と、初期allocationを選ぶ存在主張を区別した。
- **全momentと全open germsの独立内部点検。** `ng8:uniform-k2-end-periods`、`ng8:thin-source-tail-choice`、`ng8:quintic-full-moment` の統合本文と成分別面積定理・ordered cuts・source wallを読んだ。負側の補正は(J_i+(n−1)μ)−(R_i−μ)=J_i−R_i+nμ、全量は正側−ΣR−μ／負側−ΣR+4μで一致する。全深部評価からextended bandの正marginを得て、Darboux-ball分割による面積連続性とDiniで初期全tailsを小さくする。Target−protected massのsmoothness、最後の同targetへの相対Moser・open germs恒等・source point first jetsを照合した。同じP_j内で初期葉を選び、通常P0と作用指定構成を別に作る量化とfixed Tも確認した。
- **同じπのatlas/GHへの接続。** `ke:quintic-simultaneous-realization` の実本文を読み、same analytic cuts・canonical moments・full K2 partitions・中央full nodal neighborhoodsからrelative-replacementの四条件を確認した。新foliationについても飽和となるcuts、whole-fiber閉商、core/branchの一斉2π換算、q=1 branch chart、actual cocycle、同じ射影の値比較からslow diagonalへの接続を照合した。改訂42では `atl:qone-chart`・`atl:gluing-criterion`・`qg8:star-transition`・actual-anchor・endpointへ逆向きにたどり、全平行移動付きの式 `ke:eq:quintic-affine-full-transition` を独立に確認した。ζ'=ζ、s'=−s+(y_k+y'_k)ζ+w_i,j+w_j,iは全三面で同じtranslationを持ち、Σy=Σy'=1からGL(3,Z)へ延びる。Primitive branch gradient、非対称正weights、2π、focus puncturesも整合する。主担当も新式を別に点検した。
- **Source-free限定とthin葉の量化。** `neck_action_matching.tex` 前半の `ng8:central-criterion` までの自由作用・面積affine性は、source-free neckに限る。Actual source-inclusive neckはt≠0でもμ=0に固定点を持ち、全intervalにはwall項を使う。`ng8:thin-source-tail-choice` と `ng8:quintic-full-moment` ではS_t・Dを先に固定し、引戻し座標でthin葉を選ぶ。S_tが新annuliを保つことや全source円葉がDの支持外にあることは不要。点近傍のμ非依存とmarked classを保ち、全同一moment connector・同じclipped-depth mapによりGH予算へ葉の幅・C^k定数・追加t閾値を入れない。この修正箇所の対象限定点検を曲面側から同期する。

これらの既存独立監査と今回の体積測度極限の直接点検は指定接続に限り、一般成分別面積定理、P0全体又は外部解析原著を全面的に再監査したものではない。各tの同じ射影でのatlas/GHは、atlasのt方向の収束、極限基底のintegral affine構造、cubical距離のHessian・Monge–Ampère性を含まない。任意先指定source tails・非標準六次targets・t連続性・速度も結論しない。

- **Actual五次anchorの独立内部点検。** `ke:k4-actual-end-anchor` と `ke:k4-protected-anchor-selection`、`ke:actual-anchor-fan-criterion`、`ke:anchor-stokes-budget`、component linkのmoment・meridian規格化、相対面積実現、actual cone fillingの指定証明を読んだ。O(1)のsectionの単純零点によるwinding −1と、同じgraph/averaging/Hamiltonian isotopiesによるactual cyclesへの移送を確認した。K2内側cutの二深度比一様評価とj→N→tの順序、三basinのstrict margins、Diff_0(P rel K)内のdensity–Moserと有限marked点のfirst-jet固定、fan角の単調性、全normal–corner開overlapの保持を確認した。Source全飽和近傍はδ決定後に中央へ選び、大きい相対isotopyを先に入れてから同anchorの二族をsmall interpolationで合わせる。この限定選択で新たなgapは認めなかった。任意先指定の大source近傍や追加anchor保持annuli、この局所系単体には全neckの作用直線性、反対端の切片/shear・全域atlasは含まれず、上の全moment構成と統合定理を使う。

- **成分別輸送の独立内部点検。** `ng8:componentwise-primitive`、`ng8:componentwise-critical-area`、`ng8:strict-area-cuts` の全証明を読んだ。Rel-K orbitが各自由成分を保つ必要性、固定線型right inverseと凸性によるsmooth正配分、cell densities、成分ごとの零積分差の固定支持primitive、相対Moserの順序を確認した。Protected mass自体がnonsmoothでもfree要求量r=a−κがsmoothなら足りる。Strict cutはalternating pathによる非負配分と全edgeへの小さい先行配分から証明される。Annulus障害と端点模型は、正のbaselineとcell内bumpsにより実面積familyとして実現できることも確認した。既存のdisjoint-disks版への反例ではない。
- **Actual source固定の微小変更。** `ng8:p0-source-protected-reduction` と `ng8:p0-small-area-flexibility` の統合証明を読んだ。全source annuliの外のsmooth reduction、incidence graphの連結性、spanning-tree right inverse、正のbaselineからの小摂動、自由部分のMoserとcircle liftを確認した。源点だけでなくfull nodal neighborhoodsを固定する。支持するfree部分の大きさに依存する小変更であり、所定大targetやtに一様な自由度を結論しない。
- **Anchorとcoreの指定証明。** `ke:anchor-liouville-actions`、`ke:actual-anchor-fan-criterion`、`ke:anchor-stokes-budget` の草案作成と統合時の点検を行い、別担当も独立に読んだ。Liouville actionの倍率、closed primitive差・整数framing、Stokesの符号と総量、actual annulusからのface係数の正値性、near-core fan chartとambient normal actionの整数延長を確認した。一般のcore判定ではactual clutching/marking、anchor葉の面積実現、neck両端の切片とwhole-fiber一致を入力として保持する。標準P0の五次end-collar選択については、今回の `ke:k4-actual-end-anchor` がclutchingと所定anchor targetを実現するが、この局所系自体には全neckと反対端の整合は含まれない。無理period ratioの障害は固定したfillingのchartに対するものである。

- **相対変更の指定証明。** `ke:moment-relative-replacement`、`ke:relative-replacement-gh`、`ke:raw-moment-error-insufficient` を本文で読んだ。Whole-fiber閉商を底空間同定より先に作る順序、同じ保持corner全葉・source nodal neighborhoods・canonical moment・anchor/cap・component領域、実際のmarked product/cone商という条件を確認した。Cornerでの厳密一致とneckでの共通profile比較から全域Cη評価を得るため、reduced diffeomorphismのC1小ささは不要。一つの固定木系をslow diagonalに沿って構成する量化と、raw momentのL^(-α)例も確認した。Atlas候補の存在を安定性から推論しない。
- **Fixed-fiber面積とsource wall。** `ng8:fixed-fiber-relative-dh` と `ng8:source-dh-wall` の証明を読んだ。固定tのfree compact band、作用不変primitive、affine boundary actionsと整数framingからのStokes式を確認した。周期2πのweights(1,−1)模型の面積π(c−|μ|)は固定点で折れる。Source横断全intervalへの適用、actual P0全体の面積公式、t=0へのsmooth extension、族一様な評価を結論しない。相対Moserのarea positivity・総量・保存collars/capsの余裕・端germsは別入力である。
- **全域上界の独立内部点検。** `ke:anchor-trimmed-neck-domain`、`ke:same-moment-corner-reference`、`ke:collapsed-tree-common-moment`、`ke:point-to-corner-portal` から `ke:global-ambient-upper` への鎖を読んだ。旧full cornerの経路は除去capを通ってもambient上界に使え、保持集合のintrinsic上界を仮定しない。全端点の分類、anchorの等号境界、同じmoment上の全fiber合併、coreごとの拡大compact接続を確認した。有限galleryのM本に対し、junctionがM−1、両端が2なので接続費用は(M+1)Hである。
- **下界・局所入力の共同点検。** `ke:global-clipped-cogram-lower` は固定t,m,K、0<S≤R、任意の非負誤差εに対する有限評価であり、ε→0やS/R→1は最後の対角化で用いる。Sourceを含む固定Pのshell補題 `ke:source-inclusive-fixed-shell` は、同一の非零正則体積frameと固定rでSongのfixed-compact収束を適用し、Rochon–Zhangのcusp評価からmoment主項とshell横断下界を得る。これらの指定証明と一次箇所は各担当が照合した結果を同期しており、本資料の編集担当が全外部解析を再証明したという意味ではない。異なるnormal formsのprimitive差、固定compactとmoving exhaustion、protected距離とambient距離を区別する。
- **有限targetの独立内部点検。** `topo:cubical-local-models`、`topo:cubical-moving-blowups` の全局所閉球とmoving-basepointの証明を読んだ。Support二元の折れ点e_i+e_jもbookであり、三座標全て1の点だけが全角3π/2の錐となる。固定局所錐のfull-ambient閉球へ移し、成分錐から逃げる場合はpositive-starの退出費用でbook又は平面を得る。四型の任意の有限基点は、任意の拡大列で実現できる。
- **実曲面への移送。** `ke:distortion-to-pointed-balls` はcompact geodesic spaces間の全射の歪みδから、全中心・同半径閉球の基点付きGH距離≤3δ/2を与える。`ke:intermediate-moving-classification` は同じf=pπを用い、a→∞、a/R→0、Rε/a→0の条件下で全型と実現を移す。Core・変更collarへの既存の一様成分錐も保持する。一般的な局所cone幾何・GH移送自体の新規性を主張せず、任意尺度・tensor収束・極限交換へ拡張しない。

この指定範囲で結論を妨げるgapは認めなかった。五次と標準等重み六次では初期source葉を選ぶ存在問題として同じπのatlas/GH/測度収束まで証明が閉じる。任意先指定のfull source tailsと非標準targetsへの相対問題は別に残る。全曲面原稿・Part IV原著の包括的再監査、外部査読、形式証明、網羅的な先行研究比較は未了である。CP/PBE/TC、H_loc/H_anc、controlled push-offは独立のままである。

## 曲面接続の一次文献比較

次は検索snippetではなく、指定した一次本文を確認した範囲である。原著の全証明の独立検証ではない。

| 一次資料・確認版 | 確認した箇所と射程 | 本研究との比較 |
| --- | --- | --- |
| Fernández de Bobadilla–Pełka, *Fibrations by Lagrangian tori for maximal Calabi–Yau degenerations and beyond*, CPAM (2026), e70060、online 8 July 2026。[出版社](https://doi.org/10.1002/cpa.70060)、[arXiv:2312.13248v4](https://arxiv.org/html/2312.13248v4)（9 July 2026） | Proposition 5.6 p.24、Example 5.8／Remark 5.9 p.25、Propositions 6.3 p.27／6.13 p.30、Theorem 6.14 p.31、Remark 7.4。一般Kähler SNC退化。(b)のfibrationは部分領域だが、(c)はproperなら全fiberの構成Kähler計量のpair GH。固定εとadmissible path (|z|,q)→(0,0)、直径正規化、選択部分複体Δ_Sを区別する | 全fiberのGHを局所結果へ弱めない。明示的GH写像とaction affine structureも既存。Actual負KE計量、coreを埋めた全域fibration、同じ射影の全endpoint距離評価が比較対象で、一般的なtransport・collapseを新規とはしない |
| Evans–Mauri, *Constructing local models for Lagrangian torus fibrations*, AHL **4** (2021), 537–570。[掲載版PDF](https://ahl.centre-mersenne.org/item/10.5802/ahl.80.pdf)、[arXiv:1905.09229v3](https://arxiv.org/abs/1905.09229v3) | 掲載版Lemma 2.16 pp.543–544／Remark 2.18 p.544、Lemma 2.22／Remark 2.23 p.545、Assumption 1 p.561、Propositions 6.11–6.12 p.565／Theorem 6.14 p.566。Linkからcompletionへのcone extension、curvature条件付きcircle lift（曲線では自動）、log-CYな一次元strata下の近傍fibrationとdual monodromy | Genus零だけのlifting原理ではない。多数puncturesの曲線へAssumption 1を流用せず、指定finite collar・normal moment・core primitiveを保つ相対構成を別に確認する |
| Chakravarthy–Groman, *Almost toric fibrations on K3 surfaces via degenerations*。[arXiv:2502.04304v3](https://arxiv.org/html/2502.04304v3)（28 May 2026） | Definition 1.2、Theorems 1.6／1.8、Corollary 1.9、改訂Lemma 2.13。Symplectic Kulikov modelから全nearby K3へのATFとnodal affine structure。Transportの連続性は指定cylindersを潰した商への主張 | 全域fibrationの先行結果として扱い、anticanonical cycleの入力と一般型曲面の曲線strataを区別する。FBP bibliographyの誤記2502.11224は転記せず、正しい識別子2502.04304を用いる |

Moserによる同じcohomology classの形式の同定だけでは、移送された複素構造の計量比較は得られない。今回明確にした相違が最初の成果であるか、より広い既存構成からどこまで導けるかというpriorityの網羅的確認は未了である。Stokes、GH安定性、cone extension、action座標の一般原理を独自成果とは扱わない。

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

