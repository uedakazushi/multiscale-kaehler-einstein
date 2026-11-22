# 現行研究方針：配置補空間の多重スケールKähler–Einstein幾何
更新：2026-11-22 / v1.18（Part I v1.9、総説v1.14）

## 公表に向けた実行計画

数学的重要性、新規性、理解の深化、応用可能性、正確性、読者による検証、実現可能性を総合し、研究全体の価値を最大化する。[三研究の公表計画](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/blob/main/00_research_plan.md)と共同で進め、本repoではPart Iを第一優先とする。既存の五篇の順番を公表の条件にしない。

1. 距離錐と精密な体積漸近を中心に、一般SNCへの適用とRochon–Zhangからのtensor入力、全域の加法誤差への接続を読者が追える形にする。
2. 実球裾係数 \(W(o)=\lim_{R\to\infty}e^R\operatorname{vol}(X\setminus B(o,R))\) の内在性、基点比較、compact基点集合上の一様性を証明する。面質量とoffsetの表示について、幾何学的量と座標規格化を区別する。
3. 非可積分metric誤差、弱いvolume remainder、実距離というobservableの三つの役割を区別する。非KE回転cuspと抽象測度のAbel/Mellin例を保持し、actual KE積の実距離変換の対数分岐を複素領域で求める。その係数の幾何学的情報を基点距離分布まで正確に同定し、等長型の復元とは区別する。
4. Leuzingerの局所対称空間の錐、Chambert-Loir–Tschinkelのheight積分・residue measuresとの対象・observable・仮定の差を一次資料で確定する。既存原理を新規成果に数えず、個別検索で未発見であることを新規性の証明としない。
5. Part IIの無条件Torelliと条件付きWP、Part IIIの(H_loc)+(H_anc)付き局在を保持し、Part I完成の阻害要因にしない。総説は中心結果と現在の依存関係を示す入口とする。

達成基準は、主張・仮定・証明・先行研究比較を整合させ、変更証明の独立内部点検、LuaLaTeX組版と変更箇所の表示確認を終えること。これは外部査読・新規性の網羅的確認・投稿の完了を意味しない。本文と研究ノートを正本として保存し、その結果に基づき曲面側の依存表とresearch-hubを更新する。共通の一般原則・保存許可は本書後半と `AGENTS.md` に記す。


### 実行状況と次の課題

Part I v1.9は、尖点付き有限面積双曲曲線Sと任意の閉コンパクト連結Riemann因子Yの積について、実距離Laplace変換を Re s<3 の切断半平面で W/(1−s)−H(s)Log(1−s)+G(s) と表示する。Hはentire、GはRe s<3全体で正則である。`prop:compact-product-logarithmic-germ` は曲線裾A(p)e^−R+O(e^−3R)をStieltjes部分積分で扱い、積距離kernelの級数の一様絶対収束まで証明する。`cor:compact-radial-recovery` はWと対数monodromyからYの正規化された基点距離分布を復元する。コンパクト負KE因子なら総複素次元2以上のactual KE例となる。一般の通常volume-IRFAからの解析接続・基点付き等長型・安定性へは拡張しない。作成担当・統合担当・別担当が指定証明を読んで点検した。指数積分・Bessel公式とcompact moment一意性は既知の原理であり、新規性の網羅的確認は未了。 既存の全face conditional moments→vertex tightness→actual-ball tail、weighted total variation→Abel–Mellin recursion、内在的裾係数・compact基点一様性・norm gauge・非KE cusp・K5比較の対象限定点検は有効な範囲で保持し、今回の新証明の点検と区別する。

現行の曲面接続先は[改訂44・確認済み保存commit 1088f86](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/tree/1088f86cf8f0c70c74a1e4caa3b90393ff627067)。`ke:global-volume-measure` は全固定d≥5について、同じf=pπによる正規化KE体積の押出しを成分頂点上の等重み原子測度へ収束させる。固定成分の体積公式と全体積の一致、固定compact上の収束、頂点逆像の一点性を直接確認した。五次と標準等重み六次の同時atlas/GHにも適用するが、atlasのt方向の収束、極限integral affine構造、Hessian・Monge–Ampère性は含まない。標準六次の同時実現は `ke:petersen-full-moment` と `ke:sextic-simultaneous-realization` により証明され、任意先指定source tailsへの相対存在は別に残る。原子化自体の先行性はPille-Schneiderのhybrid収束定理へ帰属させ、同じactual射影の実現と区別する。

