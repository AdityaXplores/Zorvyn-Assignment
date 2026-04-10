# 💰 Finance Dashboard

Track your income and expenses with a modern full-stack finance dashboard.
<img width="1055" height="632" alt="image" src="https://github.com/user-attachments/assets/3dff0208-ac65-4fe0-815f-7d252cdbf6df" />


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
Make sure Git and NodeJS is installed.
Clone this repository to your local computer.
Create .env.local file in root directory.
Contents of .env.local:
Obtain Clerk Authentication Keys

Source: Clerk Dashboard or Settings Page
Procedure:
Log in to your Clerk account.
Navigate to the dashboard or settings page.
Look for the section related to authentication keys.
Copy the NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY and CLERK_SECRET_KEY provided in that section.
Retrieve Neon Database URI

Source: Database Provider (e.g., Neon, PostgreSQL)
Procedure:
Access your database provider's platform or configuration.
Locate the database connection details.
Replace <username>, <password>, <hostname>, and <database> placeholders in the URI with your actual database credentials.
Ensure to include ?sslmode=require at the end of the URI for SSL mode requirement.
Specify Public App URL

Procedure:
Replace http://localhost:3000 with the URL of your deployed application.
Save and Secure:

Save the changes to the .env.local file.
Install Project Dependencies using npm install --legacy-peer-deps or yarn install --legacy-peer-deps.

Migrate database:

In terminal, run npm run db:generate to generate database client and npm run db:migrate to make sure that your database is up-to-date along with schema.

Run the Seed Script:
In the same terminal, run the following command to execute the seed script:

npm run db:seed
This command uses npm to execute the Typescript file (scripts/seed.ts) and writes transaction data in database.

Verify Data in Database:
Once the script completes, check your database to ensure that the transaction data has been successfully seeded.

Now app is fully configured 👍 and you can start using this app using either one of npm run dev or yarn dev.
NOTE: Please make sure to keep your API keys and configuration values secure and do not expose them publicly.

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
