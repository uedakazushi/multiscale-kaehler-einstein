# 現行研究方針：配置補空間の多重スケールKähler–Einstein幾何
更新：2026-11-20 / v1.1

## 研究固有の目標
滑らかな ample SNC pair の負KE計量の無限遠を、第一漸近錐・facewise測度・residual periods・singular conifold cellsの階層として記述する。最優先の核心は、**actual singular arrangement metricの大域pGH収束に必要なwall-compatible lifting**である。

## 原資料と主張の状態
- Part I：2026-08-21 v1.0、Library `Multiscale_KE_Arrangements_I_ja_v10.tex`。bounded-additive cone theorem、face masses、tails/LDPの証明が草稿に記載される。Rochon–Zhangのuniform recursive asymptoticsからの帰結は今回独立に監査していない。
- Part II：同日v1.0、`Multiscale_KE_Arrangements_II_ja_v10_submission.tex`。secondary TorelliとWP completionの証明が原稿に記載されるが、文献と仮定の独立監査は未了。
- Part III：同日v1.2、`Multiscale_KE_Arrangements_III_ja_v12_submission.tex`。explicit conifold models、fixed nodeでのqualitative localization、canonical transverse angle \(8\pi/3\)、residual Torelliを原稿中で証明したと記録する。**Global pGHは条件付き定理・予想で、無条件定理ではない。**
- 移行時点で元の長いTeX本文と計算ZIPのGitHub移植は未完了。GitHubにある各 `papers/*.tex` は原稿の完全な代替ではなく、数学的再構成草稿である。

## 次の課題と着手方法
1. Part III全wall layersのtemplate liftsとkernel connectorsを一様 \(o(R)\) で制御するか、仮定不足を同定する。
2. Part Iのmetric-IRFAをRochon–Zhangの一次資料の仮定へ還元し、exact-fibre liftingを独立監査する。
3. Part IIのsecondary periods・WP completionの全証明を復元し、一般matroidのresidual period mapへ拡張する。
4. 外部入力：Tian–Yau/Yau completeness、Datar–Fu–Song pair-end volume、Rochon–Zhang uniformity、Dumas–Wolf bootstrap等を精査する。

## 正本と論文
主原稿 `papers/multiscale-kaehler-einstein.tex`（Part I）。独立論文 `papers/secondary-periods-torelli.tex`（Part II）、`papers/conifold-localization.tex`（Part III）。ノートは `research/notes.md`。退化族の一様解析の正本は [kaehler-einstein-degeneration](https://github.com/uedakazushi/kaehler-einstein-degeneration)。

## 共通研究原則と保存許可（研究固有方針から独立）
数学的重要性・新規性・理解の深化・応用可能性・正確性・実現可能性を総合して方針を更新する。証明済み・仮定付き・未完成・予想・計算観察を区別し、既知結果と新規貢献、草稿中の証明と今回の監査を分ける。重要な文献は一次資料を照合する。論文は原則日本語LuaLaTeXで、価値ある証明を軽量化のため削らない。ノートは現行知識に整理し、必要な再現コード・入力・証明書を残す。研究の区切りで承諾を求めず通常コミットにより `main` へpushし、長時間では15–30分で保存する。force push・GitHub Actions追加/起動をせず、他者の変更と公開範囲を保持する。Library旧資料を削除せずGitHub移行後の定常二重保存はしない。対象repoを先に保存してからresearch-hubを更新し、数学検証・組版・保存・hub更新は別々に確認する。
