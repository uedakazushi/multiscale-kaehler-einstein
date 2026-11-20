# 現行研究方針：配置補空間の多重スケール Kähler–Einstein 幾何
2026-11-20 / v1.0

## 研究固有の目標
滑らかな ample SNC pair の完備負KE計量の無限遠を、第一漸近錐・metric-measure face data・残差曲線のperiod・singular contractionのcanonical metric cellから記述する。最優先は**actual singular arrangement metricに対する大域的pGH収束の証明**である。局所定理とwall-compatible family-uniform liftingを区別する。

## 現時点の主要入力と主張の状態
- Part I：2026-08-21日本語草稿 v1.0（旧Library名 `Multiscale_KE_Arrangements_I_ja_v10.tex`）。ample SNC pairのbounded-additive cone、face masses、tail/LDPを原稿中で主張し証明を記載。Rochon–Zhangのrecursive asymptoticsから必要な一様評価を本当に導けるか、独立の一次資料照合・証明監査は未了。
- Part II：2026-08-21 v1.0（`Multiscale_KE_Arrangements_II_ja_v10_submission.tex`）。secondary periods、Torelli、residual WP completion。原稿中に証明あり。一次文献と全仮定を新たに検証した状態ではない。
- Part III：2026-08-21 v1.2（`Multiscale_KE_Arrangements_III_ja_v12_submission.tex`）。explicit conifold models、fixed arrangement / fixed nodeのqualitative local localization、canonical \(8\pi/3\) cell、single-node residual Torelliを原稿中で定理として扱う。**global pGHは条件付き定理と予想であり、無条件定理ではない。** 前稿での過大な主張を引き継がない。
- 外部文献の未検証部分：Tian–Yau/Yau completeness、Datar–Fu–Song pair-end volume argument、Rochon–Zhang uniformity、Dumas–Wolfからの全階Hessian bootstrap、localized Chern–Lu cutoff。独立の証明監査を要する。

## 最優先課題
1. Part IIIの全wall layersに対しtracked template liftsとkernel connectorsを (o(R)) で一様制御するか、反例/仮定不足を同定する。
2. Part Iのmetric-IRFAへの外部入力を一次資料の正確な定理・重み・uniformityと照合し、粗等長性の帰納法を厳密監査する。
3. 研究ノートに残るgeneral matroid/secondary WP/singular face massの問題を重要度順に選択する。独立した公表価値を優先する。

## 論文・ノートと依存
- `papers/multiscale-kaehler-einstein.tex`：Part I、主原稿。
- `papers/secondary-periods-torelli.tex`：Part II、独立論文。
- `papers/conifold-localization.tex`：Part III、独立論文。
- `research/notes.md`：原稿外の現行課題と障害。証明は論文を参照。
- 退化族への応用は [kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration) の正本で管理する。両研究の定理を自動的に同一視しない。

## 共通研究原則・保存許可（研究固有の方針ではない）
数学的重要性・新規性・理解の深化・応用可能性・正確性・実現可能性を総合し方針を更新する。証明済み・追加仮定付き・未完成・予想・計算観察を区別し、既知結果と本研究を分け、重要な文献は一次資料で検証する。日本語LuaLaTeXで本文と十分な証明を保持し、ノートは現行の有効知識だけに整理する。計算・証明書・再現入力を残し、過去版や作業ログは正本にしない。研究の区切りには承諾を求めず通常コミットで `main` にpushし、15〜30分を目安に区切って保存する。force pushとActionsの追加/起動をせず並行変更を守る。既存Library資料を削除せず、GitHub管理後の定常的なLibrary二重保存は行わない。対象repoを先に保存してからresearch-hubを更新し、双方の反映状況を別々に確認する。検証・組版・保存の実施状態は混同しない。
