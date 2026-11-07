# 3.6 build-and-test：組み立ての手順

## 必要なもの

Node.js と npm。iOS シミュレータなら Xcode、Android エミュレータなら Android Studio。実機なら Expo Go か開発ビルド。Supabase のプロジェクト。

## 手順

1. `npm install`
2. Supabase でプロジェクトを作り、SQL エディタで `supabase/migrations/0001_records.sql` を実行する
3. `.env.example` をコピーして `.env` を作り、`EXPO_PUBLIC_SUPABASE_URL`（`https://` で始まる）と `EXPO_PUBLIC_SUPABASE_ANON_KEY` を書く
4. PoC では、Supabase の「Confirm email」をオフにすると、登録してすぐホームに進める
5. `.gitignore` に `.env` と `node_modules/` を入れてから git で管理する

## 組み立てと起動

| 目的 | コマンド |
|---|---|
| 型の確かめ | `npx tsc --noEmit` |
| バンドル（組み立てが通るか） | `npx expo export --platform ios --platform android --output-dir dist` |
| 起動 | `npm run start`（iOS は `npm run ios`、Android は `npm run android`） |
| テスト | `npx jest __tests__` |

## よくあるつまずき

- 起動してすぐ Supabase のエラー：`.env` がない・空・`https://` でない。直して `npm run start -- --clear`
- 登録してもホームに進まない：「Confirm email」がオン
- パッケージは `npx expo install <名前>` で入れる。`expo-av` は SDK 58 では使えない（音は `expo-audio`）
- `ios/`・`android/` は `expo prebuild` などで作られる。作り直せるので git には入れない
