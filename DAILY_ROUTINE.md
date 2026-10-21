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


## 2026-10-21 本批已完成

- 新詞 5 個：`hedgehog` ハリネズミ／刺蝟、`pudding` プリン／布丁、`rocket` ロケット／火箭、`cabbage` キャベツ／高麗菜、`randoseru` ランドセル／小學生書包
- 新數數 2 題：`num-14-hearts`（14 顆愛心）、`num-19-apples`（19 個蘋果）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 24；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-20 本批已完成

- 新詞 5 個：`gorilla` ゴリラ／大猩猩、`daikon` だいこん／白蘿蔔、`excavator` ショベルカー／挖土機、`doughnut` ドーナツ／甜甜圈、`towel` タオル／毛巾
- 新數數 2 題：`num-17-apples`（17 個蘋果）、`num-18-stars`（18 顆星）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 23；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-19 本批已完成

- 新詞 5 個：`sweetpotato` さつまいも／地瓜、`momiji` もみじ／楓葉、`ambulance` きゅうきゅうしゃ／救護車、`hamster` ハムスター／倉鼠、`ramen` ラーメン／拉麵
- 新數數 2 題：`num-11-stars`（11 顆星）、`num-15-apples`（15 個蘋果）
- 照片來源：Wikimedia Commons（CC／CC0），裁成 800×800
- `QUESTION_BANK_VERSION` → 22；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-18 本批已完成

- 新詞 5 個：`shark` さめ／鯊魚、`chestnut` くり／栗子、`dragonfly` とんぼ／蜻蜓、`taxi` タクシー／計程車、`mittens` てぶくろ／手套
- 新數數 2 題：`num-13-stars`（13 顆星）、`num-16-apples`（16 個蘋果）
- 照片來源：Wikimedia Commons（CC 授權），處理成 800×800
- `QUESTION_BANK_VERSION` → 21；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-17 本批已完成

- 新詞 5 個：`goat` やぎ／山羊、`persimmon` かき／柿子、`acorn` どんぐり／橡實、`firetruck` しょうぼうしゃ／消防車、`onigiri` おにぎり／飯糰
- 新數數 2 題：`num-14-stars`（14 顆星）、`num-10-hearts`（10 顆愛心）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 20；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-16 本批已完成

- 新詞 5 個：`crocodile` わに／鱷魚、`jellyfish` くらげ／水母、`eggplant` なす／茄子、`eraser` けしゴム／橡皮擦、`sandwich` サンドイッチ／三明治
- 新數數 2 題：`num-4-apples`（4 個蘋果）、`num-12-stars`（12 顆星）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 19；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-15 本批已完成

- 新詞 5 個：`deer` しか／鹿、`pear` なし／梨、`spider` くも／蜘蛛、`chopsticks` はし／筷子、`helicopter` ヘリコプター／直升機
- 新數數 2 題：`num-5-stars`（5 顆星）、`num-7-hearts`（7 顆愛心）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 18；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-14 本批已完成

- 新詞 5 個：`snake` へび／蛇、`ant` あり／螞蟻、`potato` じゃがいも／馬鈴薯、`telephone` でんわ／電話、`crayon` クレヨン／蠟筆
- 新數數 2 題：`num-6-hearts`（6 顆愛心）、`num-8-apples`（8 個蘋果）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 17；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-13 本批已完成

- 新詞 5 個：`dolphin` いるか／海豚、`bee` はち／蜜蜂、`cucumber` きゅうり／小黃瓜、`guitar` ギター／吉他、`swing` ブランコ／盪鞦韆
- 新數數 2 題：`num-3-hearts`（3 顆愛心）、`num-9-stars`（9 顆星）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 16；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-12 本批已完成

- 新詞 5 個：`octopus` たこ／章魚、`whale` くじら／鯨魚、`ladybug` てんとうむし／瓢蟲、`onion` たまねぎ／洋蔥、`slide` すべりだい／溜滑梯
- 新數數 2 題：`num-1-star`（1 顆星）、`num-2-apples`（2 個蘋果）
- 照片來源：Wikimedia Commons（CC 授權），裁成 800×800
- `QUESTION_BANK_VERSION` → 15；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-11 本批已完成

- 新詞 5 個：`zebra` しまうま／斑馬、`chicken` にわとり／雞、`pineapple` パイナップル／鳳梨、`balloon` ふうせん／氣球、`camera` カメラ／相機
- 新數數 2 題：`num-19-stars`（19 顆星）、`num-20-apples`（20 個蘋果）
- 照片來源：Wikimedia Commons（CC／公有領域），裁成 800×800
- `QUESTION_BANK_VERSION` → 14；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-10 本批已完成

- 新詞 5 個：`hippo` かば／河馬、`kangaroo` カンガルー／袋鼠、`broccoli` ブロッコリー／綠花椰菜、`key` かぎ／鑰匙、`taiko` たいこ／鼓
- 新數數 2 題：`num-17-hearts`（17 顆愛心）、`num-18-apples`（18 個蘋果）
- 照片來源：Wikimedia Commons（CC 授權），裁成 800×800
- `QUESTION_BANK_VERSION` → 13；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-09 本批已完成

- 新詞 5 個：`fox` きつね／狐狸、`squirrel` りす／松鼠、`mushroom` きのこ／蘑菇、`cherry` さくらんぼ／櫻桃、`piano` ピアノ／鋼琴
- 新數數 2 題：`num-10-apples`（10 個蘋果）、`num-15-stars`（15 顆星）
- 照片來源：Wikimedia Commons（CC 授權），裁成 800×800
- `QUESTION_BANK_VERSION` → 12；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

## 2026-10-08 本批已完成

- 新詞 5 個：`snail` かたつむり／蝸牛、`owl` ふくろう／貓頭鷹、`corn` とうもろこし／玉米、`socks` くつした／襪子、`koala` コアラ／無尾熊
- 新數數 2 題：`num-9-apples`（9 個蘋果）、`num-13-hearts`（13 顆愛心）
- 照片來源：Wikimedia Commons（CC 授權），裁成 800×800
- `QUESTION_BANK_VERSION` → 11；`DAILY_NEW_BATCHES` 已登記今日批次（newest first）

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

