---
title: Subnetworkの使い方
description: 
published: true
date: 2025-06-06T15:00:03.569Z
tags: 
editor: markdown
dateCreated: 2025-06-06T14:49:22.805Z
---

# Storage Bus& ME Interfaceの使い方
俗に言うサブネットとかSSDとかと呼ばれているもの

## 前提知識

### ME Interface&ME Storage Busを貼り付けた形の挙動
**異なる**ネットワークに接続された`Interface`と`Storage Bus`を用意し、それぞれを接続できる形でおいたとき、
`Interface`側のネットワーク上にあるアイテムが`Storage Bus`側のネットワークに認識され、搬出入ができるようになります。
## 応用例
### 単純なチャンネル数の節約の例
`Annnihilation Plane`を複数枚並べるときに、一枚ごとにチャンネルを消費し、わりとめんどくさいという事があると思います。
そこで、`Annihilation Plane`のクラスター側に`Storage Bus`、メイン倉庫に`Interface`を配置すると、
`Annihilation Plane`側のネットワークは倉庫として`Interface`側のネットワークを認識しているので、そこにアイテムが搬入されるわけです。
なお、P2Pを使ったほうが楽というのはそう
### 負荷が許す限り無限に拡張できるネットワーク構築

---`Storage Bus`|`Interface`--`Storage Bus`|`Interface`---
とチェーンさせていくことによって、拡張性の高いMEネットワークが構築できます。
`Storage Bus`と`Interface`の間を区切りとし、1つのセグメントを形成することで同じパターンを永遠と繰り返すだけでお手軽設備拡張ができるわけです。
もちろん、中間のネットワークにも`ME Controller`や`P2P tunnel`が設置できるわけですから、セグメントのサイズを大きくすることも容易です。