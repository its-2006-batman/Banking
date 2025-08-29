<h1><img src="public/icons/logo.svg"> Horizon Banking Platform</h1>

Horizon is a **financial SaaS platform** built with **Next.js**. It connects multiple bank accounts, displays transactions in **real time**, enables **fund transfers** between users, and provides a complete **finance management** experience.

---

## 🤖 Introduction

Built with Next.js, Horizon connects to multiple bank accounts, displays transactions in real-time, allows users to transfer money to other platform users, and manages their finances altogether.

---

## ⚙️ Tech Stack

⚡ Next.js – React framework

🟦 TypeScript – Type safety

🗄 Appwrite – Authentication & backend services

🔗 Plaid – Bank account linking

💳 Dwolla – Payment transfers

📝 React Hook Form – Form management

✅ Zod – Schema validation

🎨 Tailwind CSS – Styling

📊 Chart.js – Data visualization

🧩 ShadCN – UI components

---

## 🔋 Features

* **Authentication** – Ultra-secure SSR authentication with validations & authorization
* **Connect Banks** – Integrates Plaid for multiple bank account linking
* **Home Page** – Overview: total balance, recent transactions, category spend & insights
* **My Banks** – Full list of connected banks with balances & account details
* **Transaction History** – Paginated & filterable per-bank transactions
* **Real-time Updates** – Changes reflected across relevant pages after linking accounts
* **Funds Transfer** – Secure transfers via Dwolla with recipient bank/user ID
* **Responsive Design** – Optimized for desktop, tablet & mobile
* **Code Architecture** – Clean structure & reusable components

---

## 📂 Project Structure (Tree)

```text
horizon-banking/
├── app/                  # Next.js app directory (routes, layouts, pages)
│   ├── (auth)/           # Authentication pages (sign-in, sign-up)
│   ├── (dashboard)/      # Dashboard pages (home, transactions, banks, transfers)
│   └── api/              # API routes for server actions
│
├── components/           # Reusable UI + feature components
│   ├── forms/            # Authentication & transfer forms
│   ├── ui/               # ShadCN & custom UI components
│   └── charts/           # Chart.js visualizations
│
├── lib/                  # API clients & utilities
│   ├── appwrite.ts       # Appwrite SDK setup
│   ├── plaid.ts          # Plaid API integration
│   ├── dwolla.ts         # Dwolla API integration
│   └── utils.ts          # Helper utilities
│
├── constants/            # Static configs & enums
├── types/                # TypeScript types
├── hooks/                # Custom React hooks
├── styles/               # Global Tailwind styles
├── public/               # Static assets (icons, logos, images)
├── .env.example          # Example environment variables
├── tailwind.config.ts    # TailwindCSS config
├── tsconfig.json         # TypeScript config
├── package.json          # Dependencies & scripts
└── README.md             # Documentation
```

---

## 🏗 Architecture Overview (Mermaid)

```mermaid
flowchart TD

    subgraph User["👤 User"]
        A1[Login / Signup]
        A2[Link Bank Accounts]
        A3[View Dashboard]
        A4[Transfer Funds]
    end

    subgraph Next["⚡ Next.js App"]
        B1[SSR Authentication]
        B2[Dashboard UI]
        B3[API Routes / Server Actions]
    end

    subgraph Backend["🗄 Backend Services"]
        C1[(Appwrite)]
        C2[(Plaid API)]
        C3[(Dwolla API)]
    end

    %% Connections
    User -->|HTTPS| Next
    Next -->|Auth / Sessions| C1
    Next -->|Bank Linking / Transactions| C2
    Next -->|Payments / Transfers| C3
    C2 -->|Bank Data| Next
    C3 -->|Transfer Status| Next
```

---

## 🗂 Visual Project Architecture (Mermaid)

```mermaid
graph TD

    subgraph App["⚡ app/ (Next.js)"]
        A1[(auth)] -->|Sign In/Up| A3[API Routes]
        A2[(dashboard)] -->|Home, Banks, Transactions| A3
        A3[api/] --> Backend
    end

    subgraph Components["🎨 components/"]
        C1[forms/] --> App
        C2[ui/] --> App
        C3[charts/] --> App
    end

    subgraph Lib["🛠 lib/"]
        L1[appwrite.ts]
        L2[plaid.ts]
        L3[dwolla.ts]
        L4[utils.ts]
    end

    subgraph Config["⚙️ Config & Types"]
        D1[constants/]
        D2[types/]
        D3[hooks/]
        D4[styles/]
    end

    subgraph Assets["🖼 Assets"]
        P1[public/]
    end

    %% Connections
    App --> Components
    App --> Lib
    App --> Config
    Components --> Lib
    Lib --> Backend
    Assets --> App
```

---

## 🚀 Getting Started

### 1) Install dependencies

```bash
npm install
# or
yarn install
```

### 2) Configure environment variables

Copy `.env.example` → `.env` and set credentials for **Appwrite**, **Plaid**, and **Dwolla**.

### 3) Run the development server

```bash
npm run dev
# or
yarn dev
```

Then open **[http://localhost:3000](http://localhost:3000)**.

---

## 🔑 Environment Variables

```bash
# Appwrite
NEXT_PUBLIC_APPWRITE_ENDPOINT=
NEXT_PUBLIC_APPWRITE_PROJECT=
APPWRITE_API_KEY=

# Plaid
PLAID_CLIENT_ID=
PLAID_SECRET=
PLAID_ENV=sandbox # or development/production

# Dwolla
DWOLLA_KEY=
DWOLLA_SECRET=
DWOLLA_ENV=sandbox # or production
```

> Tip: Never commit `.env`—use `.env.local` for development and CI secrets for deployments.

---

## 🧰 Scripts

```json
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  }
}
```

---

## 📦 Deployment

Deploy with **Vercel**:

* One-click: https://banking-five-gamma.vercel.app/
* Docs: [https://nextjs.org/docs/app/building-your-application/deploying](https://nextjs.org/docs/app/building-your-application/deploying)

---
<img width="2875" height="1616" alt="image" src="https://github.com/user-attachments/assets/91f8e9f5-7678-4cb2-8b27-86eb932747ba" />
<img width="2873" height="1609" alt="image" src="https://github.com/user-attachments/assets/bb8d69a7-4065-4409-8cac-74afa8ae64dd" />
<img width="2872" height="1609" alt="image" src="https://github.com/user-attachments/assets/ee490f71-f1fe-45ab-b892-36667512b6d9" />
<img width="2875" height="1613" alt="image" src="https://github.com/user-attachments/assets/5ae5ac9d-b916-4205-b985-9af4c2899674" />
<img width="2879" height="1616" alt="image" src="https://github.com/user-attachments/assets/09d51bde-0e02-4507-b7cd-c60332625d2c" />
<img width="2879" height="1608" alt="image" src="https://github.com/user-attachments/assets/6a71bb6e-c936-4d18-af8c-fa975a5ccb2d" />


