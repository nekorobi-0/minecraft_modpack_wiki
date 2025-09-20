---
title: おすすめmod
description: どのmodを入れるべきか解説。
published: true
date: 2025-09-20T21:52:23.097Z
tags: mods, 軽量化, qol
editor: markdown
dateCreated: 2025-02-07T20:53:29.515Z
---

# はじめに

modというのは豊富なもので、少しの便利機能を追加するもの、大きな要素を追加するものなど大量にあります。（curseforgeの累計mod数が10000越えなのもそれを物語っています。）  
ですが、そこまで量が多いと取捨選択や新しいmodの発見も慣れがいります。  
ここではそのコツや具体的に何を入れたらいいのかについて解説します。

# modのジャンルと組み合わせ

modには様々なジャンルがあります、軽量化、QoL(Quality of Life)、工業、魔術etc...  
など、その中で特に重要なのは軽量化とQoLです。  
どちらも文字通りマイクラを軽くして便利にするものです。

## 軽量化

軽量化については様々なものがありますが、安定性があり多く使われている物を選ぶといいでしょう（不安定、競合が多いと利用者に不快感を与えたり、入れれないmodがあったりとmodpack作りに制限がかかるからです。）  
まず入れるべきmodを紹介します。

---
-   [Sodium](https://www.curseforge.com/minecraft/mc-mods/sodium) (ver:Fabric:1.16.3~1.21.4)
-   [Embeddium](https://www.curseforge.com/minecraft/mc-mods/embeddium) (ver:(Neo)Forge:1.16.4~1.21.4)
-   [Angelica](https://www.curseforge.com/minecraft/mc-mods/angelica) (ver:Forge:1.7.10)  
(ここに書かれているバージョンは目安です。)  
これらはminecraftの描画を最適化し大きく軽量化するmodです。  
次に入れるべきはEntity Cullingです。

---
-   [Entity Culling](https://www.curseforge.com/minecraft/mc-mods/entityculling) (ver:Fabric&(Neo)Forge:b1.7.3,1.7.10~1.21.4)
これは見えない物を描画しないことで軽量化するものです。
---
- [FerriteCore](https://www.curseforge.com/minecraft/mc-mods/ferritecore) (ver:Fabric&(Neo)Forge:1.16.5~1.21.4)
- [VintageFix](https://modrinth.com/mod/vintagefix) (ver:Forge:1.12.2)
これはメモリの使用量を最適化します。
---
- [Lithium](https://modrinth.com/mod/lithium) (ver:Fabric:1.16.2~1.21.4,NeoForge:1.21.1\~1.21.4)
- [Radium](https://modrinth.com/mod/radium) (ver:(Neo)Forge1.20.1~1.21.1)
- [Canary](https://modrinth.com/mod/canary) (ver:Forge:1.20.4~1.18.2)
- [RoadRunner](https://www.curseforge.com/minecraft/mc-mods/roadrunner) (ver:Forge:1.16.5,1.19.2)
様々な最適化をします。
---
- [ModernFix](https://modrinth.com/mod/modernfix) (ver:Fabric&(Neo)Forge:1.16.4~1.21.4)
様々な軽量化とパッチ
---
- [Phosphor](https://modrinth.com/mod/phosphor) (非推奨)(ver:Fabric:1.16.5~1.19.2)
- [Radon](https://modrinth.com/mod/radon) (非推奨)(ver:Forge:1.16.5~1.19.4)
- [Alfheim](https://modrinth.com/mod/alfheim-lighting-engine) (ver:Forge:1.12.2)
- (fabric版)[Starlight](https://modrinth.com/mod/starlight)|(Forge版)[Starlight](https://modrinth.com/mod/starlight-forge)|(NeoForge版)[Starlight](https://modrinth.com/mod/starlight-neoforge) (ver:Fabric&(Neo)Forge:1.17~1.20.4)
- [Moonrise](すこし非推奨)(https://modrinth.com/mod/moonrise-opt) (ver:Fabric&(Neo)Forge:1.21.1~1.21.4)
ライトニングエンジンの軽量化
---
- [Noisium](https://modrinth.com/mod/noisium) (ver:Fabric&(Neo)Forge:1.20~1.21.4)
チャンク生成の最適化
---
- [BadOptimizations](https://modrinth.com/mod/badoptimizations) (ver:Fabric&(Neo)Forge:1.19.1~1.21.4)
雑多な最適化
---
- [Lightspeed](https://modrinth.com/mod/lightspeed) (ver:Forge:1.16.5~1.19.2)
ロード時のキャッシュによるロード時間の短縮
---
- [Saturn](https://modrinth.com/mod/saturn) (ver:(Neo)Forge:1.16.5~1.21.1)
メモリ使用量の削減
---
- [Palladium](https://modrinth.com/mod/mpalladium) (ver:Fabric:1.19.4~1.21.4,(Neo)Forge:1.20.1\~1.21.1)
AIと描画の最適化
---
- [Graphene](https://modrinth.com/mod/graphene) (ver:Fabric:1.20.1~1.21.8 ,(Neo)Froge:1.12.2/1.19.2~1.21.8,Quilt:1.20.1)(MPEMの後継)
非同期処理やイベント、描画最適化
---

主な軽量化modに関してはこれぐらいです。
1.7.10や1.12.2にはもう少しありますが、それらに関してはまた別のページで紹介します。
さてもっと軽量化したいというあなたに軽量化modを探すときのポイントを教えます。
まず1つ目には取り敢えず検証する、これが大切です。
バニラ環境、メジャーmod環境など比べてどのくらい速さが異なるかこれが大切です。
2つ目は何をしているか読む、これも大切です。
一口に軽量化modと言っても最適化している部分はそれぞれ異なります、それ故にここの最適化なのかと知っておくことで無駄だったmodの排除や競合の時の解決にも役立ちます。
最後はとにかく新しいのを調べろです。
mod界隈は新しいmodがたくさん生れています、それらを探すためにはmodrinth/curseforgeを探すだけではなくgithubから探す、redditなどから探すなど、様々な手段を使って探すことが大切です。
## QoL
少し横道にそれてしまいましたね、さてQoLというのはQuality of Life、直訳すると「生活の質」となります、これはサバイバル/クリエイティブで遊ぶとき、不便な部分や足りない分を補いより便利なマイクラにするというmodです。
このmodは軽量化modより多くcurseforgeでは9,145件も登録されています。
非常に多いため絞ってのご紹介となります。
「欲しい機能がある」や「もっと便利にしたい」という人などは検索なども利用して調べることをお勧めします

---
- [Mouse Tweaks](https://modrinth.com/mod/mouse-tweaks) (ver:Fabric&(Neo)Forge:b1.7.3~1.21.4)
インベントリ内のアイテム移動を便利化する。
---
- [Controlling](https://modrinth.com/mod/controlling) (ver:Fabric&(Neo)FOrge:1.7.10~1.21.4)
キー設定の便利化
---
- [Jade](https://modrinth.com/mod/jade) (ver:Fabric&(Neo)Forge:1.12.2~1.21.4)
- [The One Probe](https://modrinth.com/mod/the-one-probe) (ver:(Neo)Forge:1.9~1.21.1)
- [Waila](https://www.curseforge.com/minecraft/mc-mods/waila) (ver:Forge1.5.2~1.11.2)
見ているブロックの情報を表示
---
- [Crafting Tweaks](https://modrinth.com/mod/crafting-tweaks) (ver:Forge:1.7.10~1.21.4)
作業台のGUIの改良
---
- [Configured](https://www.curseforge.com/minecraft/mc-mods/configured) (ver:Fabric&(Neo)Forge1.15.2~1.21.4)
- [Catalogue](https://www.curseforge.com/minecraft/mc-mods/catalogue) (ver:Fabric&(Neo)Forge:1.16.3~1.21.4)
mod一覧とコンフィグ画面の改良
---
- [More Overlays](https://www.curseforge.com/minecraft/mc-mods/more-overlays) ([More Overlays Updated](https://www.curseforge.com/minecraft/mc-mods/more-overlays-updated)) (ver:Fabric&(Neo)Forge:1.8.9~1.21.1)
湧きつぶし箇所の表示やチャンクの境目の表示
---
- [Better Statistics Screen](https://modrinth.com/mod/better-stats) (ver:Fabric&Forge:1.18.1~1.21.4)
統計画面を改良
---
- [Modern UI](https://modrinth.com/mod/modern-ui) (ver:Fabric&(Neo)Forge:1.15.2~1.21.3)
文字の解像度を上げフォントを変える。(ツールチップも若干変わる)
---
- [Just Enough Items](https://modrinth.com/mod/jei) (ver:Fabric&(Neo)Forge:1.8~1.21.1)
- [Not Enough Items](https://modrinth.com/mod/nei) (ver:Forge:1.6.2~1.8)
- [Roughly Enough Items](https://modrinth.com/mod/rei) (Just Enough Itemsとの非互換性)(ver:Fabric&(Neo)Forge:1.13~1.21.4)
- [EMI](https://modrinth.com/mod/emi) (Just Enough Itemsとの互換性)(ver:Fabric&(Neo)Forge:1.21.1~1.18.2)
様々なクラフトのレシピが見れるようになるmod
---
などがあります、またこのほかにもQoLmodの追加機能mod(JEIのAddonなどがいい例です)もあり、自分の環境に合ったmodを探すことが大切です。
## Modpack用Mod

Modpackを作るうえで、レシピ変更、クエスト要素の追加などをすることで、充実したModapckライフを送ることができます。
そのために必要なModたちを紹介していきます。

### レシピ変更系
- [Kubejs](https://www.curseforge.com/minecraft/mc-mods/kubejs) (ver:Fabric&(Neo)Forge:1.16.5~1.21.1)
Javascriptでプログラムを書くことで[レシピ変更など](/kubejs)ができます。
- [CraftTweaker](https://www.curseforge.com/minecraft/mc-mods/crafttweaker) (ver:Fabric&(Neo)Forge:1.3.2~1.21.1)
ZenScriptという独自の言語を書くことでレシピ改変などができます。