# Daily content routine（每日更新流程）

幼稚園日語看圖／數數遊戲：每天固定 **10 題**。

## 今日測驗怎麼組題

1. 優先約 **5 題**今日新詞彙（`DAILY_NEW_BATCHES` 最新一批的 `vocabIds`）
2. 優先約 **2 題**今日新數數（該批 `numberIds`，目前為 9–20 池）
3. 其餘題從**舊詞庫**補齊
4. 盡量避開前 2 天出現過的題（`DAILY_LOOKBACK_DAYS`），減少日復一日重複

實作位置：`index.html` 的 `dailyItemIds` / `DAILY_NEW_BATCHES`。

## 每天要做什麼（維護者）

1. **加約 5 個新詞彙**
   - 在 `ITEMS` 陣列末尾新增條目（顯示、假名、羅馬拼音、中文、例句、答案別名、`photo`）
   - 把清楚的正方形照片放到 `images/<id>.jpg`
2. **加約 2 個新數數（或擴充數數池）**
   - 在 `NUMBER_ITEMS` 新增（`kind: "number"`、`count`、清楚可數的圖）
   - 數數圖建議與現有 `images/count-*.jpg` 同風格（奶油底＋橘框、物件排列清楚）
3. **登記今日批次**（放在 `DAILY_NEW_BATCHES` **最前面**）

```js
{
  date: "YYYY-MM-DD",
  label: "簡短說明",
  vocabIds: ["id1", "id2", "id3", "id4", "id5"],
  numberIds: ["num-…", "num-…"]  // 或一組新數數池
}
```

4. **把 `QUESTION_BANK_VERSION` +1**  
   （未開始的「今日」測驗會自動換成新的 10 題；已作答進度會保留）
5. **提交並推到 `master`**（GitHub Pages 會更新）

```bash
git add -A
git commit -m "Daily quiz YYYY-MM-DD: +5 vocab + numbers …"
git push origin master
```

6. 確認頁面：https://sheng056-pixel.github.io/jp-kindergarten-voice-game/


## 2026-10-07 本批已完成

- 新詞 5 個：`crab` かに／螃蟹、`lemon` レモン／檸檬、`mouse` ねずみ／老鼠、`toothbrush` はブラシ／牙刷、`pumpkin` かぼちゃ／南瓜
- 新數數 2 題：`num-4-stars`（4 顆星）、`num-11-apples`（11 個蘋果）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 10；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-06 本批已完成

- 新詞 5 個：`turtle` かめ／烏龜、`peach` もも／桃子、`glasses` めがね／眼鏡、`house` いえ／房子、`scissors` はさみ／剪刀
- 新數數 2 題：`num-6-stars`（6 顆星）、`num-14-apples`（14 個蘋果）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 9；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-05 本批已完成

- 新詞 5 個：`penguin` ペンギン／企鵝、`tiger` とら／老虎、`icecream` アイス／冰淇淋、`boat` ふね／船、`butterfly` ちょうちょ／蝴蝶
- 新數數 2 題：`num-7-apples`（7 個蘋果）、`num-16-hearts`（16 顆愛心）
- 照片來源：Wikimedia Commons／rawpixel（CC 授權），裁成 800×800
- `QUESTION_BANK_VERSION` → 8；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-04 本批已完成

- 新詞 5 個：`panda` パンダ／熊貓、`giraffe` きりん／長頸鹿、`watermelon` すいか／西瓜、`fork` フォーク／叉子、`window` まど／窗戶
- 新數數 2 題：`num-5-apples`（5 個蘋果）、`num-12-hearts`（12 顆愛心）
- `QUESTION_BANK_VERSION` → 7；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-03 本批已完成

- 新詞 5 個：`lion` らいおん／獅子、`sheep` ひつじ／羊、`cake` ケーキ／蛋糕、`spoon` スプーン／湯匙、`bed` ベッド／床
- 新數數 2 題：`num-3-stars`（3 顆星）、`num-8-flowers`（8 朵花）
- `QUESTION_BANK_VERSION` → 6；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-02 本批已完成

- 數數庫擴充為 **1–20**（清楚 count 圖）
- 新詞 5 個：`monkey` さる、`horse` うま、`bag` かばん、`cookie` クッキー、`cup` コップ
- 今日測驗偏好：5 新詞 + 2 新數數（9–20）+ 舊庫補齊；降低連續日重複
- 首頁收藏、訪客計數、日期導覽、錯題複習等功能維持不變

