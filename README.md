# 🧩 Lead Distribution & Campaign Management Platform

## 📖 Overview
This project is a **lead generation and distribution platform** that enables:
- Multi-campaign landing pages for collecting user data  
- Automated data validation through third-party APIs  
- Partner (B2B) portal for purchasing and receiving leads  
- Admin dashboard for campaign and partner management  

Leads are validated, categorized, and distributed automatically via API to partner systems — ensuring delivery within **30 minutes** of submission.

---

## 🚀 Core Features

### 🏠 Main Page
- Login portal for **Admin** and **B2B Partners**
- Overview of system and campaign performance

### 🧭 Landing Pages
- Dynamic landing pages for each campaign  
- Collects user data: `name`, `address`, `email`, `phone`, etc.  
- Built for conversion and easy deployment  
- Data is sent securely to the backend via API

### 🔍 Data Validation Layer
- Integrates with **third-party APIs** (e.g., Verifalia, Telesign, Clearout)
- Checks for false or invalid info before database storage
- Flags invalid entries for review
- Ensures verified data before delivery to partners

### 🗂️ Campaign Management
- Leads organized by **campaign**
- Each campaign can have one or multiple active landing pages
- Admin can create, update, or archive campaigns
- Adjustable pricing per campaign

### 💼 Partner (B2B) Portal
- Login for partners to view and manage campaigns  
- Choose campaigns to receive leads from  
- Adjust budget for:
  - **Auto-delivery:** Automatically receive X leads daily/weekly
  - **Manual purchase:** Buy selected leads on demand  
- View analytics: leads received, spend, conversion  
- Leads automatically delivered via API (JSON/XML)

### 🧑‍💼 Admin Portal
- Full access to manage the system
- Create / edit campaigns
- Manage partners and budgets
- Adjust distribution rules
- Override / refund transactions
- Manage payments and monitor API logs
- Configure validation API keys

### ⚙️ Automation Layer
- Background jobs for:
  - Validating new leads
  - Distributing verified leads to partners
  - Retrying failed deliveries
  - Sending notifications
- Guarantee: **Lead delivered within 30 minutes**

### 💳 Payments (Phase 2)
- Integrate with Stripe or PayPal
- Payment options:
  - Prepaid wallet system
  - Pay-per-lead at purchase
  - Monthly invoicing for trusted partners
- Track revenue and balance for each partner

---

## 🏗️ System Architecture

```plaintext
[User Landing Page] 
   ↓
[Frontend Validation]
   ↓
[API Gateway]
   ↓
[3rd-Party Data Validation]
   ↓
[Database Storage]
   ↓
[Campaign Assignment]
   ↓
[Partner Portal Access]
   ↓
[Partner Auto-Buy / Manual Purchase]
   ↓
[Lead Sent via API]
   ↓
[Logs + Analytics Updated]