# SIFT インフラ改善ランブック

> 作成日: 2026-05-02 (JST)
> 起点: Course 2 ワーク完遂 + sift-templates の X053 修正後に発見された 6 件の改善点
> 自動実行範囲: **Pass 1-2 のみ（低リスク・読み取り or 軽微変更）**。Pass 3-4 は設計提案として記録、別タイミングで望月さん承認後に実行。

---

## 背景

Course 2 のワーク完遂後、sift-templates の X053 への Course 正式名称明記（commit `975f03d`）と Course 7 最終 Phase の積み残し集約ステップ追加（commit `7ad7e8a`）の中で、6 件の改善点が見えてきた:

1. **ファイル命名規則の不揃い**: 20503 だけ `retrospective`、他は `synthesis`
2. **既存受講者の README が更新されない**問題
3. **他 Phase の fabrication リスク**全件洗い出し
4. **Workshop / RUN / CPN 側との `_SIFT_CARRY_OVER.md` 連携**未整備
5. **Course 内の Part 間橋渡し**統一
6. **Phase ごとの所要時間目安**

---

## Pass 1: 即時実行（低リスク、自動実行）

### 1A. ファイル命名統一: `20503_course2_retrospective.md` → `20503_course2_synthesis.md`

#### 動機
X053 ファイルの末尾が `synthesis` で統一されているのに 20503 だけ `retrospective`。70303 の集約 Step で受講者 / Claude が混乱するリスク。

#### 手順
1. sift-templates 側で git mv（履歴保持）
2. 自身のファイル内の参照 4 箇所を Edit
3. 外部参照 3 箇所を Edit（70101_sift_retrospective.md / 70202_memory_workflow.md × 2）
4. commit & push

#### 影響範囲
- sift-templates: 3 ファイル変更（リネーム + 70101 + 70202）
- ローカル `~/sift/`: git connected ではないので独立運用、個別判断

#### 成功基準
- `grep -r "20503_course2_retrospective" ~/Plugins/sift-templates/` で結果 0 件
- すべての参照が `20503_course2_synthesis` に統一
- main へ push 成功

#### ロールバック
git mv は履歴保持なので、git revert で戻せる

#### 実行結果（2026-05-02）✅ 完了

- ✅ `git mv course2/part205/20503_course2_retrospective.md → 20503_course2_synthesis.md`（履歴保持）
- ✅ 自身のファイル内 4 箇所を `synthesis` に Edit
- ✅ 外部参照: `course7/part701/70101_sift_retrospective.md` line 53 を Edit
- ✅ 外部参照: `course7/part702/70202_memory_workflow.md` line 51 + line 180 を Edit
- ✅ `grep -r "20503_course2_retrospective" ~/Plugins/sift-templates/` で実体参照 0 件確認（残った 2 件は本ランブックの履歴記述のみ）
- ✅ commit `1f19d1e` + push 成功

---

### 1B. 「次のPhaseへのメモ」「次のPartへのメモ」のセクションヘッダ統一性

#### 調査結果（grep 全件洗い出し）
- 「次のPhaseへのメモ」: Course 3-6 の各 Phase で多数（約 50+ 件）
- 「次のPartへのメモ」: Course 3-6 の各 Phase で複数（約 10 件）
- 「Course X「正式名」への持ち越し」: X053 のみ（commit `975f03d` で修正済）

#### 判定
- セクションヘッダ自体は受講者が記入する枠のため、**fabrication リスクは低い**
- ただしヘッダ命名の一貫性は欠けている（Phase 内 / Part 内 / Course 間で表現が違う）
- ヘッダ統一は破壊的変更（24+ ファイル）になるため、Pass 3 へ送る

---

## Pass 2: Workshop / RUN / CPN 連携調査（読み取り専用）

### 2A. Workshop 側の `_SIFT_CARRY_OVER.md` 連携状況

#### 調査結果
- aifcc-workshop の Phase 00103 で SIFT 修了者が vault を持ち込む明示あり（CURRICULUM.md line 153）
- 5 層ファイル（SOUL/USER/MEMORY/WORKFLOW/DILIGENCE）の参照は CURRICULUM.md にあり
- **`_SIFT_CARRY_OVER.md` の参照は aifcc-workshop / aifcc-run / aifcc-cpn いずれにも未存在**

