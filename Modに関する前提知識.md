---
title: Modに関する前提知識
description: Mod、Modpackに関する前提知識をまとめたものです。
published: true
date: 2025-09-14T07:30:35.607Z
tags: 始めに
editor: markdown
dateCreated: 2025-09-08T15:02:39.294Z
---

### *このページについて*
*こちらは初心者向けに前提知識となるものを簡単にまとめたものです。
若干、偏見があります。
詳しくは他ページや外部サイトをご覧ください。*

# Mod、Modpackについて
Modとは所謂"改造ソフトウェア"です。ゲームに本来存在しない機能や要素を追加します。

基本的にゲームでのMod使用は不正行為ですが、**MinecraftではEULAによって定められている範囲でModの作成及び配布、使用が許可されています。**

Modpackとは平たく言うとModの詰め合わせです。
ただModを入れたものではなく、レシピ改変やconfig改変を行っています。

# Mod、Modpackのダウンロードについて
**Modは信用のできるサイトからダウンロードすることを強く推奨します。
掲示板や偽造サイト(CurseFire等)からのダウンロードは大いに危険です。**
　
　
**もしもマルウェアに感染したとしても自己責任です。**
**くれぐれも注意してください。**


## 主要なMod配布サイト
### CurseForge
リンク：https://www.curseforge.com/minecraft

最大手のMod配布サイト。非常に多くのModがダウンロードできます。
Minecraft以外のゲームも取り扱っています。親会社はOverwolf。
**ModローダーのForgeと直接の関係はないです。**
以下、CFと呼称します。

### Modrinth
リンク：https://modrinth.com/mods

強力な機能とコミュニティとの仲の良さが魅力のMinecraft専門のMod配布サイト。

### GitHub
リンク：https://github.com/

こちらはプログラマ用のSNSのようなものです。
配布サイトではありませんが、多くのModderはここにコードを公開しています。まれにここからしかダウンロードできないものもあります。

### 公式サイト
Modによっては公式サイトを用意してダウンロードする場所にしているものもあります。(Optifineなど)

## Modのダウンロード方法
1. 手動インストール

Modローダー（ForgeやFabricなど）を先にインストールし、Modファイルを `.minecraft/mods` フォルダ内に入れる方法です。**バージョンや前提Modの互換性を自分で確認する必要があります。**

2. 外部ランチャーを使った自動インストール

ランチャーがModや前提Modの依存関係を自動で解決してくれるため、手動よりも簡単でエラーが起こりにくい方法です。

## Modpackのダウンロード方法

Modpackは外部ランチャーを用いてダウンロードします。
外部ランチャーから直接ダウンロードするか、Modpackファイルを外部ランチャーで読み込むことで遊べます。
### Modpackのファイル形式について
Modやリソースパックにはライセンスがあるため、そのまま配布すると二次配布にあたり、ライセンス違反となる可能性があります。また、セキュリティ上のリスクも伴います。この問題を回避するため、ModpackはModなどをダウンロードURLなどに圧縮した形式で共有します。
これらのファイル形式は、対応した外部ランチャーで読み込むと、必要なModが自動でダウンロードされる仕組みです。

CurseForge形式: `.zip`ファイル。CurseForge AppやPrism launcherで扱えます。ただし、CurseForge App以外のランチャーの場合、CFのAPI制限により直接ダウンロードできないModがあります。その場合、誘導があります。

Modrinth形式: Modrinth独自の`.mrpack`ファイル。mrpack形式とも呼ばれます。Modrinth AppやPrism launcherで扱えます。

### Modpackファイルの読み込み方
外部ランチャーで読み込む方法は主に2つあります。
1. 起動構成の作成(又はそれに準ずるもの)からファイルを指定して、インポートする方法。
2. ファイルを外部ランチャーにドラッグアンドドロップでインポートする方法。

# 外部ランチャーについて
[詳細はここ](/ja/install-launcher)
MinecraftのModに特化したツールです。
Mojangの公式ランチャーとは異なり、Modの導入や管理を容易に行えるよう作られています。
また、データパックやリソースパック、シェーダーについてもまとめて管理できるのが特徴です。

## 主要な外部ランチャー
主要なランチャーにはPrism launcher、CurseForge App、Modrinth App、FTB App、GD launcher、AT launcherがあります。
ここではPrism launcher、CurseForge App、Modrinth Appの三つについて簡単な解説を行います。

### Prism launcher
リンク：https://prismlauncher.org/
CF、Modrinthの両方を対応
日本語対応 アリ
OSS Yes

コミュニティ製の外部ランチャーで非常に多機能かつ軽量。
一部のModはCFのAPI制約により直接ダウンロードできないため注意。

### CurseForge App
リンク：https://www.curseforge.com/download/app
CFのみ
日本語対応 アリ(不自然さがあります)
OSS No

CF製の外部ランチャー。CFのModを扱うため、Minecraft以外のmodも扱える。
公式ランチャー経由のためMicrosoft認証が不要という特徴がある。
容易に扱うことができることが魅力だが他のランチャーに比べて完成度は低い。

### Modrinth App
リンク：https://modrinth.com/app
Modrinthのみ
日本語対応 ナシ(対応予定)
OSS No

Modrinth製の外部ランチャーで、機能面とUIが魅力的。
CFのModを扱うことができないため注意。

- OSS(Open Source Software)について
*OSSはソースコードが一般に公開されており、誰でも自由に利用や修正ができるソフトウェアの総称です。透明性が高く、コミュニティによって活発な開発が行われます。*


