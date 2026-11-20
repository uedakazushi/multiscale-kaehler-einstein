# 現行研究方針：配置補空間の多重スケールKähler–Einstein幾何
更新：2026-11-20 / 原資料全文移行

## 研究固有の目標と入口
固定配置補空間の距離錐・測度漸近、secondary periods・Torelli・WP、conifold gluingを研究する。原資料の2026-08-31五篇連作v1.0を回収し、短い再構成稿を全文TeXに置換した。旧8月21日三部作より新しい再監査稿を現行とする。

## 論文と証明の状態
- `papers/multiscale-kaehler-einstein.tex`：Part I、39頁。距離錐・face masses・tails/LDP。Mellinの二重torus係数訂正とweighted uniform integrabilityを保持する。
- `papers/secondary-periods-torelli.tex`：Part II、28頁。Torelli・finite period closure・branch separationを保持。一般secondary WP completionにはcontrolled parallel push-offを仮定する。
- `papers/conifold-localization.tex`：Part III、57頁。algebraic models、positive model pGH、abstract gluing、residual Torelli。Actual localizationとactual global pGHは(H_loc)+(H_anc)に依存する。旧ノートの「fixed node局所化を無条件に証明済み」との記述を最新版の条件付き化より優先しない。
- `papers/series-overview.tex`：総説9頁。Part IV–Vの正本は[退化研究](https://github.com/uedakazushi/kaehler-einstein-degeneration)。

## 次の課題
1. (H_loc)のwhole-end localizationとparent/refined compatibility、(H_anc)のanchors・portal transport・radial densityをactual metricで確立する。
2. Part IIのcontrolled parallel push-offを証明するか、適用範囲を限定する。
3. Part Iの外部解析入力とweighted uniform integrability、一般matroidへの拡張を監査する。
4. 回収したpost-trilogy v2.2のJacobi/scattering・一般matroidの素材を `papers/research-directions.tex` に保持した。旧版のlocalization証明済み表示には現行仮定の注意を付記。Library全履歴の網羅的監査は未了。

## 保存・検証
元資料とSHA-256の対応は `research/source-manifest.json`、数学的再監査の原記録は `research/source-audit.md`、移行範囲と今回の検証は `research/migration.md`。5本をLuaLaTeXで組版した。数学の独立再証明・外部査読・新規性の再確認とは別である。

## 共通研究原則と保存許可（研究固有方針から独立）
数学的重要性・新規性・理解の深化・応用可能性・正確性・実現可能性を総合して方針を更新する。証明済み・仮定付き・未完成・予想・計算観察を区別し、既知結果と新規貢献、草稿中の証明と今回の監査を分ける。重要な文献は一次資料を照合する。論文は原則日本語LuaLaTeXで、価値ある証明を軽量化のため削らない。ノートは現行知識に整理し、必要な再現コード・入力・証明書を残す。研究の区切りで承諾を求めず通常コミットにより `main` へpushし、長時間では15–30分で保存する。force push・GitHub Actions追加/起動をせず、他者の変更と公開範囲を保持する。Library旧資料を削除せずGitHub移行後の定常二重保存はしない。対象repoを先に保存してからresearch-hubを更新し、数学検証・組版・保存・hub更新は別々に確認する。
