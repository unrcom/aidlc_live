# Sec 0：ワークフローの設定と進み方

- 最初の依頼：ネコが遊べるアプリを作りたい。YouTube のネコ動画は、ネコが触ると止まる・スキップする・別の動画に移ってしまう。ネコが熱中できるようにしたい
- 種類：新しく作る（Greenfield）
- プラン：`poc` に rough-mockups と refined-mockups を足した、自分用のプラン
- 期間：2026-11-03 〜 2026-11-05
- 深さ（Depth）：Minimal／テストの量（Test Strategy）：Minimal
- 計画の承認（plan approval）：オフ／チェックの方針（Guard Policy）：オフ（どちらも poc の既定）

## ステージ

| フェーズ | 実行したステージ | 省いたステージ |
|---|---|---|
| Initialization | workspace-scaffold、workspace-detection、state-init | — |
| Ideation | 1.1 intent-capture、1.6 rough-mockups | market-research、feasibility、scope-definition、team-formation、approval-handoff |
| Inception | 2.3 requirements-analysis、2.5 refined-mockups | reverse-engineering（新規のため）、practices-discovery、user-stories、domain-design、units-generation、contract-design、delivery-planning |
| Construction | 3.5 code-generation、3.6 build-and-test | functional-design、nfr-requirements、nfr-design、infrastructure-design、ci-pipeline |
| Operation | — | すべて（deployment-pipeline、environment-provisioning、deployment-execution、observability-setup、incident-response、performance-validation、feedback-optimization） |

承認のときの変更依頼（Request Changes）：6 回。
