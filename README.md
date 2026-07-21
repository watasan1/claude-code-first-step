# claude-code-first-step

本資料は、Claudeを初めて使う方を対象に、アカウント作成からClaude Codeの導入、そして実際にHTML/CSS/JavaScriptでTodoリストアプリを完成させるまでを、一連の流れで体験できるようにまとめたものです。
この手順に沿って進めることで、Claudeのセットアップからコード生成・修正・デバッグ・テスト・Gitによるバージョン管理まで、Claude Codeを活用した基本的な開発フローを一通り体験できます。

Claude Desktop：Claudeとチャットするためのデスクトップアプリ
Claude Code：ターミナルから利用するAIコーディングツール

本資料では、主にmacOSにおいて確認しております。
windowsでは、Gitを必要としているので先にGitのインストールをしてからClaude を導入してください。

---

## 1. Claude Desktopの導入

### Step 1 ダウンローダーをインストールする

公式サイトから、自分のOSにあったインストーラーをダウンロードします。

[https://claude.com/download](https://claude.com/download) 

### Step 2 Claude をアプリケーションフォルダにドラッグ&ドロップ

ダウンロードしたインストーラーを開き。Claudeのアイコンを「Applications」フォルダへドラッグ&ドロップします。

<img width="651" height="445" alt="Image" src="https://github.com/user-attachments/assets/bc5f8058-c01d-47ea-835f-cdb90c8cf10d" />

### Step 3 Claude Desktop を起動する

LaunchpadからClaude Desktopを起動します。

初回起動時にmacOSのセキュリティ確認ダイアログが表示されたら、「開く」ボタンをクリックします。

### Step 4 初期設定を開始する

ウェルカム画面が表示されたら、「始める」をクリックします。

<img width="560" height="493" alt="Image" src="https://github.com/user-attachments/assets/82ba07fa-907e-40aa-a143-9bb4d41d89bf" />

---

## 2. Claude のアカウントを作成する

### Step 1 Googleでサインインする

「Googleで続ける」をクリックします。

### Step 2 アカウントを作成する

表示されて項目を確認・入力し、「続ける」ボタンをクリックします。

### Step 3 利用規約に同意する

利用規約とプライバシーポリシーを確認し、チェックを入れて「アカウントを作成」をクリックします。

### Step 4 Pro プロプランを契約する (19$/月)

プランを選択します。「Pro プロプランを取得」をクリックします。

### Step 5 初期設定を進める

案内画面が表示されたら、「続ける」ボタンをクリックします。

### Step 6 表示名を入力する

Claudeから呼びかけられる際の表示名を入力します。

本名・ニックネームのどちらでも構いません。

### Step 7 アンケートに回答する

該当する職種を選択し、「次へ」をクリックします。

例

エンジニア／ソフトウェア開発
プロダクトマネージャー
デザイナー
学生／その他

---

## 3. Claude Codeの導入する

公式ドキュメントに従ってインストールします。

[https://code.claude.com/docs/en/overview](https://code.claude.com/docs/en/overview)

ターミナルを開き、以下のコマンドを実行します。

macOS:

```Bash
curl -fsSL https://claude.ai/install.sh | bash
```

次のメッセージが表示されたらインストール完了です。

```text
✔ Claude Code successfully installed!
```

というテキストを確認して完了です。

### Step 2 PATHを通す


（zshの場合。bashの場合は ~/.bashrc に読み替え）:

```Bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc && source ~/.zshrc
```

---

## 4. Claude Code を使ってみる

### Step 1 作業フォルダを準備する

1. Claude Code Desktop を実行すると
2. 「フォルダを選択」をクリックする
3. `claude` フォルダを作成して選択する

例として claude フォルダを使用します。フォルダ名は任意です。

4. 「ワークスペースを信頼しますか？」と表示されたら「ワークスペースを信頼する」ボタンをクリックする

5. VSCode でプロジェクトを開く

```text
：/Users/アカウント/claude
```

---

### Step 2 Claude Code Desktopの画面構成を確認する

Claude Desktopでは、複数のペインを自由に配置できます。

主なペイン：

Chat — チャット入力欄と会話エリアはこれ1つにまとまっています（別々の区画ではありません）
Diff — コード変更のレビュー
Browser — アプリのプレビューや外部サイト表示
Terminal — ターミナル操作
File — ファイルの閲覧・編集
Plan — 計画立案用ワークスペース
Tasks — バックグラウンド作業の監視
Subagent — サブエージェントの出力

ペインとは、

画面を分割して表示する区画（パネル）のことです。

Chatペインには

- チャット入力欄
- 会話履歴

がまとめて表示されます。

各ペインはドラッグして配置変更・サイズ変更ができ、「Views」メニューから表示・非表示を切り替えられます。

---

### Step 3 ファイル操作とコード生成

次のようなプロンプトを入力してみましょう。

- Hello Worldを表示するJavaScriptを作成してください
- hello.js をNode.jsで実行してください
- index.htmlを作成して。シンプルなランディングページを作成してください

---

### Step 4 コードを改善する

- 関数にエラーハンドリングを追加してください
- このファイル全体をTypeScriptに書き換えてください

---

### Step 5 コードの品質を向上させる

- 可読性を高めるようにリファクタリングしてください
- ESLint / Prettier に準拠するよう整形してください
- JSDocコメントを追加してください
- モデルとビューを分離してください

---

### Step 6 コードを理解・デバッグする

- @script.js このコードを初心者向けに説明してください
- この正規表現を解説してください
- このアルゴリズムを解説してください
- このエラーを修正してください

---

### Step 7 Git連携を試す

Claude CodeではGit操作も依頼できます。

- 今の変更をコミットしてください
- 日本語でコミットメッセージを提案してください
- コミットしてください


### CLAUDE.md を作成する

プロジェクトフォルダに `CLAUDE.md` を配置すると、Claude Codeは起動時に自動で読み込みます。

例えば次のような内容を書いておくと便利です。

- コーディング規約
- 使用する言語
- 命名規則
- Gitの運用ルール
- コミットメッセージのルール

---

## 5. ハンズオン

このハンズオンでは、HTML / CSS / JavaScriptを使用してTodoアプリを作成します。

最後にREADMEの作成、テスト、Gitコミットまで行い、Claude Codeを使った一連の開発フローを体験します。

### Step 1 todo_app フォルダを作成する

### Step 2 Gitリポジトリを初期化する

### Step 3 Todoアプリを作成する

以下の機能を実装します。

- Todoの登録
- Todoの一覧表示
- Todoの編集
- Todoの削除

### Step 4 テスト項目を洗い出す

作成したTodo Appからテスト項目を作成してください

### Step 5 テストを実施する

作成したTodoアプリをテストし、結果を表示します。

### Step 6 README を作成する

`todo_app` フォルダに README.md を作成します。

### Step 7 Gitコミットを行う

ここまでの変更内容を確認し、適切なコミットメッセージを提案・コミットします。
