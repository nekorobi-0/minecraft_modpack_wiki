---
title: レシピの改変
description: レシピの追加、編集及び削除を行います
published: false
date: 2025-02-23T13:55:36.163Z
tags: kubejs
editor: markdown
dateCreated: 2025-02-07T13:57:55.403Z
---

<!-- ほとんどKubeJSWikiの引用になると思います-->
> なうわーきんぐ
{.is-info}

> ここではJavaScriptについて深く解説しません
{.is-warning}

# レシピの改変
レシピイベントを使用することで、レシピ追加の編集や削除できるようになります。

前述されているとは思いますが、ここでのスクリプトは`kubejs/server_scripts`内に配置し、`Minecraft`内で`/reload`コマンドを使用することで適用できます。

---
レシピの変更には`recipes`イベントへと登録する必要が有ります。
`ServerEvents.recipes`等を行うことにより、そのイベントに登録することができるようになります。

また、スクリプトの書き方はMCバージョン`1.19.2`から**変更されたため注意**してください。



### Tabs {.tabset}
#### 1.19.2+
```js
//ServerEvents.recipes(callback) は関数を受け取る関数で、
//コールバックと呼ばれています。
//このコールバックが動作するタイミングは、
//サーバーがレシピを登録するタイミングになります。
//コールバックが動作することを、"発火"などと言ったりします。

//"recipes"をサーバーから取得できるまで待機します。
ServerEvents.recipes(event => {
  //"event"の部分は任意の名前に変更できます。 "e"でもOK
  
  //ここにたくさんのレシピを変更するスクリプトを挿入
  
  console.log("レシピイベントが発火されました！")
})

```
#### 1.18.2
```js
//onEvent("recipes", callback) は関数を受け取る関数で、
//コールバックと呼ばれています。
//このコールバックが動作するタイミングは、
//サーバーがレシピを登録するタイミングになります。
//コールバックが動作することを、"発火"などと言ったりします。

//"recipes"をサーバーから取得できるまで待機します。
onEvent("recipes", event => {
  //"event"の部分は任意の名前に変更できます。 "e"でもOK
  
  //ここにたくさんのレシピを変更するスクリプトを挿入
  
  console.log("レシピイベントが発火されました！")
})

```
### 
これが正しく実行されていれば、レシピを編集する準備が整ったと言えるでしょう。
ここからのコードは、このコールバック内に書かれることを想定しています。
# レシピの追加
このセクションでは様々なレシピを追加する方法について解説します。
## 定型レシピ
TNTや、鉄つるはしのような定型レシピです。
`event.shaped()`で登録できます。

引数の説明
1. 出力アイテム(max: 64)
2. 文字列(最大3文字)で作業台の横行を表現し、それを最大3つの配列で表現。スペースはアイテムのないスロットを表現し、文字はアイテムを表現します。文字自体に意味を付けるのはこの後の作業です。
3. 文字にアイテムを結びつけるオブジェクト`{key: Item}`。入力アイテムは1つずつのみです。

```js
//丸石を4つの土で囲むことでダイヤモンドを3つ作るレシピ
event.shaped(
  //minecraftに限りMODIDは省略可能です
  "3x minecraft:diamond", 	//引数1: 完成品のアイテム
  [
  	" D ",									//引数2: これを作るためのアイテム配置
    "DCD",
    " D "
  ], {
  	D: "dirt",							//引数3: 文字とアイテムの紐づけ
    C: "cobblestone"
  }
)

event.shaped(
  //kjsではデフォルトでミラーリングと縮小が行われるため、
  //UU-Matterライクなレシピを作るにはそれを無効にする必要が有ります。
  //noMirror関数とnoShrink関数を併用することでこれを可能にします。
  "8x diamond",
  [
  	"S ",
    " S"
  ], {
    S: "stick"
  }
).noMirror().noShrink()

//ネザライトの剣をネザライトインゴットで囲うと不可壊になるレシピ
event.shaped(
  //kjsで用意されてる関数を使えば個数を引数で指定したり、
  //入力、出力アイテムにNBTをつけることができる
  Item.of("netherite_sword").withNBT("{Unbreakable:1b}"),
  [
    "BBB",
    "BSB",
    "BBB"
  ], {
    //Ingredient.of()を使えばタグでアイテムを指定できる
    B: Ingredient.of("#c:netherite_ingots"),
    //材料にNBTをつけるには.weakNBT()が必要
    S: Item.of("netherite_sword").withNBT("{Damage:0}").weakNBT()
  }
)
```
## 不定形レシピ
染料の混合のような決められた配置のないレシピを追加します。
`event.shapeless()`で登録できます。
1. 出力アイテム(max: 64)
2. 入力アイテムの配列。 アイテムの合計が9つまででなければなりません。
```js
event.shapeless(
  "6x tnt",       //引数1: 出力するアイテム
  [
  	"bone_meal",  //引数2: 入力するアイテム
    "4x sand"     //ここでの複数指定は同じアイテムを複数スロット分
                  //という解釈にされます
  ]
)
```

## 精錬及び調理レシピ
このセクションで解説する関数はとても似通っており、1つの入力(単一アイテム)から1つの出力(max: 64)を返すだけです。
ここで燃料について変更を加えることはできません。
<!--あとで燃料の奴書くかもしらん？-->
- 精錬レシピを追加するには `event.smelting()`
- 溶鉱レシピを追加するには `event.blasting()`
- 燻製レシピを追加するには `event.smoking()`
- 焚火レシピを追加するには `event.campfireCooking()`

経験値量の編集には`.xp(xp: Float)`関数を用いることでできます。
調理時間の編集には`.cookingTime(ticks: Int)`関数を用います
また、第三引数がXP、第四引数が調理時間となっているため、そこで設定しても良いでしょう。

