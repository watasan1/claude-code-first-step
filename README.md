# claude-code-first-step

本資料は、プログラミング学習を目的にClaudeを初めて利用する方を対象に、アカウント作成からClaude デスクトップアプリの導入、そして実際にHTML / CSS / JavaScriptを使ったTodoアプリの作成までを、一連の流れで体験できるようにまとめたものです。

## 用語について

- Claude：Anthropicが提供するAI全体のブランド名をClaudeと言います。
- Claude Code：AIエージェントで、Claudeデスクトップアプリ・ブラウザ・ターミナルから利用できます(本資料ではデスクトップアプリとターミナルでの利用方法を学びます)。
- Claudeデスクトップアプリ：Claude Codeのデスクトップアプリ版。ファイル編集・ターミナル操作・ブラウザレビュー・Git連携などをGUIで行えます。本資料ではこのアプリを中心に手順を進めます。

本資料では主に macOS 環境で動作を確認しています。

（参考）Windows環境については未検証のため、本資料では扱いません。動作確認が取れ次第、別途手順を追記する予定です。
先んじて試される場合は、Git for Windowsをインストールしておくことをおすすめします（未インストールの場合、Claude CodeはシェルとしてPowerShellを使用します）。

---

## 1. Claudeアカウントを作成する

Anthropicが提供するClaudeのアカウントを作成します。

### Step 1 サインアップページにアクセスする

