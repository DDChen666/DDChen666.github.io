---
layout:     post
title:      "百日AI Vibe Coding 學習地圖"
subtitle:   "想要出一張嘴寫出資深程式專案？來吧！"
date:       2024-02-08 12:00:00
author:     "Yuan"
header-img: "img/post-bg-universe.jpg"
catalog:    true
tags:
    - 獨立開發
    - vibe coding
    - AI
    - 程式設計
    - 學習路線
---

> "對AI Coding新手來說，最難的往往是大量的名詞、架構、技術棧等專業術語，以及數百種編程語言的組合與選擇困難。"

## 前言

對AI Coding新手來說，最難的往往是大量的名詞、架構、技術棧等專業術語，以及數百種編程語言的組合與選擇困難，所以我創建了這個『**Vibe Coding 學習地圖**』。

本文希望拋磚引玉，希望能幫助想編程的新手迅速起步，早日開發出爆款，財務自由！我會逐步將各個階段的細分教程更新上來，希望可以獲得你的反饋，有興趣也歡迎來信或私訊我，一起交流進步！

---

## 🎯 學習目標

**目標**：用 AI 輔助，快速做出「**80% 精美可用**」的網站 / Web App / 行動 Web（不含遊戲）。

**方法**：用「**由淺入深**」的學習階梯。每一階都有——
- 專有名詞 → 類型 → 要懂的知識 → 上手技巧 → 推薦技術棧

---

## 📚 學習階段詳解

### 階段 0｜工具與基本功（1–2 週）

#### 🔤 專有名詞（必背）
- **Git / GitHub**、**CLI（終端機）**、**Node.js**、**npm/pnpm**
- **TypeScript**、**環境變數（ENV）**、**.gitignore**、**README**

#### 📋 類型
版本控管、封包管理、型別系統、專案腳手架（scaffold）

