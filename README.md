# claude-code-first-step

本資料は、プログラミング学習を目的にClaudeを初めて利用する方を対象に、アカウント作成からClaude Code Desktopの導入、そして実際にHTML / CSS / JavaScriptを使ったTodoアプリの作成までを、一連の流れで体験できるようにまとめたものです。

## 用語について

- Claude：Anthropicが提供するAI全体のブランド名をClaudeといいます。AnthropicのClaudeアカウントを作成します。
- Claude Code：Claude Code は、AIエージェントで、Claudeデスクトップアプリ・ブラウザ・ターミナルから利用できます。
- Claudeデスクトップアプリ：Claude Codeのデスクトップアプリ版。ファイル編集・ターミナル操作・ブラウザレビュー・Git連携などをGUIで行えます。本資料ではこのアプリを中心に手順を進めます。

本資料では主に macOS 環境で動作を確認しています。

Windowsで利用する場合は、Git for Windowsのインストールを推奨します。
未インストールの場合、Claude CodeはシェルとしてPowerShellを使用します。

---

## 1. Claude アカウントを作成する

Anthropicが提供するClaudeのアカウントを作成します。

### Step 1 サインアップページにアクセスする

ブラウザで [https://claude.ai](https://claude.ai) にアクセスします。

### Step 2 Googleでサインインする

「Googleで続ける」をクリックします。

### Step 3 利用規約に同意する

利用規約とプライバシーポリシーを確認し、チェックを入れて「アカウントを作成」をクリックします。

### Step 4 Proプランを契約する（任意）

Claude Codeは、サブスクリプション と　従量課金　の二つのパターンで利用できます。

本資料では、サブスクリプション契約のProプランを前提に進めていきます。（$20/月、年払いの場合は$17/月。2026年07月21日現在の価格です。最新の料金は公式サイトでご確認ください）。

### Step 5 初期設定を進める

案内に従って「続ける」ボタンをクリックします。

### Step 6 表示名を入力する

Claudeから呼びかけられる際の表示名を入力します。

本名・ニックネームのどちらでも構いません。

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

公式サイトから、自分のOSに合ったClaudeデスクトップアプリのインストーラーをダウンロードします。

[https://claude.com/download](https://claude.com/download) 

### Step 2 Claudeデスクトップアプリをアプリケーションフォルダへ移動する

ダウンロードしたインストーラーを開き、Claudeデスクトップアプリのアイコンを「Applications」フォルダへドラッグ&ドロップします。

<img width="651" height="445" alt="Image" src="https://github.com/user-attachments/assets/bc5f8058-c01d-47ea-835f-cdb90c8cf10d" />

---

## 3. Claudeデスクトップアプリの基本操作

### Step 1 Claudeデスクトップアプリを起動する

LaunchpadからClaudeデスクトップアプリを起動します。

初回起動時にmacOSのセキュリティ確認ダイアログが表示された場合は、「開く」ボタンをクリックします。

※ Windowsで利用する場合は、Git for Windowsのインストールを推奨します。未インストールの場合、Claude CodeはシェルとしてPowerShellを使用します。

### Step 2 Claudeデスクトップアプリの初期設定を開始する

ウェルカム画面が表示されたら、「始める」をクリックします。

<img width="560" height="493" alt="Image" src="https://github.com/user-attachments/assets/82ba07fa-907e-40aa-a143-9bb4d41d89bf" />

### Step 3 Claudeデスクトップアプリにログインする



### Step 2 作業フォルダを準備する

「フォルダを選択」をクリックする
 `claude` フォルダを作成して選択する

例として「claude」フォルダを使用します。フォルダ名は任意です。

### Step 2 「ワークスペースを信頼しますか？」と表示されたら、「ワークスペースを信頼する」ボタンをクリックします。

※ Claude Code Desktop単体でファイルの閲覧・編集が可能です。VSCodeなど別のエディタを併用したい場合は、任意のタイミングで同じフォルダ（例：/Users/アカウント/claude）を開いてください。

### Step 3 VS Code でプロジェクトを開く

例
```text
：/Users/アカウント/claude
```

※ フォルダ名は任意です。

---

### Step 4 Claudeデスクトップアプリの画面構成を確認する

Claudeデスクトップアプリでは、複数のペインを自由に配置できます。
ペインとは、画面を分割して表示する区画（パネル）のことです。

各ペインはドラッグして配置やサイズを変更でき、「Views」メニューから表示・非表示を切り替えられます。

主なペイン：

Chat — チャット入力欄と会話履歴
Diff — コード変更のレビュー
Browser — ブラウザ表示やプレビュー
Terminal — ターミナル操作
File — ファイルの閲覧・編集
Plan — 作業計画の作成
Tasks — バックグラウンド処理の確認
Subagent — サブエージェントの出力

---

### Step 5 ファイル操作とコード生成

次のようなプロンプトを入力してみましょう。

- Hello Worldを表示するJavaScriptを作成してください
- hello.js をNode.jsで実行してください
- index.htmlを作成し、シンプルなランディングページを作成してください

---

### Step 6 コードを改善する

- 関数にエラーハンドリングを追加してください
- このファイル全体をTypeScriptへ書き換えてください

---

### Step 7 コードの品質を向上させる

- 可読性を高めるようにリファクタリングしてください
- ESLint / Prettier に準拠するよう整形してください
- JSDocコメントを追加してください
- モデルとビューを分離してください

---

### Step 8 コードを理解・デバッグする

- @script.js このコードを初心者向けに説明してください
- この正規表現を解説してください
- このアルゴリズムを解説してください
- このエラーを修正してください

---

### Step 9 Git連携を試す

Claude CodeではGit操作も依頼できます。

- 今の変更をコミットしてください
- 日本語でコミットメッセージを提案してください
- コミットしてください

---

### Step 10 CLAUDE.md を作成する

プロジェクトフォルダに `CLAUDE.md` を配置すると、Claude Codeは起動時に自動で読み込みます。

例えば、次のような内容を記載しておくと便利です。

- コーディング規約
- 使用する言語
- 命名規則
- Gitの運用ルール
- コミットメッセージのルール

---

## 5. ハンズオン

このハンズオンでは、HTML / CSS / JavaScriptのみを使用してTodoアプリを作成します。

最後にREADMEの作成、テスト、Gitコミットまで行い、Claude Codeを使った一連の開発フローを体験します。

### Step 1 todo_appフォルダを作成する

### Step 2 Gitリポジトリを初期化する

### Step 3 Todoアプリを作成する

HTML / CSS / JavaScriptのみを使用して、次の機能を持つTodoアプリを作成してください。

- Todoの登録
- Todoの一覧表示
- Todoの編集
- Todoの削除

### Step 4 テスト項目を作成する

作成したTodoアプリからテスト項目を作成してください。

### Step 5 テストを実施する

作成したTodoアプリをテストし、結果を表示してください。

### Step 6 README を作成する

`todo_app` フォルダに README.md を作成します。

READMEには次の内容をまとめます。
プロジェクト概要
使用技術
セットアップ方法
使い方

### Step 7 Gitコミットを行う

ここまでの変更内容を確認し、適切なコミットメッセージを提案してください。

その後、その内容でコミットしてください。

---

## 6. ターミナルでClaudeを実行してみる

## 4. Claude Code をターミナルから使えるようにします

公式ドキュメントに従って Claude Code desktop をインストールします。

[https://code.claude.com/docs/en/overview](https://code.claude.com/docs/en/overview)

### Step 1 Claude Code desktopをインストールする

ターミナルを開き、次のコマンドを実行します。

macOS:

```Bash
curl -fsSL https://claude.ai/install.sh | bash
```

次のメッセージが表示されたらインストールは完了です。

```text
✔ Claude Code successfully installed!
```

### Step 2 PATHを設定する

Claude Code コマンドをどこからでも実行できるようにPATHを設定します。

（zshの場合。bashの場合は ~/.bashrc に読み替えてください）

```Bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc && source ~/.zshrc
```

ターミナルを起動して、以下のコマンドを実行する

```bash
claude --version
2.1.215 (Claude Code)
```

インストールされていることを確認します。

起動方法

作業ディレクトリに移動して以下のコマンドを実行します。

```bash
claude
```


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

これはClaude Codeの初回起動時に出るテーマ選択画面です。翻訳するとこうなります

1. Autoを選択しました。

 Claude Code can be used with your Claude subscription or billed based on API usage through your Console account.

 Select login method:

 ❯ 1. Claude account with subscription · Pro, Max, Team, or Enterprise
   2. Anthropic Console account · API usage billing
   3. 3rd-party platform · Amazon Bedrock, Microsoft Foundry, or Vertex AI

Claude Codeは、Claudeのサブスクリプション、またはConsoleアカウント経由のAPI利用料金のいずれかで使用できます。
ログイン方法を選択してください：
1. サブスクリプション付きのClaudeアカウント（Pro、Max、Team、Enterpriseプラン）
2. Anthropic Consoleアカウント（API利用に応じた従量課金）
3. サードパーティ・プラットフォーム（Amazon Bedrock、Microsoft Foundry、Vertex AI）

おすすめの選び方：
* すでに Claude Pro / Max / Team / Enterprise のサブスクリプションに加入している（月額課金プラン）なら → 1番（追加料金なしで使えるのでこれが一番お得）
* サブスクリプションはなく、使った分だけ払うAPI課金にしたいなら → 2番（Anthropic Consoleでクレジットカード登録・API keyの発行が必要）
* 会社で AWS Bedrock / Microsoft Foundry / Google Vertex AI を経由してAnthropicモデルを契約している場合 → 3番


登録したgoogle アカウントを選択します。

Claude CodeさんがClaude chat accountのへの接続を希望しています

同意が求められるので 承認ボタンをクリックして承認します。

素晴らしいものを作りましょう
Claude Codeの準備が整いました。
このウィンドウを閉じることができます。


 Logged in as ishiwatahirotaka1012@gmail.com
 Login successful. Press Enter to continue…

Enter キーをクリックします。


 Use Claude Code's terminal setup?
 
 For the optimal coding experience, enable the recommended settings
 for your terminal: Option+Enter for newlines and no audible bell
    
 ❯ 1. Yes, use recommended settings
   2. No, maybe later with /terminal-setup
    
 Enter to confirm · Esc to skip


Claude Codeのターミナル設定を使用しますか？

1. はい、推奨設定を使用する


 Accessing workspace:
     
 /Users/hirotaka                 
            
 Quick safety check: Is this a project you created or one you trust? (Like your own code, a well-known open source project, or work
 from your team). If not, take a moment to review what's in this folder first.
                                             
 Claude Code'll be able to read, edit, and execute files here.

 Security guide
                                                      
 ❯ 1. Yes, I trust this folder          
   2. No, exit

 Enter to confirm · Esc to cancel




---