#### 含意
- Workshop は 5 層ファイルベースで設計されている
- `_SIFT_CARRY_OVER.md` は SIFT 卒業時に新たに生まれる素材として、Workshop / RUN / CPN 側に組み込みが必要

### 2B. aifcc-run の SIFT 持ち越し参照
- RUNBOOK.md に「SIFT 側に持ち越し」「SIFT 側 2 件の持ち越し」の言及あり（line 372 / 604）
- ファイルベースの参照ではなく、概念的な持ち越し管理

### 2C. 連携拡張提案（実行は別タイミング、設計のみ）

`~/sift/_SIFT_CARRY_OVER.md` を 3 つの下流（Workshop / RUN / CPN）で受け取る仕組み:

| 下流 | 提案箇所 | 拡張内容 |
|------|--------|--------|
| **aifcc-workshop** | Phase 00103 or 00104 | 5 層ファイルと併せて `_SIFT_CARRY_OVER.md` も Read。「SIFT 卒業時の持ち越し事項を Workshop の最初の課題リスト初期値として使う」 |
| **aifcc-run** | 入口 Phase（Phase B# 系列の起点） | `_SIFT_CARRY_OVER.md` を Read して B/E 系の B# 課題テンプレートに統合 |
| **aifcc-cpn** | 入口 Phase | Read して認定対象の振り返り素材として活用 |

#### 実行条件
望月さん承認後、各 repo で個別 PR / 直接修正

---

## Pass 3: 大規模変更の設計提案（実行は別タイミング）

### 3A. Part 間橋渡し統一

#### 対象
各 Part の最終 Phase（X103, X203, X303, X403）に「次の Part への橋渡し」を統一フォーマットで追加。
- 24 ファイル（4 Part × 6 Course）。
- X503（Course 最終 Part の最終 Phase）= X053 は既に Course 間の橋渡しで完了。

#### 統一フォーマット案
```markdown
## 次の Part「[Part 名]」への持ち越し
> [Part 概要 1-2 行]
- 持ち越したい気づき:
- 次の Part で扱うこと:
```

#### 工数見積もり
24 ファイル × 5 分 / 件 = 約 2 時間

#### 実行条件
- 望月さん承認後
- 既存ヘッダ（「次のPhaseへのメモ」等）の命名整理と同時実施推奨

---

### 3B. Phase 所要時間目安

#### 対象
99 Phase 全部のヘッダに「目安時間: X 分」を追加

#### 案
```markdown
> 目安時間: 60 分（事前メモ 10 分 + 対話 50 分）
```

#### 工数見積もり
99 Phase × 1 分 / 件 = 約 100 分（一律 60 分仮置きする場合）

#### 実行条件
- 望月さん承認後
- 一律 60 分にするか、Phase ごとに調整するか判断必要

---

## Pass 4: 運用ドキュメント（後回し可）

### 4A. 既存受講者への README 更新案内

#### 課題
sift-templates の README を更新しても、既に `~/sift/` を運用している受講者は古い README のまま。

#### 提案
1. SIFT.aifcc.jp の UI で「テンプレ更新があった時の取り込み方」を案内
2. aifcc-sift の README に「`git -C ~/sift pull origin main` で最新テンプレを取り込めます」と明記
3. 重要な更新時はメーラー / Discord で通知

#### 実行条件
望月さん判断、aifcc-sift / SIFT.aifcc.jp の UI 設計と統合

---

## 完了状況サマリー

| Pass | 内容 | 状態 |
|------|------|------|
| 1A | 20503 リネーム | ✅ 完了（2026-05-02） |
| 1B | ヘッダ命名調査 | 完了（Pass 3 へ移送） |
| 2A | Workshop 連携調査 | 完了（連携未整備が判明） |
| 2B | RUN 連携調査 | 完了（概念存在、ファイル未統合） |
| 2C | 連携拡張提案 | 完了（設計のみ、実行は別タイミング） |
| 3A | Part 間橋渡し統一 | 設計提案のみ |
| 3B | Phase 所要時間目安 | 設計提案のみ |
| 4A | README 更新案内 | 設計提案のみ |

---

## メンテナンス方針

- このランブックは sift-templates のメタ情報。Course 2 ワーク完遂後の改善サイクルの一環
- 今後の SIFT 改善で発生したアイデアもここに追記
- 完了したら ✅ + 完了日を追記、削除はしない（参照履歴）

---

*SIFT インフラ改善ランブック / SIFT by AIFCC*
