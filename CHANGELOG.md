# Changelog

本リポジトリの変更履歴です。フォーマットは [Keep a Changelog](https://keepachangelog.com/ja/1.1.0/) に準拠し、バージョニングは [Semantic Versioning](https://semver.org/lang/ja/) に従います。

## [1.0.0] - 2026-05-27

### Added

- SCORM 1.2 仕様書 4 冊の日本語訳 HTML を初回公開:
  - `scorm_overview_ja.html` — The SCORM Overview
  - `scorm_cam_ja.html` — The SCORM Content Aggregation Model
  - `scorm_rte_ja.html` — The SCORM Run-Time Environment
  - `scorm_addendums_ja.html` — The SCORM Addendums (Version 2.0, January 2002)
- CAM および RTE の本文中に、対応する Addendums 各項目への相互参照リンクを埋め込み。
- 原典 PDF 4 冊を `source/` 配下に同梱（参照用）。
- GitHub Pages 用ランディングページ `index.html`。
- ライセンス (CC BY 4.0) および原典クレジット (NOTICE) を整備。

### 翻訳品質

- 訳語選択は SCORM 1.2 の用語集に基づく。API 関数名・データモデル要素・エラーコード・データ型・語彙値は英語のまま `<code>` でマークアップ。
- 図版は SVG で再描画し、ラベルを日本語化（識別子は英語のまま）。
- セクション番号・階層は原典を維持し、`id="sec-X-Y-Z"` 形式で個別参照可能。
- 初回公開前にセルフレビューと再レビューを実施し、計 9 件の指摘事項を反映済み。
