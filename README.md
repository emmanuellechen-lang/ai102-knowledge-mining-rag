# ai102-knowledge-mining-rag
AI-102 portfolio: RAG assistant for my book "高我喚醒我的38件事" using Azure AI Search + Azure OpenAI
# AI-102 Portfolio — 《高我喚醒我的38件事》RAG 助教

## 1) 專案目標
用 Azure AI Search + Azure OpenAI 建立「可引用」的書籍 RAG 助教：
- 問答：回答附引用（章節/段落）
- 摘要：指定章節摘要附引用
- 知識挖掘：抽取行動清單/金句成結構化資料

## 2) 架構（Classic RAG）
Query → Azure AI Search (Hybrid + Semantic Ranking) → Top-k chunks → Azure OpenAI → Answer with citations

## 3) 資料策略（避免全文公開）
- data_private/: 放整本書全文/電子書檔（不 commit）
- data_sample/: 放少量示例段落（可公開）
- .env: 放金鑰（不 commit）

## 4) 里程碑
- M1: 文本整理 + Chunk/Metadata
- M2: 本機 RAG 原型（可回覆 + 引用）
- M3: 上 Azure AI Search（Hybrid + Semantic ranker）
- M4: 評估 + Content Safety