引数の説明
1. 出力アイテム(max: 64)
2. 入力アイテム(max: 1)
3. 経験値量
4. 調理時間: Tickであるため`秒数x20`にすると良い
```js
//土を1つのネザースターにするかまどレシピ
event.smelting("nether_star", "dirt")

//鉄を5つのネザライトナゲットにする溶鉱炉レシピ
event.blasting("5x netherite_nugget", "iron_ingot")

//生の牛肉を2つのステーキにする燻製レシピ: 1.2XP
event.smoking("2x steak", "raw_beef").xp(1.2)

//棒を4つの松明にするキャンプファイアレシピ: 2.0XP, 調理時間20秒
event.campfireCooking("4x torch", "stick", 2.0, 400)
```

## 鍛冶台レシピ
鍛冶台のレシピは1.19.2から鍛冶型が追加されたため変更されています。
### Tabs {.tabset}
#### 1.19.2+
```js
event.smithing(
  "netherite_ingot",                      //引数1: 出力するアイテム
  "netherite_upgrade_smithing_template",  //引数2: テンプレート
  "iron_ingot",                           //引数3: アプグレアイテム
  "black_dye"                             //引数4: アプグレ素材
)
```
#### 1.18.2
```js
event.smithing(
  "netherite_ingot",  //引数1: 出力するアイテム
  "iron_ingot",       //引数2: アプグレアイテム
  "black_dye"         //引数3: アプグレ素材
)
```
## 石切台レシピ
`event.stonecutting()`で登録できます。

引数の説明
1. 出力アイテム(max: 64)
2. 入力アイテム(max: 1)
```js
// オークの板材をオークの板材のハーフブロック2個にするレシピ
event.stonecutting(
  "2x oak_slab",
  "oak_planks"
)
```
## カスタムレシピ
`event.custom()`を使用して、データパック/JSONの形式でレシピを登録できます。

引数の説明
1. データパック/JSON形式でのレシピ
```js
//mekanismの粉砕機でレンガブロックを粉砕してレンガ4つを作るレシピ
event.custom({
  "type": "mekanism:crushing",
  "input": {
    "ingredient": {
      "item": "minecraft:bricks"
    }
  },
  "output": {
    "count": 4,
    "item": "minecraft:brick"
  }
})

//mekanismの冶金注入機で基本インダクションセルにレッドストーンを吹き込んでエネルギーを貯めるレシピ
event.custom({
  "type": "mekanism:metallurgic_infusing",
  "chemicalInput": {
    amount: 100,
    "tag": "mekanism:redstone"
  },
  "itemInput": {
    "ingredient": Ingredient.of("mekanism:basic_induction_cell").toJson() //customでは.toJson()を使う
  },
  "output": Item.of('mekanism:basic_induction_cell', '{mekData:{EnergyContainers:[{Container:0b,stored:"8000000000"}]}}').toJson()
})
```
# フィルタリング
レシピを選択するための様々なフィルターが有ります。
これより下では、フィルターが仕様な箇所では`filter`と表記します。

- `{output: "item_id"}`: このアイテムを作成できるレシピ
- `{input: "item_id"}`: このアイテム使用するレシピ
- `{mod: "mod_id"}` : ModIDによる指定
- `{id: "recipe_id"}` : レシピIDによる指定
- `{type: "recipe_type"}` : レシピタイプによる指定
---
また、フィルター同士は論理演算のように組み合わせ可能です。
- AND: `{filter1: "value", filter2: "value"}`
- OR: `[{filter1: "value"}, {filter2: "value"}]`
- NOT: `{not: {filter1: "value"}}`

## レシピの消去
レシピの消去は`event.remove(filter)`で行えます。
引数の説明
1. オブジェクト形式のレシピフィルター

```js
//オブジェクト内に何も記述しなければ核ガンジーの様に全てのレシピを消し去ります
event.remove({}) //Nuke option

//ダイヤピッケルを作るレシピを削除します
event.remove({output: "minecraft:diamond_pickaxe"})

//"wool"タグが付いている全てのレシピを消去します
event.remove({output: "#minecraft:wool"})

//丸石を必要とする全てのレシピを消去します
event.remove({input: "cobblestone"})

//Mekanismからのレシピをすべて消します
event.remove({mod: "mekanism"})

//かまどレシピを全て消します
event.remove({type: "smelting"})
```

## レシピの編集
レシピの編集は、
入力アイテムを変更する場合は`event.replaceInput()`
出力アイテムを変更する場合は`event.replaceOutput()`
で行うことができます。

引数の説明
1. オブジェクト形式のレシピフィルター
2. 変更するアイテム/タグ
3. 変更先のアイテム/タグ

注：タグを使用できるのは入力のみ
```js
//全てのレシピの入力に含まれる棒をブレイズロッドにします
event.replaceInput({}, "stick", "blaze_rod")

//かまどのレシピの出力の金塊を金インゴットにします
event.replaceOutput({type: "smelting"}, "gold_nugget", "gold_ingot")

```
# 応用編
## ヘルパー関数
決まった形式のレシピを複数登録するときに、
そのレシピを登録する関数を定義することで簡単に登録できます。
```js
let multiSmelt = (output, input, includeBlasting) => {
  event.smelting(output, input)
  
  if (includeBlasting) {
    event.blasting(output, input)
  }
}

multiSmelt('minecraft:blue_dye', '#forge:gems/lapis', true)
multiSmelt('minecraft:black_dye', 'minecraft:ink_sac', true)
multiSmelt('minecraft:white_dye', 'minecraft:bone_meal', false)
```
## forEach