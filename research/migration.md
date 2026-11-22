# 原資料の移行と検証

現行の記録整理：2026-11-23 / v1.1。移行元の同定と現在のソース検査を区別する。

2026-11-20。Libraryの `Multiscale_KE_Geometry_I-V_ja_v1_source_and_pdfs.zip`（2026-08-31）を取得した。これは旧配置補空間三部作と旧退化二部作を再監査・統合した五篇連作である。元資料のREADME・数学的監査と本文の仮定を照合し、短い再構成稿を全文のTeXへ置換した。旧稿への誤り訂正・条件付き化を引き継ぐ。元Libraryファイルは削除していない。

ソースの対応、バイト数、SHA-256は `source-manifest.json`。五篇統合稿のTeX本文は移行時点で元ファイルとのバイト単位一致を確認した。その後の数学的な追記により現行ファイルは元バイト列と異なる。現行manifestでは、記録がある `source_sha256` を元資料のハッシュ、`recovered_record` を移行・初期編集時に保存されていたsnapshot、`current_source` を確認日に実ファイルから計算したSHA-256・バイト数・Git blob hashとして区別する。`recovered_record` の全値が元bundleのバイト列であるとは主張せず、未記録の元hashを推測しない。2026-11-23には全5ファイルの現在の値を実計算したが、Library資料を再取得したのではない。追加で取得したpost-trilogy v2.2は研究素材としてresearch-directions.texへ保持し、現行の追加仮定の注意書きを冒頭に加えた。Part I–IIIと総説の正本はmultiscale-kaehler-einstein、Part IV–Vと五つの補助スクリプトの正本はkaehler-einstein-degeneration。元の統合PDFと旧版ZIPはGitへ重複保存しない。移行とhash照合だけで、新しい定理の証明や文献の再監査を実施したことにはしない。

## 移行時に行った組版

リポジトリルートから `latexmk`。LuaLaTeX、PDF/SyncTeXはbuild/に出力する。移行時にはTeX Live 2026で実行したと記録されている。現在の組版engineと実行範囲は `validation.json` を参照する。フォントキャッシュが書込不可の環境では、書込可能なTEXMFCACHE・TEXMFVARを指定する。最終頁数・参照と引用・警告の確認結果は検証結果に記す。VS Code UIの検証は実施していない。

## 完全移行の範囲

本記録は取得できた統合版の全文移行を示す。Libraryの全履歴・全旧稿だけに残る内容の網羅的照合は未了。退化研究の旧v0.12の16 scriptsは別資料であり、統合版の五つの検査で全てを代替したとは扱わない。Post-trilogy v2.2は回収済みだが、全旧版の固有内容を網羅的に照合したわけではない。旧資料の独自内容を回収する作業と、現行稿の数学的な未解決問題は別である。

移行時の全主原稿の最終logに未解決参照・引用とoverfull/underfull boxはなし。各原稿の冒頭・中間・末尾を描画して確認した。全頁の目視監査は未実施。フォント置換・scale・PDF bookmarkの数式警告は残る。VS Codeは主原稿だけをroot候補とする設定を検査したがUI操作は未検証。

## 回収済み旧資料の再確認

五篇統合版の第I–III篇と総説、およびpost-trilogy v2.2から移した研究ノートの計5ファイルについて、取り込み直後のファイルSHA-256を移行時の一覧と照合して一致を確認した。後の数学的追記が入った原稿は、現行SHA-256と元資料のハッシュを別に管理する。v2.2のJacobi/scattering・一般matroidの素材は `papers/research-directions.tex` に収録済み。統合前の各版との証明単位の照合は残る。