ブラウザで [https://claude.ai](https://claude.ai) にアクセスします。

---

### Step 2 Googleでサインインする

「Googleで続ける」をクリックします。

---

### Step 3 利用規約に同意する

利用規約とプライバシーポリシーを確認し、チェックを入れて「アカウントを作成」をクリックします。

---

### Step 4 Proプランを契約する

Claude Codeは、サブスクリプションと従量課金の二つのパターンで利用できますが、本資料ではサブスクリプション契約のProプランを導入したうえで進めます。

---

### Step 5 初期設定を進める

案内に従って「続ける」ボタンをクリックします。

---

### Step 6 表示名を入力する

Claudeから呼びかけられる際の表示名を入力します。

本名・ニックネームのどちらでも構いません。

---

### Step 7 アンケートに回答する

該当する職種を選択し、「次へ」をクリックします。

例

- エンジニア／ソフトウェア開発
- プロダクトマネージャー
- デザイナー
- 学生／その他

---

## 2. Claudeデスクトップアプリをインストールする

### Step 1 Claudeデスクトップアプリのインストーラーをダウンロードする

公式サイト（[https://claude.com/download](https://claude.com/download)）から、自分のOSに合ったClaudeデスクトップアプリのインストーラーをダウンロードします。

---

### Step 2 Claudeデスクトップアプリをアプリケーションフォルダへ移動する

ダウンロードしたインストーラーを開き、Claudeデスクトップアプリのアイコンを「Applications」フォルダへドラッグ&ドロップします。

<img width="651" height="445" alt="Image" src="https://github.com/user-attachments/assets/bc5f8058-c01d-47ea-835f-cdb90c8cf10d" />

---

## 3. Claudeデスクトップアプリの基本操作

### Step 1 Claudeデスクトップアプリを起動する

LaunchpadからClaudeデスクトップアプリを起動します。

初回起動時にmacOSのセキュリティ確認ダイアログが表示された場合は、「開く」ボタンをクリックします。

---

### Step 2 Claudeデスクトップアプリのログイン

ウェルカム画面が表示されたら、「始める」をクリックします。

<img width="560" height="493" alt="Image" src="https://github.com/user-attachments/assets/82ba07fa-907e-40aa-a143-9bb4d41d89bf" />

---

### Step 3 Claudeデスクトップアプリにサインイン

サインイン画面が表示されたら、1章で作成したClaudeアカウントでサインインします。

ここではGoogleアカウントでログインする例を示します。「Googleで続ける」ボタンをクリックします。

<img width="600" height="599" alt="Image" src="https://github.com/user-attachments/assets/52c0edb5-ddb7-4034-a451-64e1ce535a9f" />

Googleアカウントで登録した場合、「Claude」から「claude.com」を使用してサインインしようとしています、という画面が表示されます。

「アプリとWebサイトにあなたに関する情報を共有することを許可します。」と表示されたら、「続ける」ボタンをクリックします。

<img width="305" height="347" alt="Image" src="https://github.com/user-attachments/assets/7df77502-a39d-4e34-aea8-cfb9eb582c3e" />

「Claude」に移動画面が表示されたら、Googleアカウントをクリックしてログインします。

続いてClaudeに再ログインしようとしている画面が表示されるので、規約を確認して「次へ」をクリックしてください。（初回ログインでは表示されない可能性があります）

---

### Step 4 作業フォルダを準備する

「フォルダを選択」をクリックします。

`claude` フォルダを作成して選択します。

例として「claude」フォルダを使用します。フォルダ名は任意です。

---

### Step 5 ワークスペースを信頼する

「ワークスペースを信頼しますか？」と表示されたら、「ワークスペースを信頼する」ボタンをクリックします。

※ Claudeデスクトップアプリ単体でファイルの閲覧・編集が可能です。VSCodeなど別のエディタを併用したい場合は、任意のタイミングで同じフォルダ（例：/Users/アカウント/claude）を開いてください。

---

### Step 6 Claudeデスクトップアプリの画面構成を確認する

Claudeデスクトップアプリでは、複数のペインを自由に配置できます。
ペインとは、画面を分割して表示する区画（パネル）のことです。

各ペインはドラッグして配置やサイズを変更でき、「Views」メニューから表示・非表示を切り替えられます。

主なペイン：

- Chat — チャット入力欄と会話履歴
- Diff — コード変更のレビュー
- Browser — ブラウザ表示やプレビュー
- Terminal — ターミナル操作
- File — ファイルの閲覧・編集
- Plan — 作業計画の作成
- Tasks — バックグラウンド処理の確認
- Subagent — サブエージェントの出力

---

### Step 7 ファイル操作とコード生成を試す

次のようなプロンプトを入力してみましょう。

- Hello Worldを表示するJavaScriptを作成してください
- hello.js をNode.jsで実行してください
- index.htmlを作成し、シンプルなランディングページを作成してください

---

### Step 8 コードを改善する

- 関数にエラーハンドリングを追加してください
- このファイル全体をTypeScriptへ書き換えてください

---

### Step 9 コードの品質を向上させる

- 可読性を高めるようにリファクタリングしてください
- ESLint / Prettier に準拠するよう整形してください
- JSDocコメントを追加してください
- モデルとビューを分離してください

---

### Step 10 コードを理解・デバッグする

- @script.js このコードを初心者向けに説明してください
- この正規表現を解説してください
- このアルゴリズムを解説してください
- このエラーを修正してください

---

### Step 11 Git連携を試す

Claude CodeではGit操作も依頼できます。まずコミットメッセージを提案してもらい、内容を確認してから実際にコミットする、という2段階の流れがおすすめです。

1. 日本語でコミットメッセージを提案してください
2. （提案内容を確認後）そのままコミットしてください

---

### Step 12 CLAUDE.md を作成する

プロジェクトフォルダに `CLAUDE.md` を配置すると、Claude Codeは起動時に自動で読み込みます。

例えば、次のような内容を記載しておくと便利です。

- コーディング規約
- 使用する言語
- 命名規則
- Gitの運用ルール
- コミットメッセージのルール

---

## 4. ハンズオン

このハンズオンでは、HTML / CSS / JavaScriptのみを使用してTodoアプリを作成します。

最後にREADMEの作成、テスト、Gitコミットまで行い、Claude Codeを使った一連の開発フローを体験します。

### Step 1 todo_appフォルダを作成する

todo_appという名前のフォルダを作成してくださいとClaudeに指示します。

---

### Step 2 Gitリポジトリを初期化する

作成した、todo_appフォルダ内でGitリポジトリを初期化するようClaudeに指示します。

---

### Step 3 Todoアプリを作成する

HTML / CSS / JavaScriptのみを使用して、次の機能を持つTodoアプリを作成してください。

- Todoの登録
- Todoの一覧表示
- Todoの編集
- Todoの削除

---

### Step 4 テスト項目を作成する

作成したTodoアプリからテスト項目（チェックリスト）を作成してください。

---

### Step 5 テストを実施する

作成した、テスト項目に沿って、Claudeにブラウザでの動作確認(手動テスト)を依頼し、テスト結果を表示してください。

---

### Step 6 README を作成する

todo_appフォルダに、README.mdを作成してくださいとClaudeに指示します。

README.mdには次の内容をまとめてくださいとClaudeに指示します。
 
- プロジェクト概要
- 使用技術
- セットアップ方法
- 使い方

---

### Step 7 Gitコミットを行う

ここまでの変更内容を確認し、適切なコミットメッセージを日本語で提案してください。

提案内容を確認する

その後、その内容でコミットしてください。

---

## 5. ターミナルからClaude Codeを実行できるようにする

### Step 1 Claude Code CLIをインストールする

公式ドキュメント（[https://code.claude.com/docs/en/overview](https://code.claude.com/docs/en/overview)）
に記載の手順に従い、以下のコマンドでインストールします。

ターミナルを開き、次のコマンドを実行します。

macOS:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

次のメッセージが表示されたらインストールは完了です。

```text
✔ Claude Code successfully installed!
```

---

### Step 2 PATHを設定する

Claude Code コマンドをどこからでも実行できるようにPATHを設定します。

（zshの場合。bashの場合は `~/.bashrc` に読み替えてください）

```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc && source ~/.zshrc
```

ターミナルを起動して、以下のコマンドを実行し、インストールされていることを確認します。

```bash
claude --version
```

2.1.215 (Claude Code)

バージョン番号は執筆時点の例です。実際に表示される値はインストール状況により異なります

---

### Step 3 Claude Code を起動する

作業ディレクトリに移動します。

```bash
cd ~/claude
```

Claude Code を起動するコマンドを実行します。

```bash
claude
```

初回起動時は、テーマ選択・ログイン・ターミナル設定・ワークスペースの信頼確認が順番に表示されます。

---

### Step 4 テーマを選択する

以下のようなテーマ選択画面が表示されます。


```text
Let's get started.

Choose the text style that looks best with your terminal
To change this later, run /theme

❯ 1. Auto (match terminal)✔
2. Dark mode 
3. Light mode
4. Dark mode (colorblind-friendly)
5. Light mode (colorblind-friendly)
6. Dark mode (ANSI colors only)
7. Light mode (ANSI colors only)
```

ここでは「❯ 1. Auto (match terminal)」を選択します。

---

### Step 5 ログイン方法を選択する

続いて、ログイン方法を選択する画面が表示されます。

```text
Claude Code can be used with your Claude subscription or billed based on API usage through your Console account.

Select login method:

 ❯ 1. Claude account with subscription · Pro, Max, Team, or Enterprise
   2. Anthropic Console account · API usage billing
   3. 3rd-party platform · Amazon Bedrock, Microsoft Foundry, or Vertex AI
```

日本語訳：Claude Codeは、Claudeのサブスクリプション、またはConsoleアカウント経由のAPI利用料金のいずれかで使用できます。ログイン方法を選択してください。

1. サブスクリプション付きのClaudeアカウント（Pro、Max、Team、Enterpriseプラン）
2. Anthropic Consoleアカウント（API利用に応じた従量課金）
3. サードパーティ・プラットフォーム（Amazon Bedrock、Microsoft Foundry、Vertex AI）

本資料の1章でProプランを契約しているので、「1. Claude account with subscription」を選択します。

「1」を選択すると、ブラウザが開き登録したGoogleアカウントを選択する画面になります。

「Claude CodeがClaude chat accountへ接続を希望しています」という同意画面が表示されるので、承認ボタンをクリックして承認します。

```text
素晴らしいものを作りましょう
Claude Codeの準備が整いました。
このウィンドウを閉じることができます。
```

ターミナルに戻ると、以下のように表示されます。

```text
 Logged in as アカウント@gmail.com
 Login successful. Press Enter to continue…
```

Enter キーを押します。

---

### Step 6 ターミナルの推奨設定を有効にする

```text
Use Claude Code's terminal setup?
 
For the optimal coding experience, enable the recommended settings
for your terminal: Option+Enter for newlines and no audible bell
    
❯ 1. Yes, use recommended settings
  2. No, maybe later with /terminal-setup
    
Enter to confirm · Esc to skip
```

日本語訳：Claude Codeのターミナル設定を使用しますか？

「1. はい、推奨設定を使用する」を選択します。

---

### Step 7 ワークスペースを信頼する

```text
 Accessing workspace:
     
 /Users/アカウント名               
            
 Quick safety check: Is this a project you created or one you trust? (Like your own code, a well-known open source project, or work
 from your team). If not, take a moment to review what's in this folder first.
                                             
 Claude Code'll be able to read, edit, and execute files here.

 Security guide
                                                      
 ❯ 1. Yes, I trust this folder          
   2. No, exit

 Enter to confirm · Esc to cancel
```

自分が作成した、または信頼できるフォルダであることを確認し、「1. Yes, I trust this folder」を選択します。

---


