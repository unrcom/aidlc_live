# 3.6 build-and-test：要件と作ったファイルの対応

ユニットに分けず、1 つのまとまりで作った。要件の ID ごとに、作ったファイルを示す（作ったステージはすべて code-generation）。
**判定：合格**（36 件すべてに対応あり）

| ID | ファイル | ID | ファイル |
|---|---|---|---|
| FR1.1 | `src/data/authRepository.ts` | FR4.4 | `src/domain/playSession.ts` |
| FR1.2 | `app/login.tsx` | FR4.5 | `__tests__/domain/playSession.test.ts` |
| FR1.3 | `src/data/pendingQueue.ts` | FR5.1 | `src/domain/playSession.ts` |
| FR1.4 | `src/ui/AuthForm.tsx` | FR5.2 | `app/result.tsx` |
| FR2.1 | `src/ui/PlayField.tsx` | FR5.3 | `src/data/recordRepository.ts` |
| FR2.2 | `src/ui/toyMotion.ts` | FR6.1 | `app/records.tsx` |
| FR2.3 | `src/ui/PlayField.tsx` | FR6.2 | `src/data/recordRepository.ts` |
| FR2.4 | `src/ui/TouchSurface.tsx` | FR6.3 | `__tests__/ui/records.test.tsx` |
| FR2.5 | `__tests__/ui/play.test.tsx` | FR7.1 | `src/data/pendingQueue.ts` |
| FR2.6 | `src/ui/useToySounds.ts` | FR7.2 | `src/data/pendingQueue.ts` |
| FR2.7 | `app/play.tsx` | FR7.3 | `src/ui/SaveStatus.tsx` |
| FR3.1 | `src/domain/alphaGesture.ts` | FR7.4 | `__tests__/ui/home.test.tsx` |
| FR3.2 | `src/ui/OwnerMenu.tsx` | NFR1 | `app/play.tsx` |
| FR3.3 | `app/result.tsx` | NFR2 | `app/play.tsx` |
| FR3.4 | `__tests__/domain/alphaGesture.test.ts` | NFR3 | `app.json` |
| FR4.1 | `src/domain/playSession.ts` | NFR4 | `__tests__/data/pendingQueue.test.ts` |
| FR4.2 | `src/data/settingsStore.ts` | NFR5 | `supabase/migrations/0001_records.sql` |
| FR4.3 | `src/domain/playSession.ts` | NFR6 | `src/ui/controls.tsx` |

「対応あり」は、その要件を作ったファイルがあるという意味で、合格の基準を満たしたことまでは示さない。NFR1・NFR2・NFR3・FR3.1・FR3.4 は実機とネコで確かめる。
