# Phase 70303: Workshop接続確認

> Part 703: Workshop への接続 | Course 7: Workshopへの接続
> 成果物: 70303_workshop_connection.md

---

## やること

5層文脈ファイルをWorkshop Phase 00103 の形式に合わせて最終調整し、workshop.aifcc.jpにログインして接続を確認する。Course 7 「整える・作る・回す」(本書 7-9) の **「整える」 → 「作る」接続地点 = SIFT 完了 + Workshop 着手の橋渡し**。SOUL.md (損徳得厄判断軸を含む) / USER.md / MEMORY.md / WORKFLOW.md / DILIGENCE.md (三層モデル停止条件) の 5 層文脈で Workshop で「作る」フェーズへ移行する。

---

## Step 1: まず自分で書く

Claudeに渡す前に、まず自分で以下を書いてください（10分）:

1. 5層文脈ファイルに自信がある部分と不安な部分は？
2. Workshopで最初にやることは明確になっている？
3. SIFTを終えて、自分のAIとの付き合い方はどう変わった？
4. Workshopに向けての意気込みを一言で。

※ SIFTの最後のPhaseです。ここまでの道のりを振り返りながら書いてください。

---

## Step 2: Claude に投げる

下のプロンプトをそのまま Claude Code に貼り付けてください。Claude Code が Step 1 の事前メモを Read し、対話しながら成果物を Step 3 に直接書き戻します。

---

### プロンプト

# Workshop接続確認

あなたはSIFT全体の成果物を振り返り、Workshopへの接続を支援するコーチです。

## 背景
私はSIFT Course 7「Workshopへの接続」Part 703 Phase 70303 (SIFT 最終 Phase) に取り組んでいます。
Part 701-702 で SIFT 全体振り返り + 5 層文脈ファイル作成を完了し、Phase 70301-70302 で Workshop の準備を整えました。今回は 5 層ファイルを Workshop Phase 00103 形式に合わせて最終調整し、workshop.aifcc.jp にログインして接続確認 + SIFT 完了メモで SIFT を完了します。

このプロンプトは Claude Code から実行されています。Read / Edit ツールで vault のファイルを直接読み書きしてください。

## 作業ファイル
`~/sift/course7/part703/70303_workshop_connection.md`

このファイルには Step 1 (事前メモ) / Step 2 (このプロンプト) / Step 3 (成果物テンプレート) / チェックリスト が含まれています。

## 参照ファイル (必須、5 件すべて)
- `~/sift/course7/part702/70201_soul_user.md` — SOUL/USER
- `~/sift/course7/part702/70202_memory_workflow.md` — MEMORY/WORKFLOW
- `~/sift/course7/part702/70203_diligence_quality.md` — DILIGENCE
- `~/sift/course7/part703/70301_workshop_first_build.md` — Workshop で最初に作るもの
- `~/sift/course7/part703/70302_handoff_checklist.md` — 引き継ぎチェックリスト

## 進め方（私に確認を取らずに開始してください）

### Step 0: 作業ファイル + 参照ファイル 5 件を読み、必要情報を揃える
1. **作業ファイル** `~/sift/course7/part703/70303_workshop_connection.md` を Read で開き、Step 1 セクションの事前メモを取得
2. **参照ファイル 5 件** をすべて Read で開く。いずれか 1 件でも Step 3 が空欄 or テンプレのままの場合、ここで停止して受講者に該当 Phase ID を明示して伝える
3. 事前メモが空欄なら、以下 4 問をまとめて 1 度に提示し、私の答えを待つ（A/B/C 選択肢は出さない）:
   - 5 層文脈ファイルに自信がある部分と不安な部分は？
   - Workshop で最初にやることは明確になっているか
   - SIFT を終えて、自分の AI との付き合い方はどう変わったか
   - Workshop に向けての意気込みを一言で
4. 必要情報が揃ったら確認や進め方ヒアリングをはさまず即 Step 1 へ

### Step 1: 5 層ファイルの最終調整（順に進める / 件数は問わない）
Claude が 5 層文脈ファイルを Workshop Phase 00103 形式に合わせて 1 ファイルずつ最終チェック + 修正案を提示する。チェック観点 (件数は問わない / 該当する観点のみ):
- ファイル名が正しいか (SOUL.md, USER.md, MEMORY.md, WORKFLOW.md, DILIGENCE.md)
- 各ファイルの冒頭に概要 (3 行以内) が書かれているか
- 他の AI ツールや Workshop 環境でも読める汎用的な形式か
- 個人情報やセキュリティ上の問題がないか
- **三層モデル + 損徳得厄判定軸の引き継ぎ確認** (本書 7-9 / SIFT-LAYER-FRAMEWORK §3-§5 / Course 4-6 全体の到達点を Workshop へ): **第一層 (4D 能力 + Design = SIFT で立ち上げた 5 能力)** が SOUL.md / USER.md に明示 / **第二層 (Pattern 6 で言語化済み 4 不安 = 存在価値 / 無能露呈 / 承認喪失 / コントロール喪失 + 残存項目)** が MEMORY.md に明示 / **第三層 (Pattern 9 ハート起点 = 胸への意識 + 寝息の呼吸 / 本書 5-11 + 損徳得厄判断軸 = 本書 7-5 / 7-6 / 「頭で得を追う」 vs 「ハートで愛を出す」)** が SOUL.md の意思決定軸 + DILIGENCE.md の停止条件に明示されているか