# Modローダーについて
ModローダーとはModを動作させるための基盤となるソフトウェアです。
Modは特定のModローダー向けに開発されており、異なるModローダーでは基本的に動作しません。

## Forge
リンク：https://files.minecraftforge.net/net/minecraftforge/forge/
推奨バージョン: 1.1〜1.20.1

特徴: 最も主流だったModローダー。単なるModローダー機能だけでなく、多彩なAPIやバニラの改善機能も含まれている。大規模なModに多く利用される。

対応Modの例: 「黄昏の森」や「BuildCraft」など。

## NeoForge
リンク：https://neoforged.net/
推奨バージョン: 1.20.4〜

特徴: Forgeの開発トップメンバーの対立が原因でForgeから分岐したModローダー。現在はこちらが主流で、主観ではあるがMod開発も活発な印象。
Forgeとの互換性はない。(1.20.1のみ互換性アリ、1.20.1はサポートしておらず非推奨)


## Fabric
リンク：https://fabricmc.net/
推奨バージョン: 1.13〜

特徴: Forgeより新しいModローダーで、純粋なModローダーとしての機能のみを持つ。軽量で開発が速く、バージョンに依存しない動作が特徴。APIを補う必要があるため(Forgeと比較すると)前提Modが多くなる。中・小規模のmodが非常に多い。特にクライアント向けModが強力。

対応Modの例: Litematica、Tweakeroo、MiniHUDなど。


## Quilt
リンク：https://quiltmc.org
推奨バージョン: 1.14〜

特徴: Fabricから分岐したModローダー。不要な機能を無効化する機能により、Fabricよりも軽量化を行っている。しかし、開発速度が比較的遅いため、modに使われることは少ない。FabricのModのほとんどを読み込るが、開発速度が原因で新しいバージョンのModは扱えないものが多い。

### ローダー間の互換性について補足
*Forge/NeoForgeとFabricのModには基本的に互換性はないです。しかし、Sinytra ConnectorやKiltといった互換性を確保するためのパッチModが存在します。*

# その他

## ライセンスについて
Modには様々なライセンスが適用されており、開発者が定めた利用規約に従う必要があります。ライセンスはコードとアセット（テクスチャやモデルなど）で別に管理されることがあるため、それぞれのライセンスを確認することが重要です。
### 代表的なライセンス表記
MIT: もっとも一般的なOSSライセンス。改変や再配布が許可されている。

LGPL: OSSライセンスの一つ。ライセンスの継承などの制限がありますが、改変や再配布が許可されます。

ARR (All Rights Reserved): 非OSSライセンス。著作権者が全ての権利を保持しており、許可なく改変・再配布はできません。

## クラッシュレポート、ログについて
MinecraftをMod環境でプレイしていると、よくクラッシュします。そのクラッシュのエラー原因を特定するためにクラッシュレポート、ログを読むことが有効です。

クラッシュレポートは`.minecraft/crash-reports`、ログは`.minecraft/logs`内に作成されます。

**注意：ログやクラッシュレポートにはIPやPC名、オーディオ機器の名前が含まれることがあります。もし、他人に見せる場合は確認してから共有しましょう。
mclogsなどの共有サイトも有効です。**

## JVM引数（ひきすう）について
Java仮想マシン（JVM）の動作をカスタマイズするためのコマンドです。特に、メモリの割り当て量を調整するために使用されることが多く、Modを多数導入した際に発生するパフォーマンス問題を解決するのに役立ちます。

参考文献
https://github.com/Mukul1127/Minecraft-Java-Flags
https://unascribed.com/garden/jvm-args/

## Javaのバージョンについて
MinecraftはJavaで動作します。
しかし、Mojang公式のランチャーが使用するJavaは古いものが含まれている場合があり、リスクがあります。

セキュリティリスクを避けるため、使用するMinecraftのバージョンに合わせた最新のJava(Oracle JDKやTemurin JDK)をダウンロードして使用することを推奨します。

Java 8: Minecraft 1.16.5以下
Java 17: Minecraft 1.20.4以下
Java 21: Minecraft 1.20.5以降

例外: Cleanroomやlwjgl3fyなどの特定の環境では、推奨されるJavaバージョンが異なることがあります。

ダウンロードリンク：
Oracle: https://www.oracle.com/jp/java/technologies/downloads/
Temurin: https://adoptium.net/temurin/releases/

## サーバーとクライアントについて
Minecraftをマルチプレイする上で、クライアントとサーバーは異なる役割を持ちます。(一人でプレイする際には一台のPCで両方を実行しています。)

クライアント: ユーザーのPCで動作するゲーム本体です。
サーバー: 複数人でマルチプレイを行う際に、ゲームの状態を管理するコンピュータです。

Modの中には、クライアントとサーバーのそれぞれに導入が必要なもの、片方のみにダウンロードが必要なものがあります。

Modの対応状況は、CurseForgeやModrinthの配布ページで確認できます。

例：
- クライアント専用Mod: シェーダーやテクスチャ系Modなどのグラフィックを改善するmod。ソート機能などの操作を改善するMod。
- サーバー専用Mod: ゲーム内のルールや管理機能を変更するMod。アイテム追加しない地形生成系などのデータパックから来るMod。
- 両方必要なMod: アイテムやmobなどを追加するMod。レシピ表示modなどの便利系。