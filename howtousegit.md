# Git,GitHubの使い方

## 自分のGitHubのページ

https://github.com/NishioRyota/


## init処理

コマンドラインを開きます git bash　を開く。
git bash の開き方はwin を押して gitで検索すると出てくる。

Gitのリポジトリを作成したいディレクトリに移動します。たとえば、/Users/username/myprojectというディレクトリにリポジトリを作成したい場合、次のコマンドを使用します（usernameはユーザー名に置き換えてください）：
```bash
cd /Users/username/myproject
```

initコマンドを使用して、新しいGitリポジトリを初期化します。次のコマンドを実行します：

```bash
git init
```
これにより、.gitという名前の隠しディレクトリが作成され、Gitリポジトリが初期化されます。

リポジトリが初期化されると、Gitはそのディレクトリ内のすべてのファイルとディレクトリを追跡します。これにより、リポジトリの状態や変更履歴を管理できるようになります。

必要に応じて、.gitignoreファイルを作成してGitが無視するファイルやディレクトリを指定することもできます。例えば、一時ファイルやコンパイルされたバイナリなどです。

これでinitの処理が完了し、Gitリポジトリが作成されました。以降は、ファイルの追加、コミット、ブランチの作成など、Gitの機能を使用してプロジェクトを管理することができます。

## 初期化が終わったら何をするか

### ファイルの追跡: 
Gitは初期化されたリポジトリ内のファイルを追跡しますが、まだ変更を検知していません。Gitがファイルの変更を追跡するためには、ファイルをステージングエリアに追加する必要があります。次のコマンドを使用して、すべての変更をステージングエリアに追加します：

```bash
git add .
```
.は現在のディレクトリ内のすべてのファイルを意味します。
特定のファイルのみを追跡したい場合は、ファイル名を指定します。

コミット: ステージングエリアに追加された変更をコミットして、リポジトリの状態を確定します。次のコマンドを使用して、変更をコミットします：

```bash
git commit -m "my first commit"
```
コミットメッセージには、コミットに関する説明や概要を記述します。コミットメッセージは他の開発者とのコミュニケーションや変更の追跡に役立ちます。

ブランチの作成: ブランチを作成して、変更の独立したセットを管理することができます。ブランチは、開発の並行処理や機能の追加などに役立ちます。次のコマンドを使用して、新しいブランチを作成します：

```bash
git branch -M main
```
ブランチ名には、新しいブランチの名前を指定します。

これらの手順を実行することで、ファイルの追跡、コミット、ブランチの作成が可能になります。Gitにはさまざまな機能がありますので、プロジェクトの要件やワークフローに応じて適切なGitコマンドを使用してください。

## pushする


### GitHubにpushするためには、以下の手順に従って進めます。

GitHubアカウントの作成: もしまだGitHubアカウントを持っていない場合は、GitHubのウェブサイトで新しいアカウントを作成してください。

リモートリポジトリの作成: GitHub上にリモートリポジトリを作成します。GitHubのウェブサイトで「New repository」ボタンをクリックし、リポジトリ名や説明などの詳細を入力して新しいリポジトリを作成します。

ローカルリポジトリとの関連付け: 既存のローカルリポジトリとGitHubのリモートリポジトリを関連付けます。次のコマンドを使用して、リモートリポジトリのURLを指定します：

```bash
git remote add origin リモートリポジトリのURL
```
originはリモートリポジトリの名前で、任意の名前を使用できます。

コミットのプッシュ: ローカルのコミットをリモートリポジトリにpushします。次のコマンドを使用します：

```bash
git push origin ブランチ名
```
ブランチ名には、プッシュしたいローカルブランチの名前を指定します。デフォルトでは、メインブランチはmasterと呼ばれています。

例えば、メインブランチにコミットをプッシュする場合は、以下のコマンドを使用します：

```bash
git push origin master
```
必要に応じて、他のブランチに切り替えてからpushすることもできます。

これで、ローカルのコミットがリモートリポジトリにpushされます。GitHubのウェブサイトでリポジトリを確認すると、プッシュされた変更が反映されているはずです。

## まとめ

gitを初期化して、GitHubにプッシュするにはつぎのコマンドを打つ。
適宜プロジェクト名は変更して使う。

初回
```bash
git init
git add .
git commit -m "my first commit"
git branch -M main
git remote add origin https://github.com/NishioRyota/my_test.git
git push -u origin main
```

２回目以降
```bash
git add .
git commit -m "second commit"
git push -u origin main
```