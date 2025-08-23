---
navigation:
  title: 複製
  icon: replication:replicator
item_ids:
  - replication:replicator
  - replication:matter_network_pipe
  - replication:identification_chamber
  - replication:disintegrator
  - replication:matter_tank
  - replication:replication_terminal
  - replication:chip_storage
---

# 複製

**複製** 是一個科技模組，允許你複製相似種類的資源。你可以將泥土轉換為石頭，但無法將泥土轉換成鑽石。

## 重要概念

**物質管線** 可讓你連接複製機器，並自動化部分流程：

* 傳輸 **能量**：運作方式類似於任何能量管線
* 傳輸 **物質**：會將物質從 **解體機** 傳送到 **物質儲罐**，並從 **物質儲罐** 傳送到需要物質的其他機器

**識別艙** 將掃描物品以獲取其物質值，並將這些數值儲存到晶片中。這些 **晶片** 可以存放在 **晶片儲存裝置** 中，並供整個網路使用。

**複製器** 可在「無限模式」下運作，在此模式下，它們會持續複製資源，直到資源欄滿或物質耗盡，你可以在使用者介面中設定此模式。

## 運作方式

要轉換物品，你需要使用 **解體機** 將其分解成原始數值。利用該機器，你可以將任何具有物質值的物品轉換為物質。一旦你掃描了一些物品並將其數值儲存到晶片中，就可以使用 **複製終端機** 請求物品。有了請求後，**複製器** 將利用儲罐中的物質從頭開始複製該物品，然後將其傳送回終端機。

<GameScene zoom="4" interactive={true}>
  <ImportStructure src="setup.snbt" />
  <IsometricCamera yaw="30" pitch="30" />
</GameScene>

## 物質百科

**物質百科** 是一個可搜尋的清單，讓你查詢哪些物品擁有特定的物質值。你可以透過複製終端機畫面中搜尋列左側的按鈕進入，也可以點擊終端機右側的物質顯示區進入。

在物質百科的搜尋列中，你可以使用：

* 任何物質名稱：將顯示所有擁有該物質的物品
* `earth>10` 將顯示所有擁有超過 10 個 earth 的物品
* `nether=20` 將顯示所有擁有恰好 20 個 nether 的物品
* `quantum<6` 將顯示所有擁有少於 6 個 quantum 的物品
* `!earth` 將顯示所有不含 earth 的物品
* `*metallic` 將顯示所有僅包含 metallic 的物品
