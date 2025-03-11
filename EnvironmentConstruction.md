---
title: 環境構築
description: 
published: true
date: 2025-02-22T12:29:44.101Z
tags: 
editor: markdown
dateCreated: 2025-02-22T12:23:08.562Z
---

# 環境構築
最悪メモ帳でもModpackはかけないことはないですが、適切なツールを用いることで快適なコーディングが可能となります。
前提条件として、Kubejsを利用したコーディングを想定しています。
また、このセットアップは一例であり、宗派によって"正解"が異なります。

## Visual Studio Code(VScode)のインストール
[VScodeのダウンロードページ](https://code.visualstudio.com/Download)からVScodeをインストールします。
お手持ちのOSに適したインストーラーをダウンロードしてください。
<img src=/vscdl.png width=50%>
インストーラーは基本的に"次へ"を連打すればよいですが、[Codeで開く]アクションを追加する、の2つの項目を有効にすることを推奨します。
<img src=/installer.png width=50%>
そしたら、VScodeを起動したら以下のような画面になるはずです。
<img src=/vscview.png width=75%>
VScodeは拡張機能をインストールすることが可能であり、拡張機能をインストールすることでよりよいコーディングができます。
### おすすめExtension
- [Japanese Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ja)
- [IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)



## Probejsまわり
まず、Probejsを入れます。Kubejs単体では縛りプレイです、あなたがド変態なドMなら...まぁうん、そういう性癖もありだと思いますよ。
Minecraft内で`/probejs dump`を実行することでKubejsフォルダ配下にTypescriptによる型アノテーションが生成されます。
そうすると、VScodeの予測とかが割と賢くなったり、関数の引数がわかったりします。

## VScodeの開き方
エクスプローラーを開いて、kubejsフォルダ内で右クリックをし、"Codeで開く"をクリックすることで開くとVScodeくんがいい感じに力を発揮してくれます。
また、上のバーからFileを選択し、Open FolderでKubejsフォルダを開くのもあり


## だいたいおわり。
これで最低限は書けるようになると思います。