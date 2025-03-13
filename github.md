---
title: Github
description: 
published: true
date: 2025-03-13T10:30:35.166Z
tags: 
editor: markdown
dateCreated: 2025-03-13T10:20:58.511Z
---

# Githubとは?
[Github](https://github.com)とはソフトウェア開発プラットフォームであり、バージョン管理にGitを使っています。
あと、GitとGithubは別物です。Javaと紅茶ぐらい違う。

## Git(Github)環境の整備
GitとVSCode入れてればだいたい戦えます。そのほかはお好みで

#### 必須項目
[Git](https://git-scm.com/downloads/win)をインストールする

#### Optional
VSCodeのExtention
* [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
> コードの編集履歴とかがいい感じに見れる
{.is-info}

デスクトップアプリケーション
* [Github Desktop](https://desktop.github.com/download/)
> そこそこわかりやすいGUIでGithubがいじれます
{.is-info}

## Git(Github)の基礎用語について

[ここ](https://qiita.com/shinshingodmt/items/637cf9e5c6660509c460)がわりとよくまとまっています

## Git(Github)の基本操作について

あくまで一例です。ほかにもやり方はたくさんあります
一応、できるだけGUI上で完結するようにまとめたつもりです。
### リポジトリの作成
Githubをブラウザで開いて作るのが楽です。[ここ](https://github.com/new)にアクセスすることで作ることもできます。

### VSCodeでGithubアカウントにログインする
左下のAccountsをクリックしてなんかそれっぽいことをしたらログインできます(書きかけ)

### Clone
リモートリポジトリからコードベースをクローンするためにはわりといくつかの方法がありますが簡単な方法として、VSCodeからクローンする方法を紹介したいと思います

まず、クローンしたいGithubリポジトリを開き、そののCodeボタンを押すと出てくるポップアップからHTTPSを選択し、コピーボタンを押すことで、リポジトリのURLをコピーできます
![githubrepourl.png](/githubrepourl.png)
そして、 `View`タブを開き、`Command Palette`をクリックし、`git clone`と入力し、enterを押します。
そして、リポジトリのURLを入力して、リポジトリをどこに配置するかを選択することでGithubリポジトリがクローン出来ます。

### Pull Requestの作成
VSCodeの`Source Control`タブの`Create Pull Request`ボタンをクリックすることで作れます。
![source_controll_pr.png](/source_controll_pr.png)

### Branchの作成
