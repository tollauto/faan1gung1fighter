# 返工 Fighter｜巴仔 VS 鐵路仔

一個單檔案、純前端嘅復古格鬥小遊戲：搭巴士定搭鐵返工，打過先知。
致敬九十年代街機畫風，384×216 低解像 bitmap，放大到全屏都係粒粒 pixel。

**成個遊戲得一個 `index.html`，唔使裝任何嘢，開瀏覽器就玩得。**

---

## 點玩

| 場景 | 內容 |
|---|---|
| 開始畫面 | 「返工 FIGHTER」標題，揀 ONE PLAYER（打 CPU）或者 PLAYER 1 VS PLAYER 2 |
| 揀人 | 簡化香港地圖，兩隻角色：巴仔（BUS BOY）／鐵路仔（T-LO CHAI），二人可以揀同一隻（2P 會變色） |
| 載入畫面 | 5 秒 VS 畫面 |
| 對戰 | 三戰兩勝，每回合 99 秒，時間到鬥血厚。背景每場隨機四選一：電車街／九十年代地鐵月台（旺角）／屯門巴士總站／炮台山站（綠牆＋電視台街訪場景） |
| 結局 | 顯示邊個畀人 K.O.，ENTER 再嚟一鋪 |

## 控制

| 動作 | 1P | 2P |
|---|---|---|
| 行 | A / D | ← / → |
| 跳 | W | ↑ |
| 格擋（避招） | S（㩒住） | ↓（㩒住） |
| 拳 | J | , |
| 腳 | K | . |
| 必殺技 | L | / |

**必殺技要爆氣**：畫面下方藍色氣條儲滿（打中人、捱打、時間都會儲）就可以放。

- 巴仔｜**旋風手**：旋轉前衝連打，全螢幕大字「再嘈車都唔撚開！！！」＋嬲嬲面＋「暫停服務 NOT IN SERVICE」大牌
- 鐵路仔｜**波動拳**：射出「OK」氣功波，全螢幕大字「我嘅訴求就係想返工！！！」＋戴眼鏡管理層面＋「返工!」大泡

放必殺嗰陣背景會變暗、爆出光環，大字闊度可達 2/3 畫面，夠晒戲。

## 放上 GitHub Pages（公開網址）

1. 喺 GitHub 開個新 repo（例如 `faan-gung-fighter`），Public
2. 將 `index.html` upload 上去（拖入去個 repo 頁面就得）
3. 入 **Settings → Pages**，Source 揀 **Deploy from a branch**，Branch 揀 `main`、folder 揀 `/ (root)`，撳 Save
4. 等一兩分鐘，網址就會係 `https://<你嘅用戶名>.github.io/faan-gung-fighter/`，直接 share 畀朋友

## 美術同版權說明

- 所有圖像（角色、背景、UI）都係程式即場繪畫嘅**原創 pixel art**，冇用任何官方圖片、商標或字體圖樣；角色身上嘅公司標誌已按需求文件「any company logo can be removed」全部移除，改用純色色塊。
- 需求文件同參考圖入面嘅真人相（包括受訪片段），已改成原創、不指向任何真人嘅 pixel 人物；炮台山站背景嘅電視台標誌一律用紅圈代替，冇用真台徽。
- 標題用 Google Fonts 嘅 Press Start 2P（開源 OFL 授權）；冇網絡時會自動 fallback 去系統字體，遊戲照玩。
- 音效全部用 WebAudio 即場合成，冇任何音訊檔。

## 技術

- 純 HTML5 Canvas + 原生 JavaScript，零依賴、零 build step
- 內部解像度 384×216，nearest-neighbor 放大保持 bitmap 質感，加埋 CRT 掃描線
- 一人模式有簡單 CPU AI（識行近、出招、格擋、放必殺）
