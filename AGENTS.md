# multiscale-kaehler-einstein — 研究・保存指示
2026-11-22 / v1.1

## 入口と正本
- 研究全体の入口は https://github.com/uedakazushi/research-hub 。再開時はhubの該当項目を確認し、最初にこのrepoの `00_research_plan.md`、次に本書、`research/notes.md` と必要な原稿を読む。
- 本研究の現行資料の正本はGitHub `main`。主たる公表用原稿は `papers/multiscale-kaehler-einstein.tex`（本文のある主原稿）であり、節分割可。独立論文は記述的な別名を付け、READMEと研究方針に役割を明記する。
- 一般原則と研究固有の目標を区別する。研究で使う文献、証明、再現入力の正本は当該repoに置く。

## 研究の方針と確実性
1. 数学的重要性・新規性・理解の深化・応用可能性・正確性・実現可能性を総合し、目的と方針を柔軟に修正する。履歴を積み増す代わりに現行資料を整理する。
2. 証明済み・追加仮定付き・証明未完成・予想・計算観察を区別し、仮定・証明の所在・依存関係・未解決箇所を記録する。原稿に証明が存在することは、その証明を今回独立に監査したことと異なる。
3. 先行研究の一次資料を確認し、適用範囲と本研究の貢献をIntroductionに明示する。文献と新規性の未確認事項は憶測で埋めない。他repoの結果を使うときは具体的な定理と仮定を記す。
4. 論文は原則日本語のLuaLaTeX。https://github.com/uedakazushi/research-hub の `papers/paper-template.tex`, `papers/README.md`, `.latexmkrc`, `.vscode/` を参考にする。主原稿を改名するときはinput、分割原稿のTeX root、文献、README、設定も更新する。
5. 研究ノートは現行の着想・例・補題・計算・障害・文献比較を保持する。論文中の十分な証明は複製せず参照する。過去の会話や更新日誌・旧版ZIPを蓄積しない。
6. 誤りの判明時は依存する主張を含めて修正し、ノート・方針・公表原稿・hubの記述を一致させる。

## 三研究の共同編集と証明の正本
- 本repoは固定SNC対・配置補空間のPart I–IIIとシリーズ総説、`kaehler-einstein-degeneration` は退化族の局所一様解析Part IVと条件付き大域枠組Part V、`surface-lagrangian-torus-fibration` はactual KE形式上の曲面fibrationと同じ射影による大域GH実現を担当する。研究方針・記法・依存関係・証明監査を一体で進め、repoや独立論文を機械的に統合しない。
- 他repoの結果は定理ラベル・仮定・規格化・固定する対象・距離の範囲・確認版を `research/notes.md` に記す。必要な定理の変更は証明の正本を先に直し、利用先と総説・hubを追随させる。証明全文を複製しない。
- 固定補空間の空間的blow-downを退化parameterに一様な評価と読み替えない。曲面側の直接scalar/portal証明を、Part IV–Vの(CP)/(PBE)/(TC)やPart IIIの(H_loc)/(H_anc)の検証済み表示へ流用しない。Secondary complex periodsとsymplectic action periodsを同一視しない。
- まずPart IVから曲面側へ渡す局所入力と全域化の非循環性を共同監査し、Part Iの再帰的接続、Part IIのcontrolled push-off、Part IIIのlocalization/anchorsは独立の未解決課題として追う。修正は必要な範囲へ限定し、他研究・並行編集を保持する。

## 保存と検証
- 現行資料だけで再開できるよう、ソース、必要な文献情報、再現コード、入力、証明書を保持する。軽量化を理由に価値ある証明を削らない。古い資料の有効部分を統合するまでは消去しない。
- 研究の区切りでは追加の承諾なしに通常コミットで `main` へpush。長時間作業時は15〜30分で区切り保存する。他の作業者の変更を保護し、force push・GitHub Actionsの追加/起動は行わない。
- `latexmk` と VS Code LaTeX Workshopで組版し、SyncTeXとPDFを `build/` に整合させる。PDF・中間生成物は通常Git追跡しない。実行した数学的点検、計算、組版、pushは別々に報告する。
- GitHub管理後はLibraryへの定常的二重保存/ZIP作成をしない。push不能時は緊急保存する。既存Libraryファイルは明示指示なしに削除しない。

## research-hub 更新義務
1. まず本repoの方針・原稿・ノート・READMEを最新の内容へ整理し、`main`へ保存する。
2. hubの最新READMEとAGENTS.mdを読んで、主要到達点・主張の状態・未解決の核心・次の一手・依存関係・正本・再開先・資料を実際に確認した日を更新する。
3. 詳細todo/証明/履歴はhubに転載しない。実質変更がないときは無用に更新しない。他項目と並行変更を保つ。
4. hubも通常コミットで`main`へ反映し、研究repo保存とhub更新の成否を独立に確認する。失敗した場合は対象と理由を報告する。公開範囲を勝手に変更しない。

## 回収した原資料の扱い
`research/source-manifest.json`と`research/migration.md`で全文・要約・未回収を区別する。移行完了の判定に短い要約を使わない。取得した最新版の訂正・追加仮定を旧稿の強い記述より優先する。保存済みの証明書と今回の再実行を混同しない。
