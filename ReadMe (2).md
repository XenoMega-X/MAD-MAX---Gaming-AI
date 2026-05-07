# 💀 MAD MAX — Gaming Intelligence System

> Elite AI-powered gaming assistant. Ask about any game, get smart recommendations, filter by specs, budget, or platform.

![MAD MAX Banner](https://img.shields.io/badge/MAD%20MAX-Gaming%20Intelligence-ff2d78?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyem0tMiAxNWwtNS01IDEuNDEtMS40MUwxMCAxNC4xN2w3LjU5LTcuNTlMMTkgOGwtOSA5eiIvPjwvc3ZnPg==)
![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000000?style=for-the-badge&logo=vercel)
![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js)

---

## ✨ Features

- **AI Gaming Intelligence** — Ask about any game and get detailed, structured info
- **Smart Recommendations** — Get game suggestions based on genre, platform, or style
- **Spec Filtering** — Find games by PC specs, storage size, price, or platform
- **Live Trending** — Real-time trending games loaded on startup
- **Secure Auth** — JWT-based login and registration system
- **Thanos Snap** — Click the logo to clear chat with a particle explosion effect
- **Mobile Friendly** — Fully responsive, works great on all devices

## 🛠️ Tech Stack

- **Frontend** — Vanilla HTML, CSS, JavaScript (zero frameworks)
- **Backend** — Node.js serverless functions (Vercel)
- **AI** — Groq API with `llama-3.3-70b-versatile`
- **Auth** — JWT (JSON Web Tokens) + bcrypt
- **Deploy** — Vercel (one-click)

## 🚀 Deploy to Vercel

### 1. Clone & Push to GitHub

```bash
git clone https://github.com/yourusername/madmax-gaming.git
cd madmax-gaming
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/madmax-gaming.git
git push -u origin main
```

### 2. Connect to Vercel

1. Go to [vercel.com](https://vercel.com) → **New Project**
2. Import your GitHub repository
3. Add **Environment Variables** (see below)
4. Click **Deploy**

### 3. Environment Variables

Set these in your Vercel project settings under **Settings → Environment Variables**:

| Variable | Description | Example |
|---|---|---|
| `GROQ_API_KEY` | Your Groq API key | `gsk_xxx...` |
| `JWT_SECRET` | Secret for signing tokens | `any-long-random-string` |
| `ADMIN_USERNAME` | Admin login username | `admin` |
| `ADMIN_PASSWORD` | Admin login password | `yourpassword` |

### 4. Get a Groq API Key

1. Go to [console.groq.com](https://console.groq.com)
2. Sign up / Log in
3. Go to **API Keys** → **Create API Key**
4. Copy and paste into Vercel env vars

## 📁 Project Structure

```
madmax-gaming/
├── api/
│   ├── auth.js        # Login + Register endpoint
│   └── groq.js        # Groq AI proxy (keeps API key secret)
├── index.html         # Login page
├── register.html      # Register page
├── app.html           # Main chat application
├── vercel.json        # Vercel routing config
├── package.json       # Dependencies
├── .env.example       # Example environment variables
└── .gitignore
```

## 🔐 Security

- **API key is server-side only** — never exposed to the browser
- **JWT authentication** — all AI requests require a valid token
- **bcrypt password hashing** — passwords are never stored in plain text
- **Token expiry** — sessions automatically expire after 7 days

## 🎮 Usage

| What you can ask | Example |
|---|---|
| Game details | `Tell me about Elden Ring` |
| Recommendations | `Games like Dark Souls` |
| Filter by spec | `Best games under 4GB RAM` |
| Free games | `Best free PC games` |
| Platform specific | `Best Android offline games` |
| Genre search | `Best horror games of all time` |

## 📄 License

MIT — free to use, modify, and distribute.
