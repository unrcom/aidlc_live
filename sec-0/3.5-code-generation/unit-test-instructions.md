# 3.5 code-generation：テストの動かし方

道具は Jest（プリセット `jest-expo`）と `@testing-library/react-native`。`npm install` のあと、次のコマンドで動かす。Supabase の本物の接続は使わないので、環境変数は要らない。

```bash
npx jest __tests__
```

型の確かめは `npx tsc --noEmit`。

| テストのファイル | 確かめる要件 |
|---|---|
| `domain/records.test.ts` | FR5.2、FR6.1 |
| `data/migration.test.ts` | NFR5 |
| `data/authRepository.test.ts` | FR1.1、FR1.2、FR1.4 |
| `data/recordRepository.test.ts` | FR5.3、FR6.1、FR6.2 |
| `data/pendingQueue.test.ts` | FR7.1〜FR7.4、NFR4、FR1.3 |
| `data/settingsStore.test.ts` | FR4.2、FR2.6 |
| `domain/playSession.test.ts` | FR4.1、FR4.3、FR4.4、FR4.5、FR5.1、FR3.2 |
| `domain/alphaGesture.test.ts` | FR3.1、FR3.4 |
| `domain/validation.test.ts` | FR1.1 |
| `ui/*.test.tsx` | FR1.2〜FR1.4、FR2.5、FR2.6、FR3.2、FR4.2、FR4.4、FR5.2、FR6.1〜FR6.3、FR7.1、FR7.3、FR7.4、NFR6 |

- 量は Minimal：要件ごとに 1 件以上、部品ごとに正常系 1 件以上。カバレッジの下限はない（poc）
- モック：Supabase の `createClient`、NetInfo（オンライン・オフライン）、AsyncStorage
- テストの中のアカウントはテスト用の値だけを使い、本物のアカウントは使わない
