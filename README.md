# 出行即時到站（My Transit）

個人日常出行用的即時到站查詢，純前端單頁應用，直接呼叫香港政府「資料一線通」公開 API，顯示港鐵與城巴的實時到站時間。

## 功能

- 兩個分頁：**學校** 與 **關口**
- 港鐵：坑口站（北角方向）、大圍站（金鐘方向）、大學站（金鐘方向），各顯示接下來 **3 班**
- 校巴：大學／大圍開出的固定時間表，自動計算接下來 **3 班**與剩餘倒數分鐘
- 城巴：B8／798 指定站點，各顯示接下來 **3 班**實時到站
- 每 **60 秒**自動刷新、每 **15 秒**本地重算倒數、手動刷新按鈕、Loading 與錯誤提示
- 行動優先（Mobile-first）響應式設計，使用 Tailwind CSS（CDN）

## 啟用 GitHub Pages

1. 開啟本 repo 的 **Settings → Pages**
2. **Source** 選 **Deploy from a branch**
3. Branch 選 **`main`**、路徑 **`/ (root)`**，點 **Save**
4. 約 1 分鐘後，訪問：<https://chenjiajinhk.github.io/my-transit/>

## 數據來源

- 港鐵列車到站時間 API：`https://rt.data.gov.hk/v1/transport/mtr/getSchedule.php`
- 城巴實時到站 API：`https://rt.data.gov.hk/v2/transport/citybus/eta/CTB/{stop}/{route}`

全部為真實公開 API，**無任何模擬（Mock）數據**。
