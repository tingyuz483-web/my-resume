# 履歷型 Portfolio 網站 Spec

## 目標
建立一個單頁 `index.html` 的履歷型 portfolio 網站，風格為 Apple Liquid Glass，符合 104 / 1111 人力銀行 2025-2026 年的履歷視覺建議。

網站應該可以直接推到 GitHub Pages，並且手機與桌機版都具有良好呈現。

## 內容區塊（依序）
1. Hero
   - 大頭照圓形
   - 中文名字
   - 一句話職涯定位
   - 求職方向 pills（例如：AI 工程師、FinTech、顧問業、科技業）
2. About 關於我
   - 2-3 段自我介紹文字
   - 右側或下方三個重點：求職方向 / 所在地 / 語言能力
3. Skills 核心技能
   - 按類別分組（例如：程式語言、工具、模型、專案管理）
   - 每組使用 tag 雲設計
4. Education 學歷
   - timeline 樣式呈現學校、科系、年份、重點
5. Experience 經歷
   - timeline 樣式呈現職務、公司、期間
   - 每項包含 1-2 個數字化成果句（如：XX 提升 20%）
6. Awards 競賽獎項
   - 卡片 grid
   - 每張卡片包含獎項名稱、年份、說明及 emoji badge
7. Projects 作品集
   - 卡片 grid
   - 每張卡片包含作品名稱、類型、簡短說明
8. Contact 聯絡
   - 4 顆按鈕：Email / GitHub / LinkedIn / IG

## 導航
- 固定浮動 TOC
- 內容可快速跳到每個區塊
- 手機版為底部或側邊導覽按鈕變形，桌機版為側邊或頂部固定區塊

## 風格要求
- Apple Liquid Glass 風格
  - 玻璃質感卡片、柔和漸層、模糊背景
  - 方角圓潤、空間感明顯
  - 文字清晰、層次分明
- 使用淺色系，搭配柔和亮色點綴
- 適度使用陰影與背景光暈

### Apple Liquid Glass 規格（細節）

- 背景光暈：兩個 radial-gradient 的光暈（由深藍到紫粉），彼此位置有微小差異，並以極慢速做平移或淡入淡出動畫，營造漂浮感。
- 玻璃卡片：每個主要卡片使用半透明白底（建議 rgba(255,255,255,0.82)），搭配 `backdrop-filter: blur(24px);`，並使用 `border: 1px solid rgba(255,255,255,0.35);` 作為邊線。
- 卡片互動（hover）：卡片在 hover 或 focus 時會有柔光浮起效果（輕微 translateY、放大與較亮的外發光），並提高陰影強度以增強層次感。
- Timeline 樣式：使用左側垂直軸線（半透明）與圓點節點，圓點帶有發光（外側霧狀光暈），以強調時間點，同時保持文字可讀性。
- Tag 雲：膠囊狀（border-radius: 999px），背景半透明（如 rgba(255,255,255,0.6)），外側有微弱對比邊框（如 1px rgba(79,125,255,0.14)），在較暗背景上仍保持良好可讀性。
- 文字對比：所有主要文字需維持至少 AA 可讀性，標題使用較深色（例如 #1d2739），副文字使用中性灰（例如 #64748b）。

## 開發限制（再次確認）
- 嚴格只修改 `index.html` 的 `<style>` 區塊來實作上述視覺效果，其他 HTML 結構不得變動。
- 使用純 CSS（含少量 vanilla JS 如需觸發動畫變換），不得使用框架或打包工具。

## 實作注意事項
- 背景動畫應使用 `@keyframes` 與 `transform` 或 `background-position` 的細微變化，避免造成高 CPU 使用或觸發大量 repaint。
- `backdrop-filter` 需要適度的透明度搭配，並提供 fallback 色塊以確保舊瀏覽器上仍可閱讀內容。
- hover 與 focus 狀態皆需提供可供鍵盤操作的視覺回饋（a, button 的 focus-visible 樣式）。

## 響應式
- 桌機：多欄布局、側邊 TOC 或頂部固定
- 平板 / 手機：單欄、卡片堆疊、易點擊按鈕
- 文字、按鈕、卡片大小對手機優化

## 技術限制
- 單一 `index.html`
- CSS 必須內嵌於 `<style>`
- 不使用 React / Vue / 任何打包工具
- 可使用純 HTML/CSS/少量 vanilla JS

## 例子內容
- 使用假資料：王小明
- 求職目標：AI 工程師
- 公司偏好：FinTech / 顧問業 / 科技業

## 交付項目
- `index.html`
- `spec.md`

> 請先確認這份 spec，確認後我再進行開發。