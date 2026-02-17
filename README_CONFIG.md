# 博客配置說明

## 已完成的配置

我已經根據 https://haer0248.me/blog/ 的風格配置了你的博客，包括：

✅ 側邊欄個人資訊卡片
✅ 社交媒體連結
✅ 文章列表布局
✅ 分類和標籤頁面
✅ 關於頁面
✅ 自定義 CSS 樣式
✅ 頁腳版權資訊

## 需要你手動修改的部分

### 1. 更新個人資訊

打開 `_config.butterfly.yml`，找到以下部分並修改：

```yaml
# 社交媒體連結
social:
  fab fa-github: https://github.com/你的帳號 || GitHub || '#24292e'
  fab fa-discord: https://discord.gg/你的Discord || Discord || '#5865F2'
  fab fa-twitter: https://twitter.com/你的帳號 || Twitter || '#1DA1F2'
  fab fa-instagram: https://instagram.com/你的帳號 || Instagram || '#E4405F'
  fas fa-envelope: mailto:你的郵箱 || E-Mail || '#4a7dbe'
```

### 2. 更新頭像

```yaml
avatar:
  img: https://i.imgur.com/your_avatar.jpg # 換成你的頭像網址
```

### 3. 更新側邊欄描述

```yaml
card_author:
  enable: true
  description: 現在是一隻正在家裡工作的貓，興趣和專長大概就是打開 VSCode 亂寫東西。
  button:
    enable: true
    icon: fab fa-github
    text: 關注我
    link: https://github.com/你的帳號
```

### 4. 更新公告內容

```yaml
card_announcement:
  enable: true
  content: 正在開發 MyGO 梗圖搜尋器與網頁遊戲中...
```

### 5. 更新關於頁面

編輯 `source/about/index.md`，修改你的個人資訊。

## 如何預覽

在終端執行：

```bash
cd d:\Coding\Hexo\my-blog
hexo clean
hexo generate
hexo server
```

然後在瀏覽器打開 http://localhost:4000 查看效果。

## 主要特色功能

### 參考網站的風格特點

1. **簡潔的導航欄** - 固定在頂部，包含首頁、歸檔、分類、標籤、關於等頁面
2. **個人資訊卡片** - 在側邊欄顯示頭像、描述和社交媒體連結
3. **文章列表** - 清晰的文章卡片布局，顯示日期和分類
4. **友好的頁腳** - 包含版權資訊和特色文字
5. **深色模式支持** - 可切換淺色/深色主題

### 自定義樣式特點

- 卡片懸停動畫效果
- 優化的文章排版
- 美化的滾動條
- 響應式設計（支援行動裝置）

## 如何發布新文章

```bash
hexo new post "文章標題"
```

然後編輯生成的 markdown 檔案，在 Front Matter 中添加分類和標籤：

```yaml
---
title: 文章標題
date: 2025-02-11 12:00:00
categories:
  - 分類名稱
tags:
  - 標籤1
  - 標籤2
---
```

## 部署到 GitHub Pages

1. 安裝部署插件：
```bash
npm install hexo-deployer-git --save
```

2. 在 `_config.yml` 中配置：
```yaml
deploy:
  type: git
  repo: https://github.com/你的帳號/你的帳號.github.io.git
  branch: main
```

3. 部署：
```bash
hexo clean
hexo deploy
```

## 需要幫助？

- Hexo 官方文檔：https://hexo.io/zh-tw/docs/
- Butterfly 主題文檔：https://butterfly.js.org/

---

喵，祝你使用愉快！/ᐠ .ᆺ. ᐟ\ノ
