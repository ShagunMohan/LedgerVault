# 🛡️ LedgerVault AI

> **The 100% Private, Local-First Expense & Invoice Sorter for Freelancers**  
> *Built with open-weight AI at its core for Hacktoberfest 2026: Side Hustle Theme.*

[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)
[![Hacktoberfest 2026](https://img.shields.io/badge/Hacktoberfest-2026%20Side%20Hustle-6366f1.svg)](https://dev.to/challenges/hacktoberfest-week2-2026-10-12)
[![Local First](https://img.shields.io/badge/Privacy-100%25%20On--Device-10b981.svg)]()
[![Currency](https://img.shields.io/badge/Currency-INR%20(%E2%82%B9)%20%26%20Global-cyan.svg)]()
[![Model Compatibility](https://img.shields.io/badge/Models-Llama%203.2%20%7C%20Qwen%202.5-purple.svg)]()

---

## 📌 Overview

**LedgerVault AI** is an on-device bookkeeping engine engineered specifically for freelancers, consultants, and boutique agency owners. It uses open-weight AI models to automatically parse receipts, extract line items and GST, categorize tax deductions, and detect audit risks — with **0 bytes ever leaving your computer**.

No subscription lock-in. No cloud data harvesting. No violation of client NDAs.

---

## ✨ Key Features

* **⚡ Zero-Cloud Privacy Guarantee**: All OCR, neural token parsing, and financial schema extraction runs directly in your browser (via Web-WASM) or connected to your local GPU via an Ollama daemon.
* **🎯 Statutory Tax Intelligence**:
  * **Indian Income Tax Act**: Section 37(1) general business write-offs, Section 44ADA presumptive taxation benchmark, Section 32 computer depreciation blocks, and Section 194J/194C TDS alerts.
  * **GST Input Tax Credit (ITC)**: Itemizes CGST, SGST, and IGST for B2B offset against client invoicing.
  * **IRS Schedule C Compatibility**: 50% business meal deductibility rules, de minimis safe harbor expensing.
* **🔍 Interactive Document Visualizer**: Live bounding boxes highlighting detected merchants, dates, subtotals, and GST amounts over uploaded receipts.
* **📊 Real-Time Financial Analytics**:
  * Interactive SVG Category Distribution Donut Chart with hover statistics.
  * Monthly Deduction Trend Dual Bar Chart (Gross vs Deductible).
  * Client Billable Reimbursement Pipeline.
* **📥 1-Click Export Center**:
  * **RFC 4180 CSV**: Formatted for Tally, Zoho Books, QuickBooks, and Excel.
  * **Standardized JSON**: Open accounting schema for automation scripts.
  * **Print-Ready Audit Summary**: Formal statutory report ready for filing with Chartered Accountants or IRS returns.
  * **Client Reimbursement Statement**: Itemized disbursement sheet to attach to client retainers.
* **🦙 Dual Inference Engine**:
  * **In-Browser Web-WASM Engine**: Zero setup required, works instantly on any computer.
  * **Ollama Local Bridge**: Connects to `http://localhost:11434` for hardware-accelerated Llama 3.2 3B or Qwen 2.5 inference.

---

## 🚀 Quick Start Guide

LedgerVault AI is built with vanilla web technologies and requires no complex build tools or npm installs.

### Option 1: Python HTTP Server (Recommended)
```bash
# Navigate to the project directory
cd "week 2"

# Start the local server
python -m http.server 8088
```
Open **[http://localhost:8088](http://localhost:8088)** in your web browser.

### Option 2: Node.js (npx serve)
```bash
npx serve -l 8088
```

### Option 3: Direct File Access
Simply double-click `index.html` to open it in Chrome, Edge, Firefox, or Safari.

---

## 🦙 Connecting to Local Ollama (Optional GPU Acceleration)

If you have [Ollama](https://ollama.com/) installed locally:

1. Pull an open-weight model:
   ```bash
   ollama pull llama3.2:3b
   # or
   ollama pull qwen2.5:7b
   ```
2. Start Ollama with permissive CORS (if accessing from a browser):
   ```bash
   # Windows PowerShell
   $env:OLLAMA_ORIGINS="*" ; ollama serve
   ```
3. Open LedgerVault AI, click **"AI Settings"** in the top navigation, select **"Ollama Local Server"**, and click **"Test Local Connection"**.


---

## 💡 The Side Hustle Business Model & Unit Economics

Traditional bookkeeping apps running on closed cloud vision APIs incur heavy recurring API bills:

| Dimension | Proprietary Cloud API (OpenAI/Google Vision) | LedgerVault AI (Open-Weight Models) |
| :--- | :--- | :--- |
| **Inference Cost / Doc** | ₹5.00 – ₹12.00 / receipt | **₹0.00 (On-device compute)** |
| **Annual Server API Bill** | ~₹1,50,000 / year (per 1k users) | **₹0.00 / year** |
| **Customer Pricing** | Forced ₹1,500/mo subscription | **₹2,999 One-Time Lifetime License** |
| **Data Breach Risk** | Cloud processor liability under DPDP Act 2023 | **Zero liability**: Data never leaves device |
| **Gross Profit Margin** | 45% – 60% | **96.8%** |

Open-source AI transforms a cost-prohibitive cloud API wrapper into a high-margin, sustainable side hustle business product.

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

*Built with ❤️ for the Hacktoberfest 2026 Open-Source AI Challenge (Week 2: Side Hustle).*
