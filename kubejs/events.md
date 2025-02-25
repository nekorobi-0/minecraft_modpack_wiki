---
title: イベント
description: 
published: false
date: 2025-02-25T12:59:15.922Z
tags: kubejs
editor: markdown
dateCreated: 2025-02-23T13:58:52.927Z
---

# イベント
イベントとは様々な動作が行われる際に発火される(呼び出される)もので、
例として、	レシピの改変時、アイテムの登録時などに使われます。
# イベントリスト
## BlockEvents
### BlockEvents.broken
`server_scripts`または`client_scripts`
### BlockEvents.detectorChanged
`server_scripts`または`client_scripts`
### BlockEvents.detectorPowered
`server_scripts`または`client_scripts`
### BlockEvents.detectorUnpowered
`server_scripts`または`client_scripts`
### BlockEvents.farmlandTrampled
`server_scripts`または`client_scripts`
### BlockEvents.leftClicked
`server_scripts`または`client_scripts`
### BlockEvents.modification
`startup_scripts`
### BlockEvents.placed
`server_scripts`または`client_scripts`
### BlockEvents.rightClicked
`server_scripts`または`client_scripts`
## ClientEvents
### ClientEvents.highPriorityAssets
`client_scripts`
### ClientEvents.init
`startup_scripts`
### ClientEvents.lang
`client_scripts`
### ClientEvents.leftDebugInfo
`client_scripts`
### ClientEvents.loggedin
`client_scripts`
### ClientEvents.loggedout
`client_scripts`
### ClientEvents.painterUpdated
`client_scripts`
### ClientEvents.paintScreen
`client_scripts`
### ClientEvents.rightDebugInfo
`client_scripts`
### ClientEvents.tick
`client_scripts`
## EntityEvents
### EntityEvents.checkSpawn
`server_scripts`
### EntityEvents.death
`server_scripts`
### EntityEvents.hurt
`server_scripts`
### EntityEvents.spawned
`server_scripts`
## ItemEvents
### ItemEvents.armorTierRegistry
`sratrup_scripts`
### ItemEvents.canPickUp
`server_scripts`または`client_scripts`
### ItemEvents.crafted
`server_scripts`または`client_scripts`
### ItemEvents.dropped
`server_scripts`または`client_scripts`
### ItemEvents.dynamicTooltips
`client_scripts`
### ItemEvents.entityInteracted
`server_scripts`または`client_scripts`
### ItemEvents.firstLeftClicked
`server_scripts`または`client_scripts`
### ItemEvents.firstRightClicked
`server_scripts`または`client_scripts`
### ItemEvents.foodEaten
`server_scripts`または`client_scripts`
### ItemEvents.modelProperties
`startup_scripts`
### ItemEvents.modification
`startup_scripts`
### ItemEvents.modifyTooltips
`server_scripts`または`client_scripts`
### ItemEvents.pickedUp
`server_scripts`または`client_scripts`
### ItemEvents.rightClicked
`server_scripts`または`client_scripts`
### ItemEvents.smelted
`server_scripts`または`client_scripts`
### ItemEvents.toolTierRegistry
`server_scripts`または`client_scripts`
## LevelEvents
### LevelEvents.afterExplosion
`server_scripts`
### LevelEvents.beforeExplosion
`server_scripts`
### LevelEvents.loaded
`server_scripts`
### LevelEvents.tick
`server_scripts`
### LevelEvents.unloaded
`server_scripts`
## NetworkEvents
### NetworkEvents.dataReceived
`server_scripts`または`client_scripts`
## PlayerEvents
### PlayerEvents.advancement
`server_scripts`
### PlayerEvents.chat
`server_scripts`
### PlayerEvents.chestClosed
`server_scripts`
### PlayerEvents.chestOpened
`server_scripts`
### PlayerEvents.decorateChat
`server_scripts`
### PlayerEvents.inventoryChanged
`server_scripts`
### PlayerEvents.inventoryClosed
`server_scripts`
### PlayerEvents.inventoryOpened
`server_scripts`
### PlayerEvents.loggedIn
`server_scripts`
### PlayerEvents.loggedOut
`server_scripts`
### PlayerEvents.respawned
`server_scripts`
### PlayerEvents.tick
`server_scripts`
## RecipeViewerEvents
### RecipeViewerEvents.addEntries
`server_scripts`または`client_scripts`
### RecipeViewerEvents.addInformation
`server_scripts`または`client_scripts`
### RecipeViewerEvents.groupEntries
`server_scripts`または`client_scripts`
### RecipeViewerEvents.registerSubtypes
`server_scripts`または`client_scripts`
### RecipeViewerEvents.removeCategories
`server_scripts`または`client_scripts`
### RecipeViewerEvents.removeEntries
`server_scripts`または`client_scripts`
### RecipeViewerEvents.removeEntriesCompletely
`server_scripts`または`client_scripts`
### RecipeViewerEvents.removeRecipes
`server_scripts`または`client_scripts`
## SeverEvents
### ServerEvents.afterRecipes
`server_scripts`
### ServerEvents.basicCommand
`server_scripts`
### ServerEvents.command
`server_scripts`
### ServerEvents.commandRegistry
`server_scripts`
### ServerEvents.compostableRecipes
`server_scripts`
### ServerEvents.generateData
`server_scripts`
### ServerEvents.loaded
`server_scripts`
### [ServerEvents.recipes](/kubejs/editingRecipe)
`server_scripts`
レシピの改変/追加時に使用します
### ServerEvents.recipeTypeRegistry
`server_scripts`
### ServerEvents.specialRecipeSerializers
`server_scripts`
### ServerEvents.tags
`server_scripts`
### ServerEvents.tick
`server_scripts`
### ServerEvents.unloaded
`server_scripts`
## StartupEvets
### StartupEvets.init
`sratrup_scripts`
### StartupEvets.modifyCreativeTab
`sratrup_scripts`
### StartupEvets.postInit
`sratrup_scripts`
### StartupEvets.registry
`sratrup_scripts`
アイテムやブロックの登録時に使用します。