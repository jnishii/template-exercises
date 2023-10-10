# プログラミング環境の準備

エディタは好きなのを使えばよいが，最近世界中でよく使われているのはVisual Studio Codeは以下から取得する。

[Visual Studio Code](https://code.visualstudio.com/download)
- Windows, Mac, Linux いずれでも使える


# GitHubの準備

## 準備0: GitHubの基本用語
以下の「Gitの基本用語」のページを読む

- [Gitの基本用語](http://bcl.sci.yamaguchi-u.ac.jp/~jun/notebook/git/intro)

## 準備1: 手元のマシンの準備
Gitを使う方法を大別すると2通りある。**長期的には方法1を使えるようにする** こと。短期的には方法2でもいいが，使い方は各自調べること。

### [方法1] コマンド直打ちで使う**

- Windowsの場合は以下を見てGit Bashを使えるようにすれば，LinuxやMacと同様にターミナル上で操作できる(はず...)。
	https://qiita.com/shinsumicco/items/a1c799640131ae33c792
- Mac/Linuxはターミナル上で，以下のURLにある「準備3」を実行しておく。
	- [GitHubを使う準備](http://bcl.sci.yamaguchi-u.ac.jp/~jun/notebook/git/preparation)

### [方法2] GitHub DeskTopをつかう

- [GitHub DeskTop](https://desktop.github.com/) からダウンロードする。
- 使い方は各自google先生に教わる。

## 準備2: 公開鍵認証設定

[研究室のメモページ](https://github.com/bcl-group/memo/wiki)のGitHubのコーナーを見る

1. 「GitHub の公開鍵認証設定」の内容を実行
2. 「GitHub のプロキシ設定」も見ておく

https://github.com/bcl-group/memo/wiki

## 準備3: GitHub上に実習用リモートレポジトリを準備

1. Slack等で連絡があったリンクをクリック(プレ配属用リポジトリを準備する)
2. 表示された画面で"Accept this assignment"をクリック。
3. GitHubに登録したアドレスにメールが届くので”View invitation”をクリックしてGitHubにログイン。
3. これでGitHub上にリモートレポジトリができる。


## 準備4: ローカルレポジトリの内容をリモートレポジトリに反映

ここからの作業は，前述の「準備1」の2つ方法のどちらを使うかで方法が異なる。

### 方法1: コマンド直打ちで

1. ターミナルを開き，作業用のフォルダを作り，その中に移動する。
2. 上記(準備2)が終わったときGitHubの画面に表示されているコマンドを実行する。大体以下のような内容のはず。
```bash
$ echo "# 〇〇を使った〇〇の作成" <=自分のしたことをわかりやすいタイトルにする
$ git init
$ git add .
$ git commit -m "はじめてのcommit"
$ git remote add origin https://github.com/... <=このリポジトリ名は各自異なる
$ git push -u origin main
```
- リポジトリ名はGitHubのページの上の方にコピーリンクとともに表示される。
- このあたりのコマンドの解説は以下にもある。
	- [リポジトリの作成](http://bcl.sci.yamaguchi-u.ac.jp/~jun/notebook/git/init)

### 方法2: GitHub Desktopで

GitHub Desktopの使い方はgoogle先生に聞く。

1. GitHub Desktopを起動して，ローカルレポジトリの場所と，上記リモートレポジトリの登録をする。
2. ローカルレポジトリの内容をリモートレポジトリにpushする。

ブラウザでGitHubのページを見て，リモートレポジトリにファイルがアップロードがされていれば成功。


## 更新情報のアップロードをする

ローカルリポジトリの内容を修正したら，1日1回は GitHubに反映しましょう。

一部のファイルを修正したり，ファイルの追加をしたときは，以下のようにGitHubのリモートリポジトリに反映する。(コマンド直打ちの例)

```bash
$ git status  # 追加・更新したファイル一覧表示(省略可)
$ git add .   # 追加・更新したファイル全てをgitに反映する
$ git commit -m "修正点を簡単にかく"  # 更新情報をローカルレポジトリに反映
$ git push origin main # 更新情報をローカルレポジトリにGitHubに反映
```

その他，自宅のパソコン等にGitHubのレポジトリをクローン(ダウンロード)する方法等の詳細は以下を参照のこと。

- [リポジトリの操作](http://bcl.sci.yamaguchi-u.ac.jp/~jun/notebook/git/commands)
