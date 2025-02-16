---
title: Kubejs
description: 現代の代表的なminecraft改変mod、kubejsについて学びます。
published: true
date: 2025-02-08T05:43:04.758Z
tags: kubejs
editor: markdown
dateCreated: 2025-02-02T02:56:30.735Z
---

# Kubejs

Kubejsとは、サーバー/クライアントで動作するModであり、Javascriptを利用して、アイテムの追加やJavaのクラスの呼び出し等ができるModです。

## Kubejsスクリプトの配置場所
`mods`の一個上のディレクトリに、Kubejsを入れた状態でMinecraftを起動すると、`kubejs`ディレクトリが生成されます。  
そこには、Kubejsスクリプトが配置される、
`startup_scripts`,`server_scripts`,`client_scripts`
ディレクトリが存在します。

## Kubejsのスクリプトの種類について
`startup_scripts`  
「何か新しい物を登録/既存のアイテムを変更する」「プレイヤーの描画に影響する」「ワールド内に影響する」すべてを含むものがここに含まれます。
例：アイテム/ブロックの登録
　　既存のアイテム/ブロックの変更  
　　Forgeのイベントリスナーの追加 

`server_script`
「サーバーにのみ影響する」「[レシピを変更する](/ja/kubejs/editingRecipe)」「ブロックを破壊する」等がここに含まれます。
例：アイテムのレシピの変更
　　ドロップアイテムの変更
　　ブロックなどを使用した時に発生するイベントの設定

`client_script`
「テクスチャの変更」「ツールチップの変更」「ログの生成」等の描画関連かつサーバーに関係ない物がここに含まれます。
例：JEIへ説明の追加、レシピを隠すなど。


基本的に作業を行うのはserver_scriptであり、startup_scriptは自作コンテンツを作り出す場合のみさわることになります。client_scriptはほとんど触りませんが、覚えておくとプレイヤーが便利になります。
