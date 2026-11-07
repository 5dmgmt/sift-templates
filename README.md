# SIFT Templates

AI 導入前の仕分けプログラム「SIFT」のワークシート集です。7 コース・33 Part・99 Phase の、書き込み前のワークシートが入っています。このフォルダを Mac の `~/sift` に置き、Obsidian の保管庫（vault）として開いて使います。

> 依頼文（Step 2）の正本は SIFT のアプリ（https://sift.aifcc.jp）の Phase 画面です。ここの写しとアプリが違うときは、アプリの方を使います。

## 使い方（Claude Code と進めます）

1. SIFT のサイトの「事前準備」を終えます（Claude のアカウント・Obsidian・Claude Code・Claude in Chrome・1Password など）。
2. ターミナルで cd ~/sift && claude と入力して起動します。Phase ごとに /clear で会話を新しくします。
3. SIFT のサイトで Phase を選び、「Obsidianで開く」でワークシートを開きます。
4. **Step 1**: まず自分の言葉で書きます（Claude に投げる前に）。前の Phase の成果物を見返したいときは、Phase 画面に出る「前の Phase の成果物の場所」から開きます。
5. **Step 2**: Phase 画面のプロンプトを Claude Code に貼り付けます。Claude Code が Step 1 を読み、対話しながら成果物を Step 3 に書き込みます。
6. **Step 3**: 書かれた成果物の中身を確かめます。最後に、サイトの Phase 画面の完了チェックを押します。

ワークシートの Step 2 とチェックリストは、アプリの Phase 画面の写しです。違いがあるときは、アプリの方を使います。

## 書いたものの置き場所について

ここにあるのは、まだ何も書かれていない状態のワークシートです。あなたが書いたファイルは Mac の `~/sift` にあり、SIFT のサイトにも GitHub にも送られません（サイトに保存されるのは進捗のチェックだけです）。ただし Claude との会話は、処理のために Anthropic に送られ、会話の記録は Mac の `~/.claude/projects` にも残ります。そのため、事前準備で「モデルの改善に協力（Help improve our AI models）」をオフにし、実名と顧客の名前は仮名で書きます。

バックアップを取りたくなったときは、iCloud Drive や Obsidian Sync など、ご自身だけが見える場所をお選びください。Claude に「GitHub に保存して」と頼むこともできますが、その保存先が公開か非公開かを、先に確かめます。

## フォルダ構成

```
sift/
├── README.md         # このファイル
├── course1/          # 人生の棚卸し（Part 101-105）
├── course2/          # 手放しの設計（Part 201-205）
├── course3/          # 目的の言語化（Part 301-305）
├── course4/          # アンラーン（Part 401-405）
├── course5/          # AI Fluency — AIを扱う力（Part 501-505）
├── course6/          # AIと共に整える（Part 601-605）
├── course7/          # Workshopへの接続（Part 701-703）
└── context/          # 5層文脈ファイル（Course 7 で Claude Code が書き出します）
```

Course 1〜6 は各 5 Part × 3 Phase = 15 ファイル、Course 7 は 3 Part × 3 Phase = 9 ファイルで、合わせて 99 ファイルです。

### Course 6 の Phase 60202 で作られるもの

Phase 60202 では、成果物を移しません。`00_INDEX.md` と 5 つのフォルダ（`01_自己理解`・`02_事業`・`03_業務手順`・`04_AI運用`・`05_振り返り`）を作り、それぞれの README から、元の場所（`courseN/partNNN/`）の成果物へリンクを張ります。成果物は元の場所にあるままです。Course 6 以降に新しく作るもの（業務の手順など）は、この 5 つのフォルダに置きます。

`_private/` は、実名と仮名の対応表だけを置く場所です。事前準備の deny の設定で、Claude Code は `_private/` を読み書きできません。伏せ字が必要なファイルは、あなたがその場で直します。

## context/ の 5 つのファイル

`context/` には、5 つのファイル（SOUL.md・USER.md・MEMORY.md・WORKFLOW.md・DILIGENCE.md）の雛形が入っています。取得した直後は中身が空です。Course 7 で、Claude Code が `~/sift/context/` に書き出します。

| Phase | 書き出されるファイル |
|-------|----------------------|
| 70201 | SOUL.md・USER.md |
| 70202 | MEMORY.md・WORKFLOW.md |
| 70203 | DILIGENCE.md |
| 70303 | 5 本の最終調整 |

Workshop に進むときは、この 5 本を `~/context/` にコピーして使います（Workshop の Phase 00103）。

## ワークシートを新しい版にする

すでに `~/sift` がある人は、SIFT のサイトの「事前準備」の Step 3 にある「既に ~/sift がある人は」の依頼文を、Claude Code に貼り付けます。あなたが書いた中身には触れず、Step 2 とチェックリストの節だけが新しくなります。

## リンク

- SIFT: https://sift.aifcc.jp
- Workshop: https://workshop.aifcc.jp
- RUN: https://run.aifcc.jp
- AIFCC: https://aifcc.jp
