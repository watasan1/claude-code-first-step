# claude-code-first-step

本資料は、プログラミング学習を目的にClaudeを初めて利用する方を対象に、アカウント作成からClaudeデスクトップアプリの導入、そして実際にHTML/CSS/JavaScriptを使ったTodoアプリの作成までを、一連の流れで体験できるようにまとめたものです。

## 用語について

- Claude：Anthropicが提供するAIサービスのブランド名です。
- Claude Code：Anthropicが提供するAIコーディングエージェントです。Claudeデスクトップアプリやターミナル（CLI）から利用できます。
- Claudeデスクトップアプリ：Claudeをデスクトップで利用するための公式アプリです。チャット機能に加えて、Claude Codeを利用し、ファイル編集・ターミナル操作・ブラウザプレビュー・Git連携なども行えます。本資料ではこのアプリを中心に手順を進めます。

本資料では主に macOS 環境で動作を確認しています。

（参考）本資料ではWindows環境については扱いません。

将来的に試す場合は、Windows PowerShellから、Git for Windowsをインストールしておくと導入しやすくなります。

---

## 1. Claudeアカウントを作成する

Anthropicが提供するClaudeのアカウントを作成します。

### 1-1. サインアップページにアクセスする

ブラウザで [Claude公式サイト](https://claude.ai) にアクセスします。

---

### 1-2. Googleでサインインする

「Googleで続ける」をクリックします。

---

### 1-3. 利用規約に同意する

利用規約とプライバシーポリシーを確認し、チェックを入れて「アカウントを作成」をクリックします。

---

### 1-4. Proプランを契約する

Claude Codeは、サブスクリプション契約または従量課金で利用できますが、本資料ではサブスクリプション契約のProプランを導入したうえで進めます。

---

### 1-5. 初期設定を進める

案内に従って「続ける」ボタンをクリックします。

---

### 1-6. 表示名を入力する

Claudeから呼びかけられる際の表示名を入力します。

本名・ニックネームのどちらでも構いません。

---

### 1-7. アンケートに回答する

該当する職種を選択し、「次へ」をクリックします。

例：

- エンジニア／ソフトウェア開発
- プロダクトマネージャー
- デザイナー
- 学生／その他

---

## 2. Claudeデスクトップアプリをインストールする

### 2-1. Claudeデスクトップアプリのインストーラーをダウンロードする


ブラウザで（[Claude 公式サイト](https://claude.com/download)）にアクセスします。
自分のOSに合ったClaudeデスクトップアプリのインストーラーをダウンロードします。

---

### 2-2. Claudeデスクトップアプリをアプリケーションフォルダへ移動する

ダウンロードしたインストーラーを開き、Claudeデスクトップアプリのアイコンを「Applications」フォルダへドラッグ&ドロップします。

<img width="651" height="445" alt="Image" src="https://github.com/user-attachments/assets/bc5f8058-c01d-47ea-835f-cdb90c8cf10d" />

---

## 3. Claudeデスクトップアプリを使う

### 3-1. Claudeデスクトップアプリを起動する

LaunchpadからClaudeデスクトップアプリを起動します。

初回起動時にmacOSのセキュリティ確認ダイアログが表示された場合は、「開く」ボタンをクリックします。

---

### 3-2. Claudeにログインする

Claudeデスクトップアプリを起動すると、ウェルカム画面が表示されます。

<img width="560" height="493" alt="Image" src="https://github.com/user-attachments/assets/82ba07fa-907e-40aa-a143-9bb4d41d89bf" />

サインイン画面が表示されたら、1章で作成したClaudeアカウントでログインします。

ここではGoogleアカウントでログインする例を示します。「Googleで続ける」ボタンをクリックします。

<img width="600" height="599" alt="Image" src="https://github.com/user-attachments/assets/52c0edb5-ddb7-4034-a451-64e1ce535a9f" />

Googleアカウントで登録した場合、「Claude」から「claude.com」を使用してサインインしようとしています、という画面が表示されます。

「アプリとWebサイトにあなたに関する情報を共有することを許可します。」と表示されたら、「続ける」ボタンをクリックします。

<img width="305" height="347" alt="Image" src="https://github.com/user-attachments/assets/7df77502-a39d-4e34-aea8-cfb9eb582c3e" />

「Claude」に移動画面が表示されたら、Googleアカウントをクリックしてログインします。

続いてClaudeに再ログインしようとしている画面が表示されるので、規約を確認して「次へ」をクリックします。（初回ログインでは表示されない可能性があります）

---

### 3-3. 作業フォルダを準備する

「フォルダを選択」をクリックします。

`claude` フォルダを作成して選択します。

本資料では「claude」フォルダを例として使用します。フォルダ名は任意です。

---

### 3-4. ワークスペースを信頼する

「ワークスペースを信頼しますか？」と表示されたら、「ワークスペースを信頼する」ボタンをクリックします。

※ Claudeデスクトップアプリ単体でファイルの閲覧・編集が可能です。VSCodeなど別のエディタを併用したい場合は、任意のタイミングで同じフォルダ（例：/Users/アカウント/claude）を開いてください。

---

### 3-5. 主なペインを確認する

Claudeデスクトップアプリでは、複数のペインを自由に配置できます。
ペインとは、画面を分割して表示する区画（パネル）のことです。

各ペインはドラッグして配置やサイズを変更でき、「Views」メニューから表示・非表示を切り替えられます。

主なペイン：

- Chat — チャット入力欄と会話履歴
- Diff — 変更内容の確認
- Browser — ブラウザ表示
- Terminal — ターミナル操作
- File — ファイルの閲覧・編集
- Plan — 作業計画の作成
- Tasks — バックグラウンド処理の確認
- Subagent — サブエージェントの出力

---

## 4. Claude Codeの基本的な使い方

### 4-1. コード生成を試す

次のようなプロンプトを入力してみましょう。

- Hello Worldを表示するJavaScriptを作成してください
- hello.js をNode.jsで実行してください
- index.htmlを作成し、シンプルなランディングページを作成してください

---

### 4-2. コードを改善する

- 関数にエラーハンドリングを追加してください
- このファイル全体をTypeScriptへ書き換えてください

---

### 4-3. コードの品質を向上させる

- 可読性を高めるようにリファクタリングしてください
- ESLint / Prettier に準拠するよう整形してください
- JSDocコメントを追加してください
- モデルとビューを分離してください

---

### 4-4. コードを理解・デバッグする

- @script.js このコードを初心者向けに説明してください
- この正規表現を解説してください
- このアルゴリズムを解説してください
- このエラーを修正してください

---

### 4-5. Git連携を試す

Claude CodeではGit操作も依頼できます。まずコミットメッセージを提案してもらい、内容を確認してから実際にコミットする、という2段階の流れがおすすめです。

1. 日本語でコミットメッセージを提案してください
2. （提案内容を確認後）そのままコミットしてください

---

### 4-6. プロジェクト設定を行う（CLAUDE.md） 

CLAUDE.md は、プロジェクト専用の「Claudeへの指示書」です。

プロジェクト直下に CLAUDE.md を配置すると、
そのプロジェクトを開くたびにClaude Codeが自動で読み込みます。

例えば、次のような内容を記載しておくと便利です。

- コーディング規約
- 使用する言語
- 命名規則
- Gitの運用ルール
- コミットメッセージのルール

Claude Codeでよく使う操作を一通り確認しました。
次は実際にTodoアプリを作成しながら、一連の開発フローを体験します。

---

## 5. ハンズオン

実際にClaude Codeへ指示を出しながらTodoアプリを作成します。

HTML/CSS/JavaScriptのみを使用して、最後にREADMEの作成、テスト、Gitコミットまでこなうことで、Claude Codeを使った一連の開発フローを体験します。

### 5-1. todo_appフォルダを作成する

todo_appという名前のフォルダを作成してください

---

### 5-2. Gitリポジトリを初期化する

作成したtodo_appフォルダ内でGitリポジトリを初期化してください

---

### 5-3. Todoアプリを作成する

HTML/CSS/JavaScriptのみを使用して、次の機能を持つTodoアプリを作成してください

- Todoの登録
- Todoの一覧表示
- Todoの編集
- Todoの削除

---

### 5-4. テスト項目を作成する

作成したTodoアプリからテスト項目（チェックリスト）を作成してください

---

### 5-5. テストを実施する

作成したテスト項目に沿って、ブラウザでの動作確認（手動テスト）を行ってください

さらに、テスト結果を表示してください

---

### 5-6. README を作成する

todo_appフォルダに、README.mdを作成してください

README.mdには次の内容をまとめてください。
 
- プロジェクト概要
- 使用技術
- セットアップ方法
- 使い方
- ディレクトリ構成

---

### 5-7. Gitコミットを行う

1. git status を確認してください

2. ここまでの変更内容を確認し、適切なコミットメッセージを提案してください

3. 提案内容を確認します

4. その内容でコミットしてください

---

## 6. Claude Code(CLI)をターミナルで使う

### 6-1. Claude Codeをインストールする

（[Claude Code Documentation](https://code.claude.com/docs/en/overview)）
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

### 6-2. PATHを設定する

Claude Code コマンドをどこからでも実行できるようにPATHを設定します。

（zshの場合。bashの場合は `~/.bashrc` に読み替えてください）

```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc && source ~/.zshrc
```

新しいターミナルを開き、以下のコマンドを実行し、インストールされていることを確認します。

```bash
claude --version
```

```text
2.1.215 (Claude Code)
```

バージョン番号は執筆時点の例です。実際に表示される値はインストール状況により異なります

---

### 6-3. Claude Codeの初期設定を行う

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

### 6-4. テーマを選択する

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

### 6-5. ログイン方法を選択する

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
3. サードパーティ・プラットフォーム（Amazon Bedrock、Microsoft Foundry、Vertex AI）

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

Enterキーを押します。

---

### 6-6. ターミナルの推奨設定を有効にする

```text
Use Claude Code's terminal setup?
 
For the optimal coding experience, enable the recommended settings
for your terminal: Option+Enter for newlines and no audible bell
    
❯ 1. Yes, use recommended settings
  2. No, maybe later with /terminal-setup
    
Enter to confirm · Esc to skip
```

日本語訳：Claude Codeのターミナル設定を使用しますか？

「1. はい、推奨設定を使用する」を選択します。

---

### 6-7. ワークスペースを信頼する

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

## 7. 安全にファイルを削除する

### 7-1. rm コマンドの動作を理解する

Claude Codeは、ファイルやフォルダの削除時に通常の`rm`コマンドを実行します。

`rm`コマンドは、ごみ箱を経由せず削除するため、誤って実行すると復元が困難になる場合があります。

そこで本章では、`rm`コマンドを`trash`コマンドへ置き換え、安全に削除できるように設定します。

前提：

macOSで確認しています（Appleネイティブの `trash`コマンドは macOS Sequoia (15) 以降 のみ搭載。Sonoma (14) 以前では標準搭載されていないため、後述のHomebrew版が必要です）。

Claude Codeへファイルやフォルダの削除を依頼する機会は少なくありません。

既定では`rm`コマンドが実行されるため、削除した内容はごみ箱を経由せず、そのまま削除されます。

そこで、`rm`コマンドを`trash`コマンドへ置き換え、削除したファイルやフォルダがいったんごみ箱へ移動するよう設定します。

### 7-2. trashコマンドを確認する

ターミナルから以下のコマンドを実行して、`trash`コマンドが利用可能か確認します。

```bash
which trash
```

```text
/usr/bin/trash
```

と表示されたらtrash がインストール済みです。

### 7-3. trashコマンドをインストールする（未インストールの場合）

`which trash` コマンドを実行しても何も表示されなかった場合は、Homebrewからインストールしてください。

```bash
brew install trash
```

Homebrewでインストールした`trash`コマンドを利用できるよう、PATHを設定します。

Apple Siliconの場合

```bash
echo 'export PATH="/opt/homebrew/bin:$PATH"' >> ~/.zshrc
```

Intel Macの場合

```bash
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.zshrc
```

### 7-4. rm を trashに置き換える

以下のコマンドをターミナルで実行します。

```bash
grep -qF 'rm() {' ~/.zshrc || cat >> ~/.zshrc << 'EOF'

rm() {
  while [[ "$1" == -* && "$1" != "--" ]]; do
    shift
  done
  [[ "$1" == "--" ]] && shift
  trash "$@"
}
EOF
```

.zshrc を更新したら、次の手順で設定を反映します。

### 7-5. 設定を反映させる

```bash
source ~/.zshrc
```

とすると、`rm`コマンドが入力されたら `trash`コマンドに自動的に変わります。



### 7-6. 動作確認する

Claude Codeに実際に削除を依頼して、rmコマンドをtrashコマンドに置き換える設定が効いているか確認します。

1. Claude Codeに、作業フォルダ（例：`~/claude`）直下にtempフォルダを作成し、その中にテスト用のファイルを作成するよう依頼します。
（例：「作業フォルダ直下にtempフォルダを作成し、その中にtest.txtというファイルを作成してください」）

2. 作業フォルダのtempフォルダの中に test.txt が作成されたことを確認します。
（例：目視で確認します）

3. Claude Codeに、そのtempフォルダとその中身を削除するよう依頼します。
（例：「tempフォルダを削除してください」）

4. 作業フォルダからtempフォルダが消えていることを確認します。
（例：目視で確認します）
  
5. Finderで「ごみ箱」を開き、tempフォルダが入っていることを確認します。

作業フォルダからtempフォルダが消えていて、かつごみ箱に tempフォルダが入っていれば、 Claude Codeからの削除依頼が `rm`コマンド ではなく `trash`コマンド 経由で行われ、完全消去ではなくごみ箱へ移動していることが確認できます。

※ この確認が重要なのは、Claude Codeがコマンドを実行するときのシェル環境が `.zshrc` を読み込んでいるとは限らないためです。手元のターミナルで `rm` の設定を確認できても、Claude Code自身が同じ設定を使ってコマンドを実行するとは限りません。実際にClaude Codeへ削除を依頼して結果を確認するのが、最も確実な検証方法です。

もしごみ箱に入らずtempフォルダが完全に消えてしまった場合は、Claude Codeが使うシェル環境が `.zshrc` を読み込んでいない可能性があります。参考として、手元のターミナルで以下を実行すると、少なくともそのターミナル上で `rm` がシェル関数として解決されているかを確認できます（`command -v` はパスを伴わず名前だけが表示されれば関数として解決されている、という意味です）。

```bash	
command -v rm	
```

```text	
rm	
```

---

## 8. 次のステップ

Todoアプリが完成したら、次は次のような開発にも挑戦してみましょう。

- TypeScript版への書き換え
- Reactでの実装
- Vue.jsでの実装
- APIとの連携
- テストの自動化

Claude Codeは、コード生成だけでなく、設計・リファクタリング・テスト・ドキュメント作成まで支援できるAIエージェントです。

ぜひさまざまなプロジェクトで活用しながら、開発スタイルに合った使い方を見つけてみてください。
