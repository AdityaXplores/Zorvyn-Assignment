# 💰 Finance Dashboard

Track your income and expenses with a modern full-stack finance dashboard.

---

## ⚙️ Tech Stack

* **Frontend:** Next.js, React, TailwindCSS
* **Backend:** Hono, Drizzle ORM
* **Database:** PostgreSQL (Neon)
* **Auth:** Clerk
* **State/Data:** React Query, Zustand
* **Charts:** Recharts

---

## 📦 Setup Instructions

### 1️⃣ Clone the repo

```bash
git clone <your-repo-url>
cd finance-dashboard
```

---

### 2️⃣ Install dependencies

```bash
npm install
```

> ⚠️ If you face dependency issues:

```bash
npm install --legacy-peer-deps
```

---

### 3️⃣ Fix known dependency issue

```bash
npm install date-fns@3
```

---

### 4️⃣ Setup environment variables

Create `.env.local`:

```env
NEXT_TELEMETRY_DISABLED=1

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_key
CLERK_SECRET_KEY=your_secret

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

DATABASE_URL=your_database_url

NEXT_PUBLIC_APP_URL=http://localhost:3000
```

---

### 5️⃣ Run database setup

```bash
npm run db:generate
npm run db:migrate
npm run db:seed
```

---

### 6️⃣ Run the app

```bash
npm run dev
```

---

## 🧹 Clean Reset (if something breaks)

### Windows (PowerShell):

```powershell
Remove-Item -Recurse -Force node_modules
Remove-Item -Force package-lock.json
npm install
```

---

## ⚠️ Important Notes

* ✅ Do **NOT delete `package-lock.json` permanently**
* ❌ Do **NOT run `npm uninstall package-lock.json`**
* ⚠️ Ensure `date-fns` version is compatible (`v3`)

---

## 🧠 Common Issues

### ❌ `Missing script: dev`

👉 Add in `package.json`:

```json
"scripts": {
  "dev": "next dev"
}
```

---

### ❌ Dependency conflict (`ERESOLVE`)

👉 Fix:

```bash
npm install date-fns@3
```

---

## 📊 Features

* Dashboard analytics
* Income & expense tracking
* Charts & reports
* Category management
* Authentication

---

## 🚀 Deployment

Deploy easily on **Vercel**

---

## 🙌 Contributing

Pull requests are welcome!

---

## ⭐ Support

Give this project a star if it helped you!
