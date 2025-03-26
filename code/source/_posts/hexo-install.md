---
title: hexo-install
date: 2025-03-26 12:49:13
tags: 
    - hexo
    - 開源軟體
categories: hexo

description: Hexo 是一款基於 Node.js 的開源部落格框架，使用 Markdown 語言來解析文章，內建很多不同的主題 ，跟內建許多現成的套件可以直接使用。
---

# Hexo 安裝教學

發表於 2024-05-18｜更新於 2024-05-20｜分類：Hexo

## 1. 什麼是 Hexo

Hexo 是一款基於 Node.js 的開源部落格框架，使用 Markdown 語言來解析文章，內建多種主題與套件可使用，能快速產生靜態網站。

---

## 2. 安裝 Hexo

安裝 Hexo 前請先準備以下工具：

- [Node.js](https://nodejs.org)
- [Git](https://git-scm.com)
- VS Code 或其他編輯器（依個人習慣）

### 2.1 安裝 Hexo CLI

```bash
npm install -g hexo-cli
```

### 2.2 初始化 Hexo 專案

```bash
hexo init <資料夾名稱>
cd <資料夾名稱>
npm install
```

### 2.3 啟動本地伺服器

```bash
hexo server
```

預設網站會出現在 `http://localhost:4000/`

---

## 3. Hexo 相關指令

### 3.1 新增文章

```bash
hexo new post "<文章標題>"
```

### 3.2 新增頁面

```bash
hexo new page "<頁面標題>"
```

### 3.3 產生靜態檔案

```bash
hexo generate
```

### 3.4 啟動伺服器

```bash
hexo server
```

---

## 4. 總結

Hexo 是一個輕量級部落格工具，適合想寫部落格但不想花費主機費用的使用者。可以結合 GitHub Pages 免費架站，下一篇將介紹如何部署至 GitHub。