Part I v1.9の既存の73頁の組版と指定13頁・150 dpiの実表示記録を保持する。今回はPart I–III・研究素材を再組版せず、そのTeX本文を変更していない。総説v1.14はLuaLaTeX/latexmkで22頁に組版し、主要log六分類は全て0。変更頁と隣接頁1–5、9–10、13–15、20–22の計13頁を150 dpiで実表示確認した。全頁の目視確認や全証明の再検証を意味しない。頁数・source/PDF hash・log分類・実表示範囲は `research/validation.json` に記録する。 総説v1.14はPart Iの対数germ、Part IV v1.12の固定end最小入力とwinding、曲面改訂44の同じ射影の確率体積極限を統合する。五次の全moment構成を保持し、標準等重み六次の二端cuts・source wallに適合するseparator・全平行移動を含む作用atlas/GH/測度収束を統合する。

### 次の具体的な着手点

公表の第一優先は曲面P0の同じ射影による計量実現と五次・標準等重み六次の同時作用atlas/GHであり、その入力を供給するPart IVの局所解析と、固定補空間のPart Iを論理的に独立した公表単位として整える。Part Iでは既存のSNCカラー→tensor→大域距離錐の全鎖を公表用に再点検し、今回の積の明示式をその限界と精密化として配置する。新規性比較は、実際の距離分布を扱う先行結果とheight/Mellin・特殊関数の一般原理を分けて続ける。非積への拡張には、有限volume-IRFAだけでは足りず、実距離又は距離pushforwardの二次以降の誤差を制御する入力をまず特定する。積の厳密式だけを根拠に一般SNCへ解析接続を外挿しない。任意先指定source tailsと非標準period targetsは独立した拡張課題とし、現行中心結果の公表準備の前提にしない。

## 研究固有の目標と入口
固定配置補空間の距離錐・測度漸近、secondary periods・Torelli・WP、conifold gluingを研究する。Part I–IIIの全文と必要な証明を現行原稿に保持し、退化族・actual Lagrangian実現との接続を定理単位で検証する。達成基準は、条件付きの解析段階を隠さず、正本の全文と本ノートだけから入力・適用範囲・残る核心を追えることである。

