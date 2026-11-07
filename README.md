# AI-DLC ライブ

AI-DLC（AI-Driven Development Life Cycle）で、ネコが遊べるアプリ「CATCHA!」を作っていく記録です。章（Sec）ごとに、ワークフローの各ステージでできた文書を要約して置いています。質問・要件・レビューの指摘などの番号は、すべて残しています。

- アプリのコード：https://github.com/unrcom/catcha
- 記事（Qiita）：[AI-DLC ライブ 0 章](https://qiita.com/unr/items/fbced0d3d1ee891b8a3a)

各ステージのフォルダには、次のファイルがあります。
- `*-questions.md`：AI からの質問と、それへの回答
- `reviews.md`：レビュー役の AI の指摘と、指摘ごとの最後の結果（READY / NOT-READY）
- それ以外：そのステージの成果物

フォルダ名の頭の番号（1.1 など）は、AI-DLC でのステージの番号です。

## Sec 0：ネコが遊べるアプリを作りたい（v0.0.0）

[sec-0/](sec-0/)：PoC に、ラフな画面と仕上げの画面を足したプラン。期間は 2026-11-03 〜 2026-11-05、アプリのタグは `v0.0.0`。
ワークフローの設定と、実行したステージ・省いたステージの一覧は [aidlc-state.md](sec-0/aidlc-state.md) にあります。

### 1.1 intent-capture：やりたいことをまとめる

[sec-0/1.1-intent-capture/](sec-0/1.1-intent-capture/)

| ファイル | 中身 |
|---|---|
| [intent-capture-questions.md](sec-0/1.1-intent-capture/intent-capture-questions.md) | 質問と回答（15 問） |
| [intent-statement.md](sec-0/1.1-intent-capture/intent-statement.md) | 解きたい問題・合格の基準・PoC の範囲 |
| [stakeholder-map.md](sec-0/1.1-intent-capture/stakeholder-map.md) | 関わる人 |
| [reviews.md](sec-0/1.1-intent-capture/reviews.md) | レビューの指摘（R-01〜R-06）と結果 |

### 1.6 rough-mockups：ラフな画面

[sec-0/1.6-rough-mockups/](sec-0/1.6-rough-mockups/)

| ファイル | 中身 |
|---|---|
| [rough-mockups-questions.md](sec-0/1.6-rough-mockups/rough-mockups-questions.md) | 質問と回答（9 問） |
| [wireframes.md](sec-0/1.6-rough-mockups/wireframes.md) | 画面のラフ（S1〜S6） |
| [user-flow.md](sec-0/1.6-rough-mockups/user-flow.md) | 画面の流れ |
| [reviews.md](sec-0/1.6-rough-mockups/reviews.md) | レビューの指摘（R-01〜R-07）と結果 |

### 2.3 requirements-analysis：要件

[sec-0/2.3-requirements-analysis/](sec-0/2.3-requirements-analysis/)

| ファイル | 中身 |
|---|---|
| [requirements-analysis-questions.md](sec-0/2.3-requirements-analysis/requirements-analysis-questions.md) | 質問と回答（8 問） |
| [requirements.md](sec-0/2.3-requirements-analysis/requirements.md) | 機能の要件 FR1〜FR7、品質の要件 NFR1〜NFR6（合格の基準つき） |
| [reviews.md](sec-0/2.3-requirements-analysis/reviews.md) | レビューの指摘（R-01〜R-09。1 回目は NOT-READY）と結果 |

### 2.5 refined-mockups：仕上げの画面

[sec-0/2.5-refined-mockups/](sec-0/2.5-refined-mockups/)

| ファイル | 中身 |
|---|---|
| [refined-mockups-questions.md](sec-0/2.5-refined-mockups/refined-mockups-questions.md) | 質問と回答（6 問） |
| [mockups.md](sec-0/2.5-refined-mockups/mockups.md) | 画面の仕上げ |
| [interaction-spec.md](sec-0/2.5-refined-mockups/interaction-spec.md) | 動きと操作のきまり |
| [design-system-mapping.md](sec-0/2.5-refined-mockups/design-system-mapping.md) | 色と部品 |
| [accessibility-checklist.md](sec-0/2.5-refined-mockups/accessibility-checklist.md) | アクセシビリティの確認項目 |
| [reviews.md](sec-0/2.5-refined-mockups/reviews.md) | レビューの指摘（R-01〜R-11）と結果 |

### 3.5 code-generation：コードを書く

[sec-0/3.5-code-generation/](sec-0/3.5-code-generation/)

| ファイル | 中身 |
|---|---|
| [code-generation-questions.md](sec-0/3.5-code-generation/code-generation-questions.md) | 質問なし。計画の承認がオフだった記録 |
| [code-generation-plan.md](sec-0/3.5-code-generation/code-generation-plan.md) | 書く順番の計画（17 ステップ） |
| [code-summary.md](sec-0/3.5-code-generation/code-summary.md) | 書いたファイルと主な判断 |
| [unit-test-instructions.md](sec-0/3.5-code-generation/unit-test-instructions.md) | テストの動かし方 |
| [reviews.md](sec-0/3.5-code-generation/reviews.md) | レビューの指摘（R-01〜R-07）と結果 |

### 3.6 build-and-test：組み立てて試す

[sec-0/3.6-build-and-test/](sec-0/3.6-build-and-test/)

| ファイル | 中身 |
|---|---|
| [build-and-test-summary.md](sec-0/3.6-build-and-test/build-and-test-summary.md) | 組み立てとテストのまとめ、動作確認で直したこと |
| [test-results.md](sec-0/3.6-build-and-test/test-results.md) | テストと実機での確認の結果 |
| [build-instructions.md](sec-0/3.6-build-and-test/build-instructions.md) | 組み立ての手順 |
| [cross-unit-traceability.md](sec-0/3.6-build-and-test/cross-unit-traceability.md) | 要件と確認の対応 |

## 公開にあたって

各ファイルは、AI-DLC が書いた原文を要約したものです。質問（Q1 など）、要件（FR1.1 など）、レビューの指摘（R-01 など）の番号と出典は、すべて残しています。経緯の記録（監査ログ・ステージの日誌・トレーサビリティの JSON）は除きました。レビューは回ごとのファイルを 1 つにまとめ、指摘ごとの最後の結果を載せています。別のアプリの名前は「別のアプリ」に置き換えています。
