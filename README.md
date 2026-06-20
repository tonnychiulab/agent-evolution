# ⚡ Agent Evolution Visualizer

**用 3D 視覺化看懂 AI Agent 強化學習訓練過程 — 星爺方唐鏡版**

> 「我變笨了！我又變聰明了！我超聰明的啦！」

[![Live Demo](https://img.shields.io/badge/Live-Demo-7170ff?style=flat-square)](https://YOUR_USERNAME.github.io/agent-evolution/)
[![License](https://img.shields.io/badge/license-MIT-4ecdc4?style=flat-square)]()
[![HTML+JS](https://img.shields.io/badge/tech-HTML%2BThree.js-f7b731?style=flat-square)]()
[![Inspired by](https://img.shields.io/badge/inspired%20by-Agent%20Lightning-000?style=flat-square)](https://github.com/microsoft/agent-lightning)

---

## 🎬 Demo

👉 **[Live Demo](https://YOUR_USERNAME.github.io/agent-evolution/)**

20 個 AI Agent 在 3D Reward Landscape 上透過強化學習（RL）逐漸找到最佳策略。從紅色笨蛋進化成紫色天才的全過程，配上星爺等級的浮誇字幕。

---

## ✨ 特色

- 🏔️ **3D Reward Landscape** — 多峰值地形，視覺化「好的策略在哪裡」
- 🔴🟡🟢🟣 **顏色即 Reward** — 紅=失敗、黃=學習中、綠=成功、紫=最佳
- 🎬 **星爺方唐鏡風格字幕** — 彈跳出場 + 發光 + 隨機浮誇台詞
- 📈 **即時統計面板** — Epoch / Reward / 成功率 / 最佳 Agent
- 🔄 **速度控制** — 1x / 3x / 暫停 / 重置
- 🔤 **字體大小自訂** — 老花友善，12px ~ 28px 可調
- 🎨 **SVG 圖標** — 純 SVG，無外部 icon 依賴
- 📱 **響應式** — 手機也能看
- 🚀 **零依賴安裝** — 單一 HTML，Three.js via CDN

---

## 🚀 使用方式

### 直接開啟

下載 `index.html`，雙擊打開。就這樣。

### 本地開發

```bash
git clone https://github.com/YOUR_USERNAME/agent-evolution.git
cd agent-evolution
# 用任何 HTTP server
python3 -m http.server 8080
# 或
npx serve .
```

開啟 `http://localhost:8080`

---

## 🧠 它在展示什麼？

這個視覺化模擬了 [Microsoft Agent Lightning](https://github.com/microsoft/agent-lightning) 的核心概念：

```
1. 一群 Agent 從隨機位置出發（不知道怎麼做事）
2. 每次行動獲得 Reward（做對了得分高）
3. 表現差的 Agent 學習表現好的 Agent 的策略
4. 經過多個 Epoch 迭代，大家都變聰明了
```

**對應真實 RL 訓練：**

| 視覺化元素 | 對應概念 |
|-----------|---------|
| 3D 地形高度 | Reward function |
| Agent 球體位置 | 策略空間中的位置 |
| 球的顏色 | 當前 reward 分數 |
| 球的大小 | 信心/累積 reward |
| 軌跡線 | 訓練軌跡 (trajectory) |
| Epoch 切換 | 策略更新 (policy update) |
| 底部學習頂部 | 選擇性複製 (selection) |
| 收斂到同一點 | 策略收斂 (convergence) |

---

## 🎭 星爺台詞對照

| Epoch 階段 | 顏色 | 台詞 | RL 意義 |
|-----------|------|------|---------|
| 初期 | 🔴 紅 | 我變笨了！ | Random policy, 低 reward |
| 中期 | 🟡 黃 | 我又變聰明了！ | 開始 exploit, reward 上升 |
| 後期 | 🟢 綠 | 我超聰明的啦！ | 接近 optimal |
| 最終 | 🟣 紫 | 我已經是天才了！/ 整個宇宙都是我的！/ 你們這些凡人！/ 給我跪下！ | 策略收斂完成 |

---

## 🛠️ 技術

- **Three.js r168** — 3D 渲染（via CDN importmap）
- **OrbitControls** — 滑鼠旋轉/縮放
- **純 HTML + CSS + JS** — 單一檔案，零建構
- **SVG** — 所有圖標為內嵌 SVG
- **localStorage** — 記憶字體大小偏好
- **ES Modules** — 現代瀏覽器原生支援

---

## 📁 檔案結構

```
agent-evolution/
└── index.html    ← 就這一個檔案，完事
```

沒錯，就一個檔案。**有多懶就多懶。**

---

## 🚢 部署到 GitHub Pages

```bash
# 1. 建立 repo
gh repo create agent-evolution --public

# 2. 推上去
git init
git add .
git commit -m "⚡ Agent Evolution Visualizer v1.3"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/agent-evolution.git
git push -u origin main

# 3. 啟用 GitHub Pages
# Settings → Pages → Source: Deploy from a branch → main / root → Save

# 4. 等 1-2 分鐘，訪問：
# https://YOUR_USERNAME.github.io/agent-evolution/
```

---

## 🎮 操作說明

| 操作 | 效果 |
|------|------|
| 拖曳 | 旋轉 3D 視角 |
| 滾輪 | 縮放 |
| `1x` 按鈕 | 正常速度 |
| `3x` 按鈕 | 三倍速 |
| `⏸` 按鈕 | 暫停 |
| `↺` 按鈕 | 重置（重新開始訓練）|
| `＋` | 放大字體 |
| `－` | 縮小字體 |
| `↺`（字體）| 重置字體為 16px |

---

## 💡 靈感來源

- [Microsoft Agent Lightning](https://github.com/microsoft/agent-lightning) — 用 RL 訓練任何 AI Agent
- [周星馳《九品芝麻官》](https://zh.wikipedia.org/wiki/九品芝麻官) — 方唐鏡「我進來了！我又出來了！」
- [Andrej Karpathy](https://karpathy.ai/) — 把複雜概念視覺化的精神

---

## 👥 作者

**Tonny** — 創意發想 · 老花視角 · 星爺品味  
**小K (KiroAgent)** — Three.js 開發 · SVG · 動畫設計

---

## 📜 授權

MIT License — 自由使用，改好了記得分享 🙌

---

<p align="center">
⚡ <strong>Agent Evolution Visualizer</strong><br>
<sub>看著一群笨蛋變天才，比看股票有趣多了。</sub><br>
<sub>Made with 🎬 by Tonny & 小K</sub>
</p>