#### 💡 要懂的知識
- 為何用 Git 分支（main/feat/*/fix/*）
- Node 是執行 JS 的「後端引擎」；npm/pnpm 管套件
- TypeScript 讓大型專案更不容易爆

#### 🛠️ 上手技巧
1. 建一個空倉庫 → README 說明 → `pnpm init` → `tsconfig.json`
2. 把私密設定放 `.env`，不進版本庫

#### 🚀 推薦技術棧
- **最小**：Node 20+、pnpm、TypeScript、ESLint、Prettier
- **進階**：Husky（提交前檢查）、Commitlint、EditorConfig

---

### 階段 1｜UI 版面與設計語言（1–2 週）

#### 🔤 專有名詞
- **HTML 語義化**、**CSS Flex/Grid**、**RWD（響應式）**
- **Design Tokens**、**Tailwind CSS**、**A11y（可及性）**
- **SVG**、**Favicon/OG 圖**

#### 📋 類型
版面系統（Grid）、間距/色彩/字體 Token、元件庫（Button/Card/Dialog）

#### 💡 要懂的知識
- 「語義化」影響 SEO 與可讀性
- RWD 三斷點思維：mobile-first
- A11y：鍵盤可操作、替代文字、對比度

#### 🛠️ 上手技巧
1. 先做 Style Guide：字體、主色、間距、圓角、陰影
2. Tailwind：抽出常用 class 做元件片段
3. 圖片壓縮、`<img loading="lazy">`

#### 🚀 推薦技術棧
- **最小**：Tailwind + Radix 或 Headless UI
- **進階**：shadcn/ui（快速漂亮）、Framer Motion（微動畫）

---

### 階段 2｜現代前端框架（2–3 週）

#### 🔤 專有名詞
- **React**、**Next.js**、**路由（App Router）**
- **CSR/SSR/SSG/ISR**、**Server Components**
- **表單驗證（Zod）**、**代碼分割（code-splitting）**、**懶載入（lazy）**

#### 📋 類型
渲染策略、狀態來源（URL/Server/Client）、表單/檔案上傳

#### 💡 要懂的知識
- 何時選 SSR（首屏快、SEO）、何時 SSG/ISR（內容站）
- 最小狀態原則：能放 URL 或由伺服器算，就別放全域 store
- 表單 ≠ 只在前端驗證，同規則後端也要驗

#### 🛠️ 上手技巧
1. Next.js App Router：`/app/(marketing)/...` 與 `/app/(app)/...` 分區
2. 用 Zod 同時驗前後端（型別推導）
3. 圖片與字型用 Next Image/Font 組件

#### 🚀 推薦技術棧
- **最小**：Next.js（App Router）+ Zod + React Hook Form
- **進階**：TanStack Query（資料快取/重試）、SWR、tRPC（型別直通）

---

### 階段 3｜API 與「小後端」（2 週）

#### 🔤 專有名詞
- **HTTP**、**REST**、**OpenAPI**、**JSON Schema**
- **Handler/Service/Repo 分層**、**Idempotency（冪等）**
- **錯誤處理（try/catch、error boundary）**
- **Webhook**、**Cron**、**Serverless Functions**

#### 📋 類型
同步 API、非同步工作（背景任務）、事件通知

#### 💡 要懂的知識
- 合約先行：先寫 OpenAPI/型別，前後端對齊
- 冪等：重試不會「重扣款」
- 失敗策略：重試、退避、逾時、斷路器

#### 🛠️ 上手技巧
1. Next.js Route Handlers 快速做 API
2. 任務排程：平台 Cron（如 Vercel/Cloudflare）定期跑
3. Webhook：驗簽（signature）、重放保護（重複檢查）

#### 🚀 推薦技術棧
- **最小**：Next Route Handlers + OpenAPI（or zod-to-openapi）
- **進階**：Serverless Queue（Upstash Q/Stainless）、Temporal（workflow）

---

### 階段 4｜資料層（交易庫、快取、檔案）（2–3 週）

#### 🔤 專有名詞
- **關聯式資料庫（PostgreSQL）**、**ORM（Prisma/Drizzle）**
- **遷移（Migration）**、**索引**、**N+1**
- **Redis（快取/節流）**、**S3/R2（物件儲存）**、**CDN**
- **向量（pgvector）**、**全文檢索**

#### 📋 類型
OLTP（交易）vs OLAP（分析）、熱資料 vs 冷資料

#### 💡 要懂的知識
- 基本正規化、主鍵/外鍵、唯一約束
- 為什麼要加索引；N+1 的危害與批次查詢
- 靜態檔→S3/R2；給 CDN 頭（Cache-Control、ETag）

#### 🛠️ 上手技巧
1. 先畫 ER 圖（User/Org/Project/Invoice…）
2. `created_at`/`updated_at` 必備；`deleted_at` 軟刪除
3. Redis：頁面片段快取、rate limit、工作去重

#### 🚀 推薦技術棧
- **最小**：Postgres（託管 Supabase/Neon/Railway）+ Prisma
- **進階**：Redis（Upstash）+ R2/S3 + pgvector（語義搜尋）

---

### 階段 5｜認證、授權、多租戶（1–2 週）

#### 🔤 專有名詞
- **OAuth/OIDC**、**Session vs JWT**、**CSRF/CORS**
- **RBAC**、**多租戶（單庫分隔/多庫分隔）**、**審計日誌**

#### 📋 類型
第三方登入、組織/團隊、角色/權限、審計/合規

#### 💡 要懂的知識
- 不自做密碼庫，交給 OAuth Provider
- RBAC：角色（Owner/Admin/Member）→ 資源範圍（Org/Project）
- CORS/CSRF：跨網域與跨站偽造

#### 🛠️ 上手技巧
1. 用現成套件快速搞定：回呼 URL、Scopes、狀態驗證
2. 審計：把「誰、何時、對什麼、做了什麼」記成表格

#### 🚀 推薦技術棧
- **最小**：NextAuth/Auth.js + GitHub/Google、session cookie
- **進階**：Clerk/WorkOS/Auth0（企業整合）、自建 RBAC 表

---

### 階段 6｜測試與品質（1–2 週）

#### 🔤 專有名詞
- **Unit/Integration/E2E**、**Contract Testing**、**Mock**
- **Seed**、**Feature Flags**、**CI**

#### 📋 類型
單元測、整合測、端到端、契約測試、灰度釋出

#### 💡 要懂的知識
- 測「錢會不會少扣、檔案會不會丟、權限會不會外洩」
- 先寫關鍵路徑 E2E（登入→建立→修改→刪除）

#### 🛠️ 上手技巧
1. 假資料（seed）讓 E2E 可重跑
2. Pull Request 自動跑 CI，紅燈不合併

#### 🚀 推薦技術棧
- **最小**：Vitest/Jest（單元）＋ Playwright（E2E）
- **進階**：Pact（契約測試）、msw（mock API）

---

### 階段 7｜部署與可觀測（1–2 週）

#### 🔤 專有名詞
- **CI/CD**、**環境（dev/staging/prod）**、**Secrets**
- **Logs/Metrics/Traces**、**p95 延遲**、**Error Rate**
- **QPS**、**成本監控**

#### 📋 類型
邊緣部署、Serverless、多環境、監控告警

#### 💡 要懂的知識
- 12-Factor：設定外部化、不可變建置
- 指標門檻：p95 < 300ms、錯誤率 < 1%

#### 🛠️ 上手技巧
1. GitHub Actions：測試→建置→部署
2. 平台內建觀測 + Sentry/Error Tracking；加 request-id

#### 🚀 推薦技術棧
- **最小**：Vercel 或 Cloudflare（Pages/Workers/D1/R2）
- **進階**：Grafana/Loki/Tempo、Inngest/Temporal（可靠任務）

---

### 階段 8｜AI 整合與自動化（2–3 週）

#### 🔤 專有名詞
- **LLM Provider 抽象**、**Prompt 模板**、**結構化輸出（JSON Schema）**
- **RAG**、**Chunking**、**嵌入（Embeddings）**、**向量索引**
- **Tool Use**、**Evals（離線評測）**、**快取（Prompt Hash + TTL）**
- **失敗降級（Fallback）**、**提示注入**

#### 📋 類型
查詢型（問答/搜尋）、轉換型（摘要/翻譯）、流程型（多步驟代理）

#### 💡 要懂的知識
- RAG 的關鍵在資料清理、切塊策略、檢索品質
- 成本與延遲：盡量快取、結果可重放、可降級
- 安全：不要把私密資料丟去不該去的地方

#### 🛠️ 上手技巧
1. 統一 `callLLM(model, prompt, schema)` 介面，內建重試/快取/日誌
2. 先做 Evals 小題庫（20–50 題）量化改進

#### 🚀 推薦技術棧
- **最小**：OpenAI/Anthropic SDK + JSON schema 驗證 + pgvector
- **進階**：LangChain/LlamaIndex（選其一）+ Ingest 管線 + Evals（Ragas 類）

---

### 階段 9｜商品化（1–2 週並行）

#### 🔤 專有名詞
- **SEO/OG**、**Analytics**、**i18n**、**支付（Stripe)**
- **發票/稅務**、**法遵（ToS/隱私）**

#### 💡 要懂的知識與技巧
- 站內事件追蹤（漏斗）、A/B 測試
- 價格層（免費/專業）用 Feature Flags 控制解鎖
- 法務頁面生成模板，避免踩雷

#### 🚀 推薦技術棧
- **最小**：Next SEO、Plausible/Umami、Stripe Checkout
- **進階**：Segment/Amplitude、i18n（next-intl）

---

## 📋 一頁式總清單（照這個順序疊加）

1. **基礎**：Git、Node、TS、CLI → 專案 scaffolding
2. **UI**：HTML/CSS、Tailwind、RWD、A11y、動效基礎
3. **前端框架**：Next.js（路由、SSR/SSG/ISR、表單、圖片）
4. **API**：REST、OpenAPI、分層設計、錯誤處理、Cron/Webhook
5. **資料**：Postgres + ORM、索引/N+1、Redis、S3/R2、pgvector
6. **Auth**：OAuth/OIDC、Session、RBAC、多租戶、審計
7. **測試**：Unit/Integration/E2E、契約測試、種子資料
8. **部署觀測**：CI/CD、多環境、Logs/Metrics/Traces、Sentry
9. **AI**：Provider 抽象、結構化輸出、RAG、Tool Use、Evals、快取/降級
10. **商品化**：SEO、Analytics、Stripe、i18n、法遵

---

## 🛤️ 兩條可直接起跑的技術棧（你選一條先跑）

### A. 個人/小團隊「超快線路」（從 0 到可收費）

```
Next.js（App Router） + Tailwind + shadcn/ui
Auth.js（GitHub/Google）
Postgres（Neon/Supabase 託管） + Prisma
Redis（Upstash）、R2/S3（檔案）
Serverless Functions + Cron（Vercel/Cloudflare）
Playwright（E2E）、GitHub Actions（CI/CD）、Sentry（錯誤）
OpenAI/Anthropic SDK + pgvector（RAG）
```

### B. 更「流程化/耐高峰」線路

```
Next.js + tRPC（端到端型別）
Postgres + Drizzle（更輕量 SQL-first）
Inngest/Temporal（可靠工作流）
OpenSearch（全文/聚合） + pgvector
Grafana/Loki/Tempo（自建觀測）
其餘同上
```

---

## 🎯 最小實作里程碑（4 週）

### 第 1 週
登陸頁＋Blog（SSR/ISR）、UI 系統、SEO、部署（Vercel/CF）

### 第 2 週
登入（OAuth）、資料庫（Postgres）、CRUD、檔案上傳（R2/S3）

### 第 3 週
E2E 測試、儀表板（p95/錯誤率/成本）、Webhook/Cron

### 第 4 週
AI 功能（RAG/翻譯/摘要：任選 1）、快取與降級、基礎訂閱（Stripe）

---

## 結語

這份學習地圖涵蓋了從零基礎到能夠開發出商業級 Web 應用的完整路徑。記住，**實作比理論更重要**，每個階段都要動手做出實際的項目。

AI 輔助編程的時代已經來臨，但基礎知識和架構思維仍然是不可或缺的。希望這份地圖能幫助你在 AI Coding 的路上走得更順暢！

**開始你的 Vibe Coding 之旅吧！** 🚀

---

*如果這篇文章對你有幫助，歡迎分享給更多想要學習 AI Coding 的朋友！有任何問題或建議，也歡迎在下方留言討論。*