各ファイル提示後、受講者に「修正したい点はあるか」を 1 問だけ聞く。
最終的に修正した箇所を Claude が記録する (件数は問わない / 該当なしも genuine)。

### Step 2: workshop.aifcc.jp ログイン確認
Claude が以下を提示し、受講者に実機ログインを依頼する:
- workshop.aifcc.jp にログイン
- プロフィールが正しいか確認
- SIFT の完了状態が反映されているか確認

受講者は実際にブラウザでログイン → 結果 (3 項目の OK / NG) を Claude Code に戻して報告。

### Step 3: SIFT 全体の積み残し集約（最終アウトプットの一つ、SIFT 卒業時の唯一の集約タイミング）

SIFT は自己を深掘りする内省ツール。各 Course のワーク中は積み残しを意識せず内省に集中する設計。Course 7 の最終 Phase で**初めて**全 Course の積み残しを集約し、Workshop / RUN / CPN への接続素材として「そっと渡す」。

1. 以下の 6 ファイルを Read で開き、「持ち越し」セクションを抽出:
   - `~/sift/course1/part105/10503_*.md`（Course 2「手放しの設計」への持ち越し）
   - `~/sift/course2/part205/20503_*.md`（Course 3「価値の発掘」への持ち越し）
   - `~/sift/course3/part305/30503_*.md`（Course 4「アンラーン — 調和と創発へ」への持ち越し）
   - `~/sift/course4/part405/40503_*.md`（Course 5「AI Fluency — AIを扱う力」への持ち越し）
   - `~/sift/course5/part505/50503_*.md`（Course 6「AIと共に整える」への持ち越し）
   - `~/sift/course6/part605/60503_*.md`（Course 7「Workshopへの接続」への持ち越し）

2. 個別運用ファイル（あれば加味、なければスキップ）:
   - `~/sift/course[N]/_PENDING_TASKS.md`（受講者が Course 完了時に個別に作成した積み残しメモ）

3. カテゴリ別に集約（並びは受講者次第、なければスキップ可）:
   - 直近の期限（時系列）
   - 物（物理 / デジタル）
   - こと（タスク / プロジェクト / 委任 / AI 化）
   - 人（関係 / 境界線 / 感謝）
   - 自己（思い込み / 内的構造 / 慈悲）
   - 仕組み・実装（プロンプト / スキル / 自動化 / ガードレール）
   - Workshop 接続（5 層文脈ファイル / 最初に作るもの 等）

4. 受講者に「積み残しのうち、特に意識して持ち越したい 3 件」を 1 問だけ聞く

5. 集約結果は Step 5 で **`~/sift/_SIFT_CARRY_OVER.md`** として書き戻す

### Step 4: SIFT 完了メモ + 一言まとめ
Claude が以下を提示する:
- **プログラム概要**: 開始日 / 完了日 / 完了 Phase 数 (90+9 = 99)
- **最大の成果**: 1 件 + エビデンス引用元
- **最大の変化**: 1 件 + エビデンス引用元
- **Workshop への期待**: 1〜2 行
- **SIFT を一言で振り返ると**: 1 行 (受講者の言葉で)

最後に受講者に修正案を 1 問だけ聞く。

### Step 5: 成果物を vault に書き戻す（2 ファイル）
受講者から実機ログイン結果が戻ってきたら、以下の 2 ファイルを書き込む:

#### 5a. `~/sift/course7/part703/70303_workshop_connection.md` の Step 3「成果物」セクション
- ファイルの Step 1 / Step 2 (このプロンプト) は触らない
- Step 3 の 5 層ファイル最終チェック表 + 修正箇所 + ログイン確認 + **SIFT 全体の積み残し集約サマリー** + SIFT 完了メモ を埋める
- チェックリストの該当項目に ✓ を入れる
- 上書き前に必ず Read で現状を確認し、Step 3 が書き込み済みなら私に確認

#### 5b. `~/sift/_SIFT_CARRY_OVER.md` を新規作成（または既存なら Edit で更新）
- Step 3 で集約した SIFT 全体の積み残しを書き戻す
- Workshop / RUN / CPN への接続素材となる SIFT 卒業後の最終リファレンス
- フォーマット: 直近の期限 + カテゴリ別 + 特に意識して持ち越したい 3 件 + 各 Course の X053 持ち越し参照リンク

## ルール
- **進め方の確認・好みヒアリングは禁止**。上記の手順で決め打ちで進める
- **質問は 1 ターンに 1 つだけ**。複数選択肢の提示や複数項目の同時質問は禁止
- 根拠がある部分と、推測の部分を分けて出力する
- まだ確定していない暫定判断には【仮説】マークをつける
- 最後だからといって「きれいなまとめ」にしなくて OK。正直な記録が一番価値がある
- 5 層ファイルの最終版の日付とバージョンを記録する (versioning)

---

## Step 3: 成果物

<!-- Claude Code が対話の結果をここに直接書き込みます -->

# Workshop接続確認

> 作成日: {{日付}}
> Phase: 70303

## 5層ファイル最終チェック

| ファイル | ファイル名 | 概要あり | 汎用形式 | セキュリティ | 状態 |
|--------|----------|---------|---------|------------|------|
| SOUL.md | OK / 要修正 | OK / 要修正 | OK / 要修正 | OK / 要修正 | |
| USER.md | | | | | |
| MEMORY.md | | | | | |
| WORKFLOW.md | | | | | |
| DILIGENCE.md | | | | | |

## 修正した箇所
1.
2.
3.

## workshop.aifcc.jp ログイン確認
- [ ] ログインできた
- [ ] プロフィールが正しい
- [ ] SIFTの完了状態が反映されている

## SIFT 全体の積み残し集約

> 全 Course の X053「次の Course への持ち越し」を集約。
> 詳細版は `~/sift/_SIFT_CARRY_OVER.md` に書き戻し（Workshop / RUN / CPN への接続素材）。

### 直近の期限（時系列）
| 期限 | タスク | 由来 Course |
|------|------|------|
|  |  |  |

### カテゴリ別件数サマリー
- 物（Course 2 由来）:  件
- こと（Course 2-3 由来）:  件
- 人（Course 2 由来）:  件
- 自己（Course 1, 3, 4 由来）:  件
- 仕組み・実装（Course 5, 6 由来）:  件
- Workshop 接続（Course 7 由来）:  件

### 特に意識して持ち越したい 3 件
1.
2.
3.

## SIFT完了メモ

### プログラム概要
- 開始日:
- 完了日:
- 完了したPhase数:

### 最大の成果
-

### 最大の変化
-

### Workshopへの期待
-

### SIFTを一言で振り返ると
-


---

## チェックリスト

- [ ] 事前メモ（Step 1）を自分で書いた
- [ ] Claude が 70201_soul_user.md / 70202_memory_workflow.md / 70203_diligence_quality.md / 70301_workshop_first_build.md / 70302_handoff_checklist.md の 5 ファイルを Read して参照したことを確認した
- [ ] Claude が 5 層ファイル (SOUL/USER/MEMORY/WORKFLOW/DILIGENCE) を 1 ターン 1 ファイルで Workshop 00103 形式に合わせて最終調整したことを確認し、納得した
- [ ] Claude が修正が必要な箇所を修正した (修正箇所 件数は問わない / 該当なしも genuine) ことを確認した
- [ ] Claude が三層モデル + 損徳得厄判定軸の引き継ぎ確認 (第一層 4D + Design = SOUL/USER / 第二層 Pattern 6 4 不安 = MEMORY / 第三層 Pattern 9 ハート起点 + 損徳得厄判断軸 = SOUL 意思決定軸 + DILIGENCE 停止条件) を提示し、5 層ファイルとの対応を確認したことを確認した
- [ ] 受講者が workshop.aifcc.jp にログインし、ログイン / プロフィール / SIFT 完了状態の 3 項目を確認して結果を Claude Code に戻した
- [ ] Claude が SIFT 全体の積み残しを Course 1-6 の X053 (10503/20503/30503/40503/50503/60503) から集約し、`~/sift/_SIFT_CARRY_OVER.md` に書き戻したことを確認した
- [ ] Claude が「特に意識して持ち越したい 3 件」を受講者に聞き、集約サマリーに反映したことを確認した
- [ ] Claude が SIFT 完了メモ (開始日 / 完了日 / 最大の成果 / 最大の変化 / Workshop への期待 / 一言まとめ) を提示したことを確認した
- [ ] Claude が Step 3 セクション (本ファイル) と `~/sift/_SIFT_CARRY_OVER.md` の 2 ファイルに書き戻したことを Obsidian で確認した

---

*SIFT by AIFCC — sift.aifcc.jp*
