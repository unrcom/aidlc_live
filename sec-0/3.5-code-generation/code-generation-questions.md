# 3.5 code-generation：質問と回答

質問は 0 問。PoC のプランでは計画の承認（plan approval）がオフのため、計画は確認なしで作られ、そのまま作業に入った。このファイルはその記録。

- 作るもの：iOS・Android 向けの Expo（React Native、TypeScript）アプリと、Supabase のテーブル定義
- 触る場所：package.json・app.json・`app/`（画面）・`src/`（ロジックと部品）・`supabase/`（テーブル定義）・`__tests__/`（テスト）
- テスト：Jest の単体テストと画面テスト、約 30 件（要件ごとに 1 件以上、部品ごとに正常系 1 件以上）
- 技術の選択：アプリは React Native（Expo）、アカウントと記録の保存先は Supabase