## 三研究を一体で進める方針
| 正本 | 担当する結果 |
| --- | --- |
| 本repo | 固定SNC対・配置補空間のPart I–III、全体の数学的総説 |
| [kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration) | 退化族の局所一様解析Part IV、(CP)＋(PBE)付き大域枠組Part V |
| [surface-lagrangian-torus-fibration](https://github.com/uedakazushi/surface-lagrangian-torus-fibration) | Actual KE Lagrangian fibrationと全曲面GH実現、五次・標準等重み六次の同一πによる作用atlas/GH/確率測度収束 |

研究・編集・証明監査は共同で進める。対象と主要定理が異なるためrepoと論文はこの責任分担を保ち、総説は入口と定理の接続を担う。論文の分割・統合は公表価値と論理的まとまりに基づき判断し、同じ証明を複製しない。依存定理の仮定・尺度・距離の範囲・確認版を[ノート](research/notes.md)に集約し、入力の修正は正本→利用先→総説・hubの順に反映する。

固定成分は $H_i\simeq\mathbf P^2$ から $d-1$ 本の直線を除いた補空間である。Part Iの固定空間の $R\to\infty$ を $t\to0$ の族一様性へ読み替えない。Part IIの残余複素periodは第二作用積分と異なる。曲面側の直接大域証明があっても、(CP)/(PBE)/(TC)や(H_loc)/(H_anc)自体の検証状況は変えない。五次と標準等重み六次では同じ曲面fibrationの作用atlas・GH・確率測度収束を同時実現する。

## 論文と証明の状態
- `papers/multiscale-kaehler-einstein.tex`：主たる公表用原稿Part I v1.9。距離錐・face masses・tails/LDPに加え、任意のnormal深さ列に対する測度付き平行移動、直接Stokesによる体積公式、全faceのvolume-IRFAからの一様Abel–Mellin recursionを証明する。KE積の実球裾の二次項、コンパクト因子との積の複素対数germと基点距離分布の復元を加え、normal-depth変換と区別した。再帰的接続は同じfiberの端点を結ぶambient曲線を用いる。固定SNC入力・距離収縮・LDP・tail、測度付き極限・Chern–Weil・Mellin、moving-basepoint分類とmetric link復元の指定証明鎖の限定点検を保持する。今回の実施範囲と組版・表示記録は検証状態を参照する。
- `papers/secondary-periods-torelli.tex`：Part II v2.1。Torelli・finite period closure・branch separationを保持。一般secondary WP completionにはcontrolled parallel push-offを仮定する。
- `papers/conifold-localization.tex`：Part III、57頁。algebraic models、positive model pGH、abstract gluing、residual Torelli。Actual localizationとactual global pGHは(H_loc)+(H_anc)に依存する。旧ノートの「fixed node局所化を無条件に証明済み」との記述を最新版の条件付き化より優先しない。
- `papers/series-overview.tex`：五篇と曲面実現の関係・定理状態・共同監査順、v1.14。曲面改訂44のactual両端period条件、全moment構成、同じ射影の五次・標準等重み六次の作用atlas/GH/測度収束を紹介し、先指定source tailsと非標準targetsの限界を明記する。Pille-Schneiderのhybrid原子極限と等重みの先行性を比較する。全移動基点の四型分類、同半径閉球比較、source-inclusive固定shell、有限stage co-Gramも保持する。Part I v1.9の対数germとradial分布回収、曲面の確率体積極限、Part IV v1.12の固定end入力・frame windingを統合する。Part IVのcapped下界補強も保持するが、五次(CP)の引用経路に(TC)、Part Vのactual直径帰結に(CP)＋(PBE)が必要なことは変えない。曲面側の直接経路と区別する。組版後の頁数と表示範囲はREADME・検証状態を参照する。

## 固定SNC入力の確立範囲
主稿 `lem:SNC-compatible-collars` は、元の実有向blow-up上の固定Hermitian normsを用い、全strataのcollarsと全normal line bundleのproduct connectionsを次元順に同時構成する。残余の深さの保存、circle-equivariance、quotient-in-stagesを厳密に保つ。`lem:fc-collar-transfer` はRochon–Zhangの延長Ξと選んだ射影の差、およびHessianの差を、任意Nに対し $x_i^N C^\infty_{\rm fc}$ と評価する。`lem:RZ-collar-tensor` はTheorem 5.1と背景形から $O(x_i^{\min(1,\nu)})$ の全残余一様tensor評価を得る。有限face反復によりsmooth/exponential volume-IRFAも成立する。

これらの三補題と適用鎖は一次資料に照合し、複数担当で限定的に独立点検した。一般log-smooth collarだけでは十分でなく、残余normを保存しないrho-smooth射影でも高階fc評価が破れる例を主稿 `rem:log-collar-obstruction` とノートに残す。固定SNC対の入力の証明であり、族一様評価・Part IIIの(H_loc)/(H_anc)を検証したことにはしない。

## 大域距離と測度の現行到達点
`prop:cogram` は十分深い共通カラーで全逆計量を比較し、残余共変ベクトルの一様ノルムを使ってrow errorを抑える。可積分majorantと深い単調cutoffから `thm:contract` のproperな1-Lipschitz全射を得る。`cor:based-ball-approximation` は、加法誤差Kに対して全中心・全半径の閉球GH距離を3K/(2R)以下とする。指定compact集合を潰す選択ではKがその集合に依存する。

LDPはexact-supportへの制限測度の下界を使わず、full collarの正質量compact残余集合をscaled ambient open setへ入れて証明する。残余raw座標はO(1)なのでRで割れば消え、既存のvolume-IRFAで足りる。`lem:level`→`lem:calibration`→`lem:vertex-tightness`→`thm:tail`→`thm:joint` は一面比較・全faceのconditional moment評価・距離上界から直接閉じ、co-Gram下界・LDP下界への依存を除いた。一般重みの角分布の分母は最小entropyのverticesだけの重み総和である。これらの鎖は複数担当で限定的に点検したが、全主張の外部査読・形式証明・新規性確認は未了。

## 曲面正本の全移動基点と固定段階の入力
[現行曲面稿（改訂44）](https://github.com/uedakazushi/surface-lagrangian-torus-fibration/tree/1088f86cf8f0c70c74a1e4caa3b90393ff627067)に保持する `topo:cubical-local-models` と `topo:cubical-moving-blowups` は、成分頂点の $C_{2,d-1}$、二元supportのbook $\mathbb R\times\mathcal Y_{d-2}$、三座標が全て1の頂点の全角 $3\pi/2$ の錐、残る点の平面を、全targetのambient局所閉球から記述する。移動基点が局所錐内で逃げる場合もpositive-starの退出費用を使い、これらの任意の有限基点で全型を尽くす。

同じ全射の歪みが $\delta$ 以下なら、`ke:distortion-to-pointed-balls` により対応する中心・同じ半径の閉球の基点付きGH距離は $3\delta/2$ 以下である。従って `ke:intermediate-moving-classification` は、$a_t\to\infty$、$a_t/R_t\to0$、$R_t\varepsilon_t/a_t\to0$ の下で、actual曲面の任意の移動基点の全部分列極限を四型に分類し、任意の許容尺度・退化列で全型を実現する。既存のcomponent core・変更collarの一様成分錐も保持する。速度未評価の $\varepsilon_t$ に対する条件を除いた任意尺度、tensor収束、極限交換は含まない。証明は曲面repoに保持し、局所錐とGH移送の一般原理の新規性は主張しない。

曲面側の `ke:source-inclusive-fixed-shell` は、sourceを含む固定残余compactとrを先に固定し、同一の非零正則体積frameでmoment $\pm4\pi/(-\log r^2)$ の主項と小rに共通のshell横断費用を得る。異なる正規形のprimitiveの一致や残余periodの消滅は追加しない。`ke:global-clipped-cogram-lower` は固定t,m,Kと任意の非負co-Gram誤差に対する有限不等式とし、誤差消失は最後の対角化でのみ課す。全域ambient上界・下界、Part IV入力、これらの補強と有限targetの指定証明鎖を共同点検した。包括的な全証明・一次文献監査は別に残る。

## 同じ曲面fibrationの相対変更と五次・標準六次の同時実現
曲面正本の `ke:moment-relative-replacement` と `ke:relative-replacement-gh` は、同じcanonical normal moment・anchor cuts・保持cornerの全葉・source nodal neighborhoods・component core/変更collarを保ち、実際のmarked product/cone商と全overlapのwhole-fiber partitionが一致する候補変更を扱う。閉商を先に構成し、射影値の差を $C\eta_{j,t}$、$\eta_{j,t}=(1+\log(N_j+1))/R_t$ で抑える。Reduced葉の同定に $C^1$ 小ささは要求しない。一つの固定marked木系の候補をslow diagonalに沿って与えれば、同じ新しい射影にGH実現を移せる。この条件付き安定性と、atlas候補そのものの実構成を分ける。

`ng8:componentwise-critical-area` は、初期marked familyと固定領域Kの外のsmoothなreductionを入力とし、Kを保つ面積指定を、regionと可動成分のincidence上の正行列のrow/column sumsへ同値に帰着する。Protected mass自体のsmoothnessは不要で、targetからそのmassを引いた自由部分の要求量をsmoothとする。`ng8:strict-area-cuts` の成分別総量とstrict cut条件が有限判定を与え、非孤立rowの要求量を正、孤立rowを零とする。Source annuliで補集合が分断されると総量と個別marginだけでは足りない。各massがaffineなら端点で判定できるが、smoothnessだけでは足りない。`ng8:p0-small-area-flexibility` はactual P0のsource近傍・moment・端を固定した十分小さい総和零の面積変更を構成するが、所定の大きなtargetは含まない。

`ke:anchor-liouville-actions` と `ke:actual-anchor-fan-criterion` は、anchor $q_a=\delta_a$、$M_a=\delta_a-\rho_a<0$ 上の有限critical periodsから、actual Liouville fillingのK4／Petersen作用chartを得る十分条件を与える。Critical period Aの延長は $A(q_a-\rho_a)/M_a$ なので、neckの直線c+pq_aとの一致には同じprimitive/frameでA=pM_a、c=−pρ_aが必要である。残余primitiveの定数差と整数shearも保持する。`ke:anchor-stokes-budget` の総量式はactual clutching relationを入力とし、source固定集合を避ける面積輸送の可解性を自動的に与えない。

五次の `ke:k4-actual-neck-periods` は、正weightsのrow sumsとactual source countsにより両端のaffine critical periodsの整合を有限等式へ帰着する。共通primitive差χとactual meridian/source framingsを保持し、独立な加法定数で切片を修正しない。`ng8:quintic-full-moment` は、解析的cutsとP_jを先に固定し、その内部で初期source葉の全tailsを小さく選んで全momentのstrict cutsを満たす。Source同定S_tとend補正Dは先に固定し、thin葉は引戻し座標で選ぶ。全同一moment集合のconnectorとclipped-depth下界を使うため、葉の幅・微分に依存するGH定数又は追加t閾値を持ち込まない。Source-free bandの `ng8:central-criterion` までの面積affine性はμ=0の固定点を横切る全neckへ適用せず、後者ではwall項を含む面積式を使う。全K2 partitions・中央full nodal neighborhoods・canonical momentsを保持し、最後のfree bandで同じtargetへの相対面積補正を再実行してcoreとの全open germsを合わせる。

`ke:quintic-simultaneous-realization` はwhole-fiber閉商、整数作用star transition、相対GH安定性をつなぎ、各tの同じπでの大域atlas/GHを得る。`ke:eq:quintic-affine-full-transition` は三面に共通する平行移動まで含むGL(3,Z)延長を示し、非対称正weightsも許す。等重みと対称六系の(3,1,1) allocationは存在を保証する。作用atlasのt極限、極限基底のintegral affine構造、cubical距離のHessian・Monge–Ampère性、任意先指定の大source tailsへの相対存在、t連続性・速度は含まない。六次Petersenの標準等重みデータでは、source wallに適合する三対三separatorで内部annulusの累積位置を調整し、二端cutsを満たした。中央parameterの固定後にfull source annuliを保護し、全moment面積輸送とfree anchor bandの再補正を行う。`ke:petersen-full-moment` と `ke:sextic-simultaneous-realization` により、全平行移動を含む同じ射影の作用atlas/GH/測度収束を得る。任意の非等重みや先指定保持集合へ拡張しない。今回の対象限定監査と以前の一般面積輸送・解析入力の確認範囲を区別し、一般的な有限輸送・Moser・Stokes・GH移送・cone extensionの新規性は主張しない。

## 移動基点とlinkの確立範囲
`prop:cone-limits` はcomponent incidencesを保つ正のface領域で積構造を用い、各壁までの距離が2Aを超える場合に、閉A球のambient距離を積の距離と厳密に同定する。これによりmoving-basepointの全部分列極限と各型の実現を証明する。閉star全体のambient積という誤った主張は用いず、短絡・境界同一視の例をノートに保持する。

`prop:link` はcoarse sectionの誤差を一様評価し、truncated angular metricとそのpath metricを復元する。非連結linkの成分間距離は∞とする。復元対象はmetric linkのisometry typeであり、divisor labels・depth weights・genuine geodesic-ray boundaryではない。Bridson–Haefligerのcone構成・復元とLeuzingerの有界加法誤差・radial公式の一次箇所を照合し、標準事項と本稿のKE構成をIntroductionで区別した。これらの指定鎖は複数担当で内部点検したが、全Part Iの包括的監査・網羅的新規性比較は未了である。

## 測度付き極限・体積公式・一様Mellinの到達点
`thm:translation` は $\min_iT_i\to\infty$ の任意のnormal深さ列に対し、全残余空間を含むbounded normal strip上で全変動収束を与える。Metric-IRFAと通常のvolume-IRFAだけで、基点のnormal offsetと残余点が収束すれば、各固定半径のambient閉球上のpointed measured GH収束と押出し測度の全変動収束が従う。Smooth volume-IRFAは不要であり、normal深さの相対速度は指定しない。

`lem:CW` は滑らかな基準曲率との差が有界primitiveの微分となる場合に、有限体積とcompact cutoffから交点数公式を直接証明する。Rochon–Zhang第5節の具体的な背景形とbounded-derivative potentialでこの仮定を検証し、`thm:facemass` の $(2\pi)^n/(n-k)!$ をnormal circleの周期とadjunctionから確認した。Mumfordのsingular Chern–Weil theoremやexact-tail評価は主証明に用いない。

全てのdeeper faceのvolume密度とexact quotient-in-stagesから、normal深さで条件付けた実際の残余測度のsubcritical指数momentsを一様に抑えられる。この評価と通常の全変動収束により、一様Abel–Mellin recursionに追加のweighted-dominator仮定は不要となる。同じconditional moment評価によりactual residual tailを一様に抑え、exact metric-ball tail・joint law・距離Laplace変換にもexponential volume-IRFAを追加しない。単独のface mass一覧だけではincidenceを結論せず、mixed localized transformsの正の最高Abel係数から包含関係を検出する。複素meromorphic continuationには、別途、残余方向に積分可能なjoint polyhomogeneous展開を要求する。

## 公表用の対象範囲とPart IIへの接続
Part I Introductionの主定理・Abstractを本文と照合し、連結な射影多様体、複素次元n≥1、reduced SNC境界、ample log canonical classを共通の対象として明記した。空境界では固定基点coneが一点となり、tailは非空境界で扱う。一般多次数配置にはcomponent-labelled dual complexを用い、超平面配置の単一cell表示を流用しない。

面質量の交点数公式は非正規化体積に対する値であり、LDPの確率正規化とは区別する。確率体積による面質量は主稿 `rem:probability-face-mass` の交点数比となる。Abel recursionの残余parameter一様性はcompact subcritical集合上である。通常volume-IRFAから有理型延長が従わない対数特異性の例は `ex:Abel-not-meromorphic` に証明を置く。

Part II v2.1では、複素periodの復元にfactor/cusp labelsとKähler orientationを保持することをIntroductionと図で明示し、Part Iへの引用を安定した定理ラベルに揃えた。向きだけを忘れるgeneric Torelliは全curve factorsから配置全体の複素共役までの結論である。今回の作業はこの接続の照合であり、Part IIの全Torelli証明の再監査ではない。

一次比較では、Kobayashiの存在定理、Guenancia–Wuの境界比較、Jiang–Shiのsmooth-divisor展開をRochon–Zhangの再帰的入力から区別した。Chambert-Loir–TschinkelのIgusa積分・residue measures・height-ball漸近を比較対象に加え、Mellin係数と面測度を結ぶ一般原理を独自成果とは扱わない。確認版・箇所・未確認点の正本は `research/source-audit.md`。

## 解析的入力とsmooth-divisorの精密誤差
Rochon–Zhang Theorem 5.1はSNC strataの共通指数\(\nu>0\)のfc漸近を与え、Theorem 7.4・7.6のpolyhomogeneous展開と\(x\log x\)の係数はsmooth divisorに限る。Smooth degree-\(e\) hypersurface\(D_e\subset\mathbf P^n\)（\(e>n+1\)、\(n\ge2\)）では\(\widetilde b_e=2(n-1)e/[3(e-n-1)]\)と計算できる。さらにnormal-circle connectionを含むcompatible modelへのtensor誤差は\(C(1+t)e^{-t}\)で、tail積分は\(C(T+2)e^{-T}\)（`cor:RZ-smooth-sharp-IRFA`）。これは一次資料から得られるsmooth boundaryの可積分評価であり、一般SNCの全大域path liftingやactual conifold gluingの証明ではない。五直線のface mass係数はintersectionとGauss–Bonnetから数値検算済み。

## 次の課題

1. **本repoの第一優先：Part Iの公表準備。** 主定理の仮定対応表を起点に、未点検の証明箇所と主要結果の網羅的な先行研究比較を詰める。距離側ではLeuzinger・Bridson–Haefliger、測度側ではChambert-Loir–Tschinkelとの既知の重なりを踏まえ、recursive cusp geometryから実距離球のBusemann phase・tail係数までの貢献を具体化する。内在性・compact基点一様性・gauge・非KE例・K5比較の既存点検を保持し、今回のactual-ball/Abel–Mellin鎖とKE積の対数項の指定証明も内部点検を終えた。これらを未解決事項へ戻さない。標準cone幾何や一般的なresidue-measure原理を独自成果として数えない。
2. **三研究の接続と五次・標準六次同時実現の公表。** 曲面P0・五次と標準等重み六次の同一πによる作用atlas/GH/測度収束・Part IVの最小局所解析の公表準備を共同で進め、最小入力・尺度・距離の範囲を一致させる。Part IV v1.11はcapped下界鎖のresidue規格化・全点Chern式・frame吸収予算・六型・compact最小値原理と固定族での量化を明記し、担当の全鎖実読と別担当の変更式点検を行った。全深部比較の境界上界をparameter一様とする追加仮定は入れない。五次の有限period条件から全moment・全open overlaps・同一πのatlas/GHまでの指定証明は閉じたので未解決へ戻さず、先行研究比較と公表用の依存整理を進める。六次の指定証明鎖も二端cuts・balanced separator・中央freeze・全open接続まで独立点検した。Pille-Schneiderの既知hybrid原子極限との比較を保持し、作用atlasを備えた同じactual射影の実現へ貢献範囲を限定する。任意先指定のfull source tailsは実際の有限cut判定へ戻す。局所protected距離と全曲面ambient距離を区別し、(CP)/(PBE)/(TC)、(H_loc)/(H_anc)は独立の課題とする。
3. **Part III。** (H_loc)のwhole-end localization・parent/refined compatibility、(H_anc)のanchors・portal transport・radial densityをactual metricで確立する。曲面側の手法は検証課題の手掛かりであり、conifold模型・対象・尺度が一致する証明ではない。
4. **Part II。** Controlled parallel push-offを証明するか適用範囲を限定する。一般matroid・Jacobi/scatteringの独立素材は `papers/research-directions.tex` に保持し、核心の監査後に進める。

## 保存・検証
元資料とSHA-256の対応は `research/source-manifest.json`、元資料の監査範囲は `research/source-audit.md` と `research/migration.md`。現行の組版・表示確認と今回の限定的な論理点検は `research/validation.json` を参照する。過去の組版記録を変更後の再実行と混同しない。独立の全証明再検証・外部査読・網羅的新規性確認・Library全履歴との照合は未了である。

## 共通研究原則と保存許可（研究固有方針から独立）
数学的重要性・新規性・理解の深化・応用可能性・正確性・実現可能性を総合して方針を更新する。証明済み・仮定付き・未完成・予想・計算観察を区別し、既知結果と新規貢献、草稿中の証明と今回の監査を分ける。重要な文献は一次資料を照合する。論文は原則日本語LuaLaTeXで、価値ある証明を軽量化のため削らない。ノートは現行知識に整理し、必要な再現コード・入力・証明書を残す。研究の区切りで承諾を求めず通常コミットにより `main` へpushし、長時間では15–30分で保存する。force push・GitHub Actions追加/起動をせず、他者の変更と公開範囲を保持する。Library旧資料を削除せずGitHub移行後の定常二重保存はしない。対象repoを先に保存してからresearch-hubを更新し、数学検証・組版・保存・hub更新は別々に確認する。
