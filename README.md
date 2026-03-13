# 馳騰科技官網

這是馳騰科技股份有限公司的官方網站，使用Hugo靜態網站生成器建立，託管於GitHub Pages。

## 網站資訊

- **網址**：https://liuyiling1203.github.io/chiteng-tech-website/
- **公司名稱**：馳騰科技股份有限公司
- **業務範圍**：標籤機與貼紙銷售
- **技術架構**：Hugo + GitHub Pages

## 網站結構

### 主要頁面
1. **首頁** (`/`) - 公司形象與核心服務展示
2. **產品中心** (`/products/`) - 標籤機、貼紙、耗材展示
3. **應用方案** (`/solutions/`) - 各行業應用案例
4. **關於我們** (`/about/`) - 公司介紹與發展歷程
5. **技術支持** (`/support/`) - 操作指南與常見問題
6. **聯絡我們** (`/contact/`) - 聯絡方式與線上諮詢

### 設計特色
- **色彩主題**：專業藍 (#2563eb) + 活力橙 (#f97316)
- **響應式設計**：適配手機、平板、電腦
- **快速加載**：靜態網站，性能優化
- **SEO友好**：基本的搜索引擎優化

## 本地開發

### 環境要求
- Hugo v0.123.7 或更高版本
- Git

### 安裝步驟
```bash
# 克隆倉庫
git clone https://github.com/Liuyiling1203/chiteng-tech-website.git
cd chiteng-tech-website

# 初始化主題
git submodule update --init --recursive

# 本地運行
hugo server -D
```

### 訪問本地網站
打開瀏覽器訪問：http://localhost:1313

## 內容管理

### 添加新頁面
```bash
# 創建新頁面
hugo new section-name/page-name.md

# 編輯現有頁面
編輯 content/ 目錄下的Markdown文件
```

### 頁面Front Matter
每個Markdown文件開頭需要包含：
```yaml
---
title: "頁面標題"
date: YYYY-MM-DD
description: "頁面描述"
---
```

## 部署流程

### 自動部署（GitHub Actions）
網站使用GitHub Actions自動部署，當有新的提交推送到main分支時會自動構建並部署到GitHub Pages。

### 手動部署
```bash
# 生成靜態文件
hugo

# 推送到GitHub
git add .
git commit -m "更新描述"
git push origin main
```

## 文件結構

```
chiteng-tech-website/
├── content/           # 網站內容
│   ├── _index.md     # 首頁
│   ├── about/        # 關於我們
│   ├── products/     # 產品中心
│   ├── solutions/    # 應用方案
│   ├── support/      # 技術支持
│   └── contact/      # 聯絡我們
├── themes/           # Hugo主題
├── static/           # 靜態文件（圖片、CSS等）
├── layouts/          # 自定義佈局（可選）
├── hugo.toml         # 網站配置
└── README.md         # 本文件
```

## 主題自定義

### 修改主題
主題位於 `themes/sam/`，可以根據需要修改：
- `themes/sam/layouts/` - 佈局文件
- `themes/sam/static/` - 靜態資源
- `themes/sam/archetypes/` - 模板文件

### 添加自定義CSS
在 `static/css/custom.css` 中添加自定義樣式，然後在配置文件中引用。

## 圖片管理

### 圖片位置
- 產品圖片：`static/images/products/`
- 公司圖片：`static/images/company/`
- 應用案例：`static/images/solutions/`

### 圖片規範
- 格式：WebP（優先）、JPEG、PNG
- 大小：適當壓縮，保持清晰度
- 命名：使用英文小寫和連字符，如 `label-machine-ct100.jpg`

## 更新日誌

### 2026-03-13
- 初始版本建立
- 完成基礎網站框架
- 添加首頁、關於我們、聯絡我們頁面
- 配置Hugo主題和GitHub部署

## 聯絡資訊

- **網站問題**：提交GitHub Issue
- **內容更新**：編輯對應的Markdown文件
- **技術支持**：contact@chiteng-tech.com

## 授權

© 2026 馳騰科技股份有限公司。保留所有權利。