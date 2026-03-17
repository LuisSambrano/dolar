# Dolar API Dashboard

[🇪🇸 Español](README.es.md) | [🇵🇹 Português](README.pt.md)

**🚀 [Live Demo](https://dolar-chi.vercel.app)**

<p align="center">
  <img src="https://img.shields.io/badge/React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React 19" />
  <img src="https://img.shields.io/badge/TypeScript-Strict-blue?style=for-the-badge&logo=typescript" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-Bundler-646CFF?style=for-the-badge&logo=vite" alt="Vite" />
  <img src="https://img.shields.io/badge/TailwindCSS-Styling-06B6D4?style=for-the-badge&logo=tailwindcss" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/License-BSL_1.1-blue?style=for-the-badge" alt="License" />
</p>

## 🏛️ Project Abstract

This repository contains the source code for a real-time exchange rate dashboard. Built with **React 19** and **Vite**, the application consumes public endpoints to display currency pair metrics. The architecture is optimized for minimal rendering overhead and stable layout calculation, providing an efficient continuous data-stream visualization layer.

---

## ⚙️ Core Technical Features

### 1. Real-Time Data Synchronization

Implementation of polling mechanisms to fetch JSON streams from the DolarAPI. Includes caching strategies to minimize network saturation while maintaining updated metrics for multiple exchange rates (parallel, official, crypto).

### 2. Rendering Optimization

Engineered to prevent React Commit Phase blocking. The interface implements CSS hardware acceleration strategies (transform-gpu) replacing expensive filter operations (like backdrop-blur) with solid opacity alternatives, resolving potential thermal throttling on high-resolution displays.

### 3. Cumulative Layout Shift (CLS) Mitigation

Zero layout shift engineering through exact-geometry skeleton loaders, ensuring the DOM tree remains immutable during the data fetching lifecycle.

---

## 🏗️ Technical Architecture Overview

```text
dolar-api/
├── src/
│   ├── components/
│   │   ├── ui/                 # Reusable React components
│   │   └── CurrencyDashboard/  # Core domain component
│   ├── services/
│   │   └── dolarService.ts    # API client and network layer
│   ├── types/
│   │   └── currency.ts        # Strict TypeScript interfaces
│   ├── App.tsx                # Application root
│   └── main.tsx               # Bootstrap entry point
```

**Enterprise Tech Stack:**

- **Framework:** React 19 (Client-Side Rendering)
- **Build Tool:** Vite
- **Styling:** Tailwind CSS, Framer Motion
- **Engine:** TypeScript (Strict Mode)

---

## ⚙️ Installation & Development

Ensure you have `Node.js 18+` installed.

1. **Clone the repository:**

   ```bash
   git clone https://github.com/LuisSambrano/dolar-api.git
   ```

2. **Install dependencies:**

   ```bash
   cd dolar-api
   npm install
   ```

3. **Run the local development server:**
   ```bash
   npm run dev
   ```

---

## 🎨 Code Standards

This repository enforces strict engineering standards:

1. `npm run lint` must yield zero errors or warnings before committing.
2. `tsc --noEmit` must pass without type errors.
3. No `any` types allowed; use strict typing or `unknown` with Type Guards.
4. Conventional Commits are required for version control.

---

## 📄 License & Contributing

This project is licensed under the [Business Source License 1.1](LICENSE). You may view and study the source code for educational purposes, but commercial use requires a separate license.
