# SIFT Templates

AI導入前の仕分けプログラム「SIFT」の成果物テンプレート集。
75 Phase 分のワークシートが入っています。

## セットアップ

### PC（Mac / Windows）

```bash
git clone https://github.com/5dmgmt/sift-templates.git ~/sift
```

Obsidian を開く → 「フォルダをVaultとして開く」→ `~/sift` を選択

### スマホ（iPhone / Android）

1. Obsidian モバイルアプリをインストール
2. iCloud Drive または Obsidian Sync で PC と同期
3. 同じ vault (`sift`) が開く

## 使い方

1. **SIFT の UI** (sift.aifcc.jp/sift) で Phase を選ぶ
2. 「Obsidianで開く」をタップ → 該当ファイルが自動で開く
3. **Step 1**: まず自分で書く（10分）
4. **Step 2**: プロンプトを Claude に貼り付ける
5. **Step 3**: Claude の出力を成果物セクションに貼り付け、自分で編集
6. チェックリストを確認して保存

## フォルダ構成

```
sift/
├── course1/          # 人生の棚卸し（Part 101-105）
├── course2/          # 手放しの設計（Part 201-205）
├── course3/          # 目的の言語化（Part 301-305）
├── course4/          # アンラーン — 調和と創発へ（Part 401-405）
├── course5/          # AI Fluency — AIを扱う力（Part 501-505）
├── course6/          # AIと共に整える（Part 601-605）
├── course7/          # Workshopへの接続（Part 701-703）
└── context/          # 5層文脈ファイル（SIFT完了時に埋める）
```

C1-C6: 各5 Part × 3 Phase、C7: 3 Part × 3 Phase = 合計 99 ファイル

## 積み残しの扱い（設計思想）

SIFT は自己を深掘りする内省ツール。各 Course のワーク中は**積み残しタスク管理を意識せず、内省に集中**してください。

- 各 Course の最終 Phase（10503 / 20503 / 30503 / 40503 / 50503 / 60503）で「次の Course への持ち越し」が自然に積まれていきます
- SIFT 全 Course を完遂した最後に、**Course 7 の最終 Phase 70303** で全 Course の持ち越しを `~/sift/_SIFT_CARRY_OVER.md` として集約し、Workshop / RUN / CPN への接続素材として「そっと渡す」設計です
- 各 Phase のワーク中に未完了タスクのリンクや一覧を見ると、内省モード（ハート優位）から TODO 管理モード（頭優位）に引き戻されてしまうため、各 Phase テンプレートは意図的にそうした参照を含めません

期限のある実行項目（締め切り / 連絡 / 決済 等）が発生した場合は、SIFT vault の外（カレンダー / タスク管理ツール）で別管理してください。

## リンク

- SIFT: https://sift.aifcc.jp
- Workshop: https://workshop.aifcc.jp
- AIFCC: https://aifcc.jp
