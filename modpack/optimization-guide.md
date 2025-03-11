---
title: 最適化・軽量化のためのガイド
description: 最適化・軽量化を行いたい人向け
published: true
date: 2025-02-16T14:04:30.377Z
tags: 軽量化, 最適化
editor: markdown
dateCreated: 2025-02-16T13:58:18.809Z
---


ここでは、簡単に最適化・軽量化を行う方法を紹介します。
[「最適化・軽量化について」](/modpack/optimization)も読むことを推奨します。 
## 最適化・軽量化ガイド
1. **Modpackを作る際に[Simply Optimized(fabric)](https://modrinth.com/modpack/sop)や[Hammer(Forge/NeoForge)](https://modrinth.com/modpack/hammer)などの最適化Modpackを導入する。** これによってバニラ側の最適化はほとんど完了します。ただし、最適化のためにデフォルトでoffになっている機能を使用していることがあるためconfigフォルダ内を確認してください。(例：ModernFixの[Dynamic Resources](https://github.com/embeddedt/ModernFix/wiki/Dynamic-Resources-FAQ))
1. **必要な軽量化modを入れる。** 上記のModpackに入っているmod以外の軽量化modを導入することで更に負荷を抑えることができます。
1. **作成したModpackの負荷を調べ、対策する。** [Spark](https://modrinth.com/mod/spark)や[Observable](https://modrinth.com/mod/observable)などを使用し、Modpackの負荷を計測することで高負荷なmodを発見できます。

以上です。