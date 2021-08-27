---
title: "智能合約(Smart contrast)"
date: 2021-08-27T10:48:34+08:00
draft: false
tags: ["麻塔巴巴", "NodeJS", "JavaScript", "Crypto"]
---
**智能合約** 就是一段在區塊鏈上執行的程式碼

當我們將智能合約部署至區塊鏈上後，我們便能依照智能合約上的內容進行交易，常見以 Solidity 撰寫。
<!--more-->
## 特性
+ 由於智能合約是在區塊鏈系統上的，因此金流動向也是完全透明可追蹤的。
+ 智能合約一旦部署至區塊鏈上後便無法修改
+ 可以公開檢視智能合約
+ 如果不相信和你交易的人? 至少你能相信程式碼
## Solidity
+ 具圖靈完備性
+ 和 Javascript 相似
+ **目前並不是個成熟的語言**
	+ 可能每隔幾個月就會有一次重大的更新，(~~線上遊戲484~~)
+ 能夠在以太坊的 EVM(Ethereum Virtual Machine) 上執行。
	+ 透過以太坊 (Ethereum) 的專用貨幣 : 以太幣 (Ether)，提供去中心化的以太虛擬機 (Ethereum Virtual Machine) 來處理點對點合約。
## 開發流程
1. 撰寫
2. 編譯
+ 編譯好的 Solidity 將會被轉換成能夠在 EVM 上執行的 Bytecode，同時也會獲得一份 **ABI**
	```
	ABI (Application Binary Interface)
	==================================
	+ 智能合約的操作說明，在其之上存有該份智能合約的函式宣告、函式名稱
	+ 可以在 ehterscan 上面看到已經被驗證並且公開的智能合約ABI
	```
+ [範例](https://etherscan.io/address/0xdac17f958d2ee523a2206206994597c13d831ec7#code)
+ ![](https://i.imgur.com/gdpO2E0.png)
3. 部署
	部署合約就是普通的一般交易流程，只是會在備註欄裡附錄合約的 Bytecode  
	所以我們也需要等待礦工打包這筆交易，礦工將交易打包至區塊鏈後該合約才能生效  
	確認後會獲得一個合約的地址，就能和合約進行互動
4. 交易

## Solidity開發環境
+ [Remix](http://remix.ethereum.org/)
+ 連接本地端資料夾
	+ [安裝node.js](https://nodejs.org/en/)
	+ 安裝完後打開你的命令提示字元(CMD)
	+ 輸入指令 
		```bash
			npm install -g @remix-project/remixd
		```
	+ 然後執行指令
	+ remixd -s <本地資料夾> --remix-ide <remix 網址>
	+ 例如:
		```bash
		remixd -s C:\Users\user\Desktop\Remix remixd-ide https://nodejs.org/en/
		```
	+ ![](https://i.imgur.com/dyKujXk.png)
	+ ![](https://i.imgur.com/XujLwEA.png)
	+ ![](https://i.imgur.com/oXT4TSr.png)
	+ 這樣就能順利連接到本地端了


                
