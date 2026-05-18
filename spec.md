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