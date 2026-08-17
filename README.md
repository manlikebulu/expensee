# expensee – Smart Budgeting & Expense Tracker

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=flat&logo=Firebase&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)

**expensee** is a fully functional, client-side expense management application that syncs your data across devices using **Firebase**. It comes with real-time updates, budget tracking, spending reports, profile management (including picture upload), and a clean, responsive UI.

---

## 📸 Screenshots

| Dashboard | Expenses | Reports |
|-----------|----------|---------|
| ![Dashboard](https://via.placeholder.com/400x200/1e293b/ffffff?text=Dashboard) | ![Expenses](https://via.placeholder.com/400x200/1e293b/ffffff?text=Expenses) | ![Reports](https://via.placeholder.com/400x200/1e293b/ffffff?text=Reports) |

---

## ✨ Features

### 🔐 Authentication
- Sign up / Sign in with **Email/Password**
- Sign in with **Google** (works on mobile with popup/redirect fallback)
- **Forgot password** flow
- **Password show/hide** toggle

### 💰 Expense Management
- Add, edit, delete, and filter expenses by category or date range
- Categorise expenses into 8 default categories (customizable in code)
- Payment method tracking (Cash, Card, Bank Transfer, Other)

### 📊 Budget Tracking
- Set monthly budgets per category
- Visual **progress bars** show how much you've spent
- **Status badges** (On track / Warning / Exceeded) warn you when spending approaches or exceeds 80%

### 📈 Reports & Analytics
- Generate date‑filtered reports
- **Category summary** with spending percentages
- **Daily spending trend** line chart (powered by Chart.js)
- **CSV export** for further analysis

### 👤 Profile Management
- Edit your display name
- Upload a **profile picture** (stored in Firebase Storage)
- Profile picture syncs across all devices

### 📤 Share Insights
- Share your **expense analysis** or **budget plan** via a generated link
- Post directly to **Email, Twitter, LinkedIn, or WhatsApp**

### 💱 Multi-Currency Support
- 17 currencies including **USD, EUR, GBP, JPY, INR, NGN (Naira)**, and more
- All amounts update instantly when you switch

### 🔄 Cross-Device Sync
- Your data is stored in **Firestore**
- Changes made on one device appear in real‑time on all others

### ⚡ Performance
- **Skeleton loaders** for smooth loading states
- Optimised for mobile and desktop

### 📱 Mobile‑First Design
- Fully responsive with a **hamburger menu**
- Touch‑friendly inputs and optimised typography
- Works on all screen sizes

---

## 🛠️ Tech Stack

| Layer         | Technology                                                                 |
|---------------|----------------------------------------------------------------------------|
| **Frontend**  | HTML5, CSS3, Vanilla JavaScript                                            |
| **Fonts**     | Inter (body) + SF Pro (headings) with fallbacks                            |
| **Charts**    | [Chart.js](https://www.chartjs.org/)                                       |
| **Icons**     | [Font Awesome](https://fontawesome.com/)                                   |
| **Backend**   | [Firebase Authentication](https://firebase.google.com/products/auth)       |
| **Database**  | [Cloud Firestore](https://firebase.google.com/products/firestore)          |
| **Storage**   | [Firebase Storage](https://firebase.google.com/products/storage)           |

---

## 🚀 Getting Started

### Prerequisites
- A **Firebase account** (free tier works perfectly)
- Basic knowledge of how to create a Firebase project and enable services

### Step 1: Create a Firebase Project

1. Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project (or use an existing one).
2. In the project overview, click **"Add app"** and select **"Web"**.
3. Register the app with a nickname (e.g., `expensee-web`).
4. **Copy the Firebase configuration object** – you'll need it in the next step.

### Step 2: Enable Authentication

1. In the Firebase Console, go to **Authentication → Sign‑in methods**.
2. Enable **Email/Password**.
3. Enable **Google** (provide a support email when prompted).

### Step 3: Create Firestore Database

1. Go to **Firestore Database → Create database**.
2. Choose **Standard edition**.
3. Select a location close to your users.
4. Start in **test mode** (you can tighten security later).

#### 🔒 Security Rules (Recommended for Production)

Replace the default rules with the following to restrict access to each user's own document:
