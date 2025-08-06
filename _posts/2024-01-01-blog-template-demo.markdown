---
layout:     post
title:      "博客文章格式示範"
subtitle:   "完整的 Markdown 格式展示和寫作指南"
date:       2024-01-01 12:00:00
author:     "Yuan"
header-img: "img/post-bg-universe.jpg"
catalog:    true
tags:
    - 博客
    - Markdown
    - 教學
    - 示範
---

> "這是一篇完整的博客文章格式示範，展示了所有可用的 Markdown 語法和功能。"

## 前言

歡迎來到我的博客！這篇文章將展示這個博客支持的所有格式和功能，包括文字格式、代碼高亮、圖片、鏈接等等。

---

## 文字格式

### 基本格式

這是**粗體文字**，這是*斜體文字*，這是***粗斜體文字***。

這是~~刪除線文字~~。

這是`行內代碼`的示例。

### 引用

> 這是一個引用塊。
> 
> 可以包含多行內容。
> 
> > 這是嵌套引用。

### 列表

**無序列表：**
- 第一項
- 第二項
  - 子項目 1
  - 子項目 2
- 第三項

**有序列表：**
1. 第一步
2. 第二步
   1. 子步驟 A
   2. 子步驟 B
3. 第三步

---

## 代碼展示

### 行內代碼
使用 `console.log()` 來輸出信息。

### 代碼塊

**JavaScript 示例：**
```javascript
function greetUser(name) {
    console.log(`Hello, ${name}!`);
    return `Welcome to Yuan's Blog, ${name}!`;
}

// 調用函數
const message = greetUser("讀者");
console.log(message);
```

**Python 示例：**
```python
def fibonacci(n):
    """計算斐波那契數列"""
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

# 生成前10個斐波那契數
for i in range(10):
    print(f"F({i}) = {fibonacci(i)}")
```

**HTML 示例：**
```html
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <title>Yuan's Blog</title>
</head>
<body>
    <h1>歡迎來到我的博客</h1>
    <p>這裡分享 AI、開發和投資的內容。</p>
</body>
</html>
```

---

## 表格

| 技術棧 | 熟練度 | 應用場景 |
|--------|--------|----------|
| Python | ⭐⭐⭐⭐⭐ | AI/ML 開發 |
| JavaScript | ⭐⭐⭐⭐ | 前端開發 |
| React | ⭐⭐⭐⭐ | 用戶界面 |
| Node.js | ⭐⭐⭐ | 後端服務 |

---

## 鏈接和圖片

### 鏈接示例
- [我的 GitHub](https://github.com/DDChen666)
- [我的 Instagram](https://www.instagram.com/danielchen_16888/)
- [外部鏈接示例](https://www.google.com)

### 圖片示例
![博客示例圖片](/img/post-sample-image.jpg)

---

## 數學公式（如果啟用 MathJax）

行內公式：$E = mc^2$

塊級公式：
$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

---

## 特殊功能

### 警告框（使用引用模擬）

> ⚠️ **注意**：這是一個重要提醒！

> ✅ **提示**：這是一個有用的建議。

> ❌ **錯誤**：這是需要避免的問題。

### 任務列表

- [x] 完成博客搭建
- [x] 配置社交媒體鏈接
- [ ] 撰寫第一篇技術文章
- [ ] 添加評論系統
- [ ] 優化 SEO 設置

---

## 文章結構建議

### 1. 開頭
- 簡潔的引言
- 文章概述

### 2. 主體內容
- 使用標題分段
- 適當的代碼示例
- 清晰的解釋

### 3. 結尾
- 總結要點
- 相關鏈接
- 鼓勵互動

---

## 寫作技巧

1. **保持簡潔**：用簡單明了的語言表達複雜概念
2. **使用示例**：通過實際例子幫助讀者理解
3. **結構清晰**：使用標題和列表組織內容
4. **視覺友好**：適當使用圖片和代碼塊
5. **互動性**：鼓勵讀者評論和分享

---

## 標籤使用指南

選擇合適的標籤有助於文章分類和 SEO：

- **技術類**：AI, Python, JavaScript, React, 機器學習
- **主題類**：教學, 心得, 分析, 評論
- **行業類**：獨立開發, 投資, 創業, 科技

---

## 結語

這篇示範文章展示了博客的所有主要功能。你可以：

1. 複製這個模板開始寫作
2. 根據需要調整格式
3. 添加自己的內容和風格

記住，好的內容比華麗的格式更重要。專注於為讀者提供價值，格式只是輔助工具。

**開始你的寫作之旅吧！** 🚀

---

*如果你覺得這篇文章有幫助，歡迎在下方留言或分享到社交媒體！*