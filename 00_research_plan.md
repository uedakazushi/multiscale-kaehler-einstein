# 現行研究方針：配置補空間の多重スケールKähler–Einstein幾何
更新：2026-11-22 / v1.4（Part I v1.3）

## 研究固有の目標と入口
固定配置補空間の距離錐・測度漸近、secondary periods・Torelli・WP、conifold gluingを研究する。Part I–IIIの全文と必要な証明を現行原稿に保持し、退化族・actual Lagrangian実現との接続を定理単位で検証する。達成基準は、条件付きの解析段階を隠さず、正本の全文と本ノートだけから入力・適用範囲・残る核心を追えることである。

## 三研究を一体で進める方針
| 正本 | 担当する結果 |
| --- | --- |
| 本repo | 固定SNC対・配置補空間のPart I–III、全体の数学的総説 |
| [kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration) | 退化族の局所一様解析Part IV、(CP)＋(PBE)付き大域枠組Part V |
| [surface-lagrangian-torus-fibration](https://github.com/uedakazushi/surface-lagrangian-torus-fibration) | Actual KE Lagrangian fibrationと同じ射影による全曲面GH実現、別立ての作用atlas問題 |

研究・編集・証明監査は共同で進める。対象と主要定理が異なるためrepoと論文はこの責任分担を保ち、総説は入口と定理の接続を担う。論文の分割・統合は公表価値と論理的まとまりに基づき判断し、同じ証明を複製しない。依存定理の仮定・尺度・距離の範囲・確認版を[ノート](research/notes.md)に集約し、入力の修正は正本→利用先→総説・hubの順に反映する。

固定成分は $H_i\simeq\mathbf P^2$ から $d-1$ 本の直線を除いた補空間である。Part Iの固定空間の $R\to\infty$ を $t\to0$ の族一様性へ読み替えない。Part IIの残余複素periodは第二作用積分と異なる。曲面側の直接大域証明があっても、(CP)/(PBE)/(TC)や(H_loc)/(H_anc)自体の検証状況は変えない。同じ曲面fibrationで作用atlasとGHを同時実現する問題も別に残す。

## 論文と証明の状態
- `papers/multiscale-kaehler-einstein.tex`：主たる公表用原稿Part I v1.3、50頁。距離錐・face masses・tails/LDP。Mellinの二重torus係数訂正とweighted uniform integrabilityを保持する。再帰的接続は同じfiberの端点を結ぶambient曲線を用いる。固定SNCの三補題に加え、全射な距離収縮と全中心・全半径の閉球近似、ambient LDP下界、Busemannからexact tailへの証明を補強・点検した。
- `papers/secondary-periods-torelli.tex`：Part II、28頁。Torelli・finite period closure・branch separationを保持。一般secondary WP completionにはcontrolled parallel push-offを仮定する。
- `papers/conifold-localization.tex`：Part III、57頁。algebraic models、positive model pGH、abstract gluing、residual Torelli。Actual localizationとactual global pGHは(H_loc)+(H_anc)に依存する。旧ノートの「fixed node局所化を無条件に証明済み」との記述を最新版の条件付き化より優先しない。
- `papers/series-overview.tex`：五篇と曲面実現の関係・定理状態・共同監査順、v1.3、11頁。五次の(CP)も本稿で引用するPart IVの経路では(TC)付きであり、Part Vのactual直径帰結には(CP)＋(PBE)が必要。曲面側の直接経路と区別する。

## 固定SNC入力の確立範囲
主稿 `lem:SNC-compatible-collars` は、元の実有向blow-up上の固定Hermitian normsを用い、全strataのcollarsと全normal line bundleのproduct connectionsを次元順に同時構成する。残余の深さの保存、circle-equivariance、quotient-in-stagesを厳密に保つ。`lem:fc-collar-transfer` はRochon–Zhangの延長Ξと選んだ射影の差、およびHessianの差を、任意Nに対し $x_i^N C^\infty_{\rm fc}$ と評価する。`lem:RZ-collar-tensor` はTheorem 5.1と背景形から $O(x_i^{\min(1,\nu)})$ の全残余一様tensor評価を得る。有限face反復によりsmooth/exponential volume-IRFAも成立する。

これらの三補題と適用鎖は一次資料に照合し、複数担当で限定的に独立点検した。一般log-smooth collarだけでは十分でなく、残余normを保存しないrho-smooth射影でも高階fc評価が破れる例を主稿 `rem:log-collar-obstruction` とノートに残す。固定SNC対の入力の証明であり、族一様評価・Part IIIの(H_loc)/(H_anc)を検証したことにはしない。

## 大域距離と測度の現行到達点
`prop:cogram` は十分深い共通カラーで全逆計量を比較し、残余共変ベクトルの一様ノルムを使ってrow errorを抑える。可積分majorantと深い単調cutoffから `thm:contract` のproperな1-Lipschitz全射を得る。`cor:based-ball-approximation` は、加法誤差Kに対して全中心・全半径の閉球GH距離を3K/(2R)以下とする。指定compact集合を潰す選択ではKがその集合に依存する。

LDPはexact-supportへの制限測度の下界を使わず、full collarの正質量compact残余集合をscaled ambient open setへ入れて証明する。残余raw座標はO(1)なのでRで割れば消え、既存のvolume-IRFAで足りる。`lem:level`→`lem:calibration`→`lem:vertex-tightness`→`thm:tail`→`thm:joint` は一面比較と距離上界から直接閉じ、co-Gram下界・LDP下界への依存を除いた。一般重みの角分布の分母は最小entropyのverticesだけの重み総和である。これらの鎖は複数担当で限定的に点検したが、全主張の外部査読・形式証明・新規性確認は未了。

## 解析的入力とsmooth-divisorの精密誤差
Rochon–Zhang Theorem 5.1はSNC strataの共通指数\(\nu>0\)のfc漸近を与え、Theorem 7.4・7.6のpolyhomogeneous展開と\(x\log x\)の係数はsmooth divisorに限る。Smooth degree-\(e\) hypersurface\(D_e\subset\mathbf P^n\)（\(e>n+1\)、\(n\ge2\)）では\(\widetilde b_e=2(n-1)e/[3(e-n-1)]\)と計算できる。さらにnormal-circle connectionを含むcompatible modelへのtensor誤差は\(C(1+t)e^{-t}\)で、tail積分は\(C(T+2)e^{-T}\)（`cor:RZ-smooth-sharp-IRFA`）。これは一次資料から得られるsmooth boundaryの可積分評価であり、一般SNCの全大域path liftingやactual conifold gluingの証明ではない。五直線のface mass係数はintersectionとGauss–Bonnetから数値検算済み。

## 次の課題
1. **共通の最優先監査。** Part IVのcapped volume・full-triple・closed-corner・固定成分収束から曲面側のsame-map大域証明へ渡す仮定を照合する。局所protected距離と全曲面ambient距離を分け、(CP)/(PBE)/(TC)経路へ循環しないことを確認する。
2. **Part I。** 距離上下界・SNC入力・ambient LDP・Busemannからexact tailへの鎖を限定的に点検した。次は `thm:translation` の測度付き距離収束とbasepoint/ballの量化、`lem:CW`→`thm:facemass` の規格化・一次資料、Abel–Mellinのweighted uniform integrabilityを順に点検する。主要結果の先行研究比較も進め、新規性は未確認の部分を明示する。
3. **Part III。** (H_loc)のwhole-end localization・parent/refined compatibility、(H_anc)のanchors・portal transport・radial densityをactual metricで確立する。曲面側の手法は検証課題の手掛かりであり、conifold模型・対象・尺度が一致する証明ではない。
4. **Part II。** Controlled parallel push-offを証明するか適用範囲を限定する。一般matroid・Jacobi/scatteringの独立素材は `papers/research-directions.tex` に保持し、核心の監査後に進める。

## 保存・検証
元資料とSHA-256の対応は `research/source-manifest.json`、元資料の監査範囲は `research/source-audit.md` と `research/migration.md`。現行の組版・表示確認と今回の限定的な論理点検は `research/validation.json` を参照する。過去の組版記録を変更後の再実行と混同しない。独立の全証明再検証・外部査読・網羅的新規性確認・Library全履歴との照合は未了である。

## 共通研究原則と保存許可（研究固有方針から独立）
数学的重要性・新規性・理解の深化・応用可能性・正確性・実現可能性を総合して方針を更新する。証明済み・仮定付き・未完成・予想・計算観察を区別し、既知結果と新規貢献、草稿中の証明と今回の監査を分ける。重要な文献は一次資料を照合する。論文は原則日本語LuaLaTeXで、価値ある証明を軽量化のため削らない。ノートは現行知識に整理し、必要な再現コード・入力・証明書を残す。研究の区切りで承諾を求めず通常コミットにより `main` へpushし、長時間では15–30分で保存する。force push・GitHub Actions追加/起動をせず、他者の変更と公開範囲を保持する。Library旧資料を削除せずGitHub移行後の定常二重保存はしない。対象repoを先に保存してからresearch-hubを更新し、数学検証・組版・保存・hub更新は別々に確認する。
