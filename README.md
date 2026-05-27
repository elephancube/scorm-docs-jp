# scorm-docs-jp

**SCORM 仕様書 日本語訳プロジェクト（非公式）**

ADL Initiative が発行する SCORM (Sharable Content Object Reference Model) 仕様書を、LMS 開発者・SCORM コンテンツ作成者などの技術者向けに日本語訳したものです。

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## 収録バージョン

| バージョン | ステータス | 場所 |
|---|---|---|
| **SCORM 1.2** | v1.0.0 / 公開中 | [scorm-1.2/](scorm-1.2/) |
| SCORM 2004 | 未着手 | — |

GitHub Pages を有効化している場合、各バージョンの `index.html` から個別文書へアクセスできます。

## リポジトリ構成

```
scorm-docs-jp/
├── README.md             プロジェクト全体の概要（このファイル）
├── LICENSE               CC BY 4.0 — リポジトリ全体に適用
├── NOTICE                ADL 原典クレジット・SCORM 商標・免責
├── CHANGELOG.md          リポジトリの変更履歴
├── index.html            リポジトリトップのハブページ（GitHub Pages 用）
└── scorm-1.2/            SCORM 1.2 関連ドキュメント
    ├── index.html          SCORM 1.2 ランディング
    ├── scorm_overview_ja.html
    ├── scorm_cam_ja.html
    ├── scorm_rte_ja.html
    ├── scorm_addendums_ja.html
    └── source/             原典 PDF（参照用、ADL 著作物）
```

将来 SCORM 2004 等の翻訳を追加する場合は、同レベルに `scorm-2004/` ディレクトリを作成して同じ構造で配置します。

## SCORM 1.2 の収録ドキュメント

| 原典 PDF | 日本語訳 HTML | 概要 |
|---|---|---|
| `SCORM_1.2_Overview.pdf` | [scorm-1.2/scorm_overview_ja.html](scorm-1.2/scorm_overview_ja.html) | SCORM 全体像。Asset / SCO / Content Aggregation の概念導入、ADL の背景、LMS モデル。 |
| `SCORM_1.2_CAM.pdf` | [scorm-1.2/scorm_cam_ja.html](scorm-1.2/scorm_cam_ja.html) | Content Aggregation Model。コンテンツ・モデル、メタデータ (IEEE LOM)、コンテンツ・パッケージング (IMS)。 |
| `SCORM_1.2_RunTimeEnv.pdf` | [scorm-1.2/scorm_rte_ja.html](scorm-1.2/scorm_rte_ja.html) | Run-Time Environment。Launch、API、Data Model、エラーコード。 |
| `SCORM_1.2_Addendums.pdf` | [scorm-1.2/scorm_addendums_ja.html](scorm-1.2/scorm_addendums_ja.html) | 17 件のエラータ（2002 年 1 月）。CAM / RTE の修正箇所を FROM/TO で記載。 |

### 読み順の推奨

1. **Overview** — SCORM が何を解決するための規格か、用語の定義から把握する。
2. **CAM** — コンテンツのパッケージ構造とメタデータの仕様。
3. **RTE** — LMS と SCO 間の API およびデータモデル。実装の中核。
4. **Addendums** — 上記 3 冊への正誤表。CAM / RTE 内には Addendums への相互参照リンクが埋め込まれており、該当箇所から直接ジャンプできます。

## 翻訳方針

技術仕様書としての参照性を最優先にしています。

- **英語のまま残す要素**: API 関数名 (`LMSInitialize("")` 等)、データモデル要素 (`cmi.core.lesson_status` 等)、エラーコード、データ型 (`CMIString255` 等)、語彙値 (`"passed"`, `"browse"` 等)。これらは LMS 実装や他言語ドキュメントとの参照性を保つために英語を維持し、`<code>` でマークアップしています。
- **専門用語**: 標準的な英語形がある語（API / SCO / LMS 等）は安易にカタカナに直さず、初出時に「Sharable Content Object (SCO)」のようにフルスペルとの併記を行ったうえで以降は略語を使用しています。
- **文体**: 「〜である」「〜する」調。冗長な敬体は避けています。
- **構造**: 原典のセクション番号・階層を維持し、`id="sec-X-Y-Z"` 形式の見出し ID で個別 URL 参照が可能です。
- **図版**: SVG で再描画し、ラベルは日本語化しています。ただし API 名・要素名は図中でも英語のままです。
- **コード**: JavaScript やプソイドコードは原典のまま保持し、コメントのみ日本語に置換しています。
- **訳注**: 原典の typo（例: cmi.interactions 章の誤ったエラーコード 205）など特記事項は、本文末尾に小さく注釈を付与し、Addendums の該当箇所へリンクしています。

## ライセンス

- **翻訳成果物**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.ja)
  - クレジット表示と本リポジトリへのリンクを行えば、商用利用を含めて自由に利用・改変・再配布が可能です。
  - 詳細は [LICENSE](LICENSE) を参照してください。
- **原典 PDF (`scorm-1.2/source/` 配下)**: Copyright (c) 2001-2002 Advanced Distributed Learning Initiative. All rights reserved.
  - 本リポジトリは参照用に同梱しているのみで、利用条件は ADL の指示に従ってください。

## 免責 / 無保証

本翻訳は **「現状のまま (AS IS)」** で提供される非公式の日本語訳であり、いかなる保証も付帯しません。誤訳・解釈相違・最新版との不一致を含む可能性があります。

**LMS や SCORM コンテンツの実装にあたっては、必ず ADL が発行する原典 PDF を参照してください。本翻訳と原典に矛盾がある場合、原典の記述が優先します。**

「SCORM」は ADL の商標です。本翻訳は ADL によって承認・支援されたものではなく、ADL とは無関係に作成された非公式の翻訳です。ADL からの要請があれば、本リポジトリの内容を速やかに修正・削除します。

## クレジット

- **翻訳**: 株式会社エレファンキューブ (Elephancube Inc.) — info@elephancube.co.jp
- **翻訳支援**: Anthropic Claude（Claude Code / Opus 4.7 を用いた人間との共同作業）
- **原典**: Advanced Distributed Learning Initiative, 2001-2002

## フィードバック

誤訳の指摘・改善提案は GitHub Issues、もしくは info@elephancube.co.jp までご連絡ください。Pull Request も歓迎します。

## 関連リンク

- [ADL Initiative (現 ADL Net)](https://adlnet.gov/) — SCORM の発行元
- [SCORM 1.2 解説 (scorm.com)](https://scorm.com/scorm-explained/business-of-scorm/scorm-versions/) — 各 SCORM バージョンの歴史的位置づけ
