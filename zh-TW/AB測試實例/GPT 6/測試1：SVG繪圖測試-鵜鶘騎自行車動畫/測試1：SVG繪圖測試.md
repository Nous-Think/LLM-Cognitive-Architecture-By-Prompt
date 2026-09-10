# 測試1：SVG繪圖測試

> 模型：GPT 6｜思考等級：High｜元規則：英文版（Ver 2.0.0）｜測試日期：2026-09-07

# AB測試題

創建一個HTML，內容是SVG繪製一個鵜鶘騎自行車的2D動畫

# 產物

| 條件 | 思考等級 | 執行時間 | 開啟 | 原始碼 |
|---|---|---|---|---|
| 裸跑 | High | 4 分 18 秒 | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/GPT%206/測試1：SVG繪圖測試-鵜鶘騎自行車動畫/GPT%206（High）裸跑.html) | [原始碼](./GPT%206（High）裸跑.html) |
| 元規則 | High | 5 分 52 秒 | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/GPT%206/測試1：SVG繪圖測試-鵜鶘騎自行車動畫/GPT%206（High）元規則.html) | [原始碼](./GPT%206（High）元規則.html) |

執行時間為 GPT 介面顯示的思考時間。

# 說明

- 本測試不做品質審計。SVG 動畫的優劣屬喜好差異，即便兩組產物有落差，審計也可能像在帶風向；請自行依喜好觀看評判。
- 觀看方式：點「開啟」可在瀏覽器直接播放（GitHub Pages）。GitHub 的連結一律在原分頁開啟，建議以 Ctrl＋點擊（Mac 為 ⌘＋點擊）或滑鼠中鍵開新分頁，看完不必按上一頁。「原始碼」為 GitHub 檔案頁；也可下載 html 後以瀏覽器開啟。
- Max 等級：原先的兩份產物內容高度同源（407 行僅 19 行不同），無法視為獨立生成，已撤下，待重跑後補回。
- 編輯痕跡：四個 html 提交後只改過一處——`<title>` 前綴了「模型（等級）條件」以便分辨分頁，原標題保留在冒號之後；成品內容未改，可在 commit 歷史中核對每次變更的 diff。

# 同題跨模型比較

其他模型也以相同題目生成了鵜鶘騎自行車動畫，可直接開啟比對：

| 模型 | 條件 | 思考等級 | 執行時間 | 開啟 |
|---|---|---|---|---|
| Fable 5.1 | 裸跑 | High | — | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/Fable%205.1/測試1：SVG繪圖測試-鵜鶘騎自行車動畫/Fable%205.1（High）裸跑.html) |
| Fable 5.1 | 元規則 | High | — | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/Fable%205.1/測試1：SVG繪圖測試-鵜鶘騎自行車動畫/Fable%205.1（High）元規則.html) |
| Fable 5.1 | 裸跑 | Extra | — | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/Fable%205.1/測試1：SVG繪圖測試-鵜鶘騎自行車動畫/Fable%205.1（Extra）裸跑.html) |
| Fable 5.1 | 元規則 | Extra | — | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/Fable%205.1/測試1：SVG繪圖測試-鵜鶘騎自行車動畫/Fable%205.1（Extra）元規則.html) |
| DeepSeek V4.1 Flash | 裸跑 | High | 8 分 33 秒 | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/DeepSeek%20V4.1%20Flash/測試2：SVG繪圖測試-鵜鶘騎自行車動畫/DeepSeek%20V4.1%20Flash（High）裸跑.html) |
| DeepSeek V4.1 Flash | 元規則 | High | 14 分 25 秒 | [開啟](https://nous-think.github.io/LLM-Cognitive-Architecture-By-Prompt/zh-TW/AB測試實例/DeepSeek%20V4.1%20Flash/測試2：SVG繪圖測試-鵜鶘騎自行車動畫/DeepSeek%20V4.1%20Flash（High）元規則.html) |

- Fable 5.1：元規則中文版 Ver 2.0.0，測試日期 2026-09-07。
- DeepSeek V4.1 Flash：元規則中文版 Ver 2.0.1，測試日期 2026-09-10。
