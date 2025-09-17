<h1 align="center">🤖
  <br />
 Multi AI BOT
</h1>

<p align="center">
  A sleek, multi-provider AI chat app with a unified browser interface.<br/>
  Supports <b>OpenAI, Groq, Mistral, Anthropic, Gemini, and xAI</b> — API keys stay safe on the server 🚀
</p>

<p align="center">
  <a href="https://multi-bot-fawn.vercel.app" target="_blank">🌐 Live Demo</a> ·
  <a href="#-features">✨ Features</a> ·
  <a href="#-getting-started">⚡ Getting Started</a> ·
  <a href="#-api-reference">📡 API</a> ·
  <a href="#-tech-stack">🛠 Tech Stack</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Live-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Made%20With-Node.js-blue?style=for-the-badge&logo=node.js" />
  <img src="https://img.shields.io/badge/Deployed%20On-Vercel-black?style=for-the-badge&logo=vercel" />
</p>

---

## ✨ Features

- ✅ **Provider-agnostic** – switch between AI providers effortlessly  
- 🔒 **Secure API handling** – keys managed **server-side** via `.env`  
- 📝 **Markdown rendering** – formatted text + syntax-highlighted code blocks (Marked.js)  
- ⚡ **Smooth UX** – dark theme, compression, HTTP logging  
- ☁️ **Deployment-ready** – plug-and-play with **Vercel** or any Node.js host  

---

## 📂 Project Structure

```

Multi-Bot/
├── public/              # Client-side assets
│   ├── index.html       # Chat interface
│   ├── styles.css       # Dark theme styling
│   └── app.js           # Chat UI logic
│
├── server.js            # Express backend + provider routes
├── package.json         # Dependencies & scripts
├── vercel.json          # Vercel config
└── .env                 # Environment variables (ignored by git)

````

---

## ⚡ Getting Started

### 1️⃣ Prerequisites
- Node.js **v16+**
- npm

### 2️⃣ Installation
```bash
git clone https://github.com/Harshsfd/Multi-Bot.git
cd Multi-Bot
npm install
````

### 3️⃣ Configure Environment

Create `.env` in root:

```env
OPENAI_API_KEY="YOUR_OPENAI_KEY"
GROQ_API_KEY="YOUR_GROQ_KEY"
MISTRAL_API_KEY="YOUR_MISTRAL_KEY"
ANTHROPIC_API_KEY="YOUR_ANTHROPIC_KEY"
GEMINI_API_KEY="YOUR_GEMINI_KEY"
XAI_API_KEY="YOUR_XAI_KEY"

# Optional
CORS_ORIGIN="*"
PORT=3000
```

💡 *Only providers with valid API keys appear in the UI.*

### 4️⃣ Run Locally

```bash
npm run dev
```

👉 Open [http://localhost:3000](http://localhost:3000)

---

## 🚀 Deployment

### ▶ Vercel

1. Push repo → GitHub
2. Import into [Vercel](https://vercel.com)
3. Add `.env` variables in **Project Settings → Environment Variables**
4. Deploy ✅

### ▶ Other Hosting

```bash
npm start
```

---

## 📡 API Reference

**POST** `/api/chat`

**Request:**

```jsonc
{
  "provider": "mistral",
  "model": "mistral-large-latest",
  "system": "You are a helpful assistant",
  "temperature": 0.7,
  "max_tokens": 1024,
  "messages": [
    { "role": "user", "content": "Hello!" }
  ]
}
```

**Response:**

```jsonc
{
  "provider": "mistral",
  "model": "mistral-large-latest",
  "text": "Hi there! How can I help?"
}
```

---

## 🎨 UI Highlights

* 🎯 **Provider Selector** – choose backend instantly
* 🧩 **Model Input Field** – custom model selection
* 🗒 **System Prompt** – define assistant behavior
* 📝 **Markdown Rendering** – clean, formatted AI responses
* ⚙️ **Config Controls** – tweak temperature, tokens
* 🔐 **Security Reminder** – API keys never leave the server

---

## 🛠 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=nodejs,express,js,html,css,vercel,git,github" />
</p>

**Backend**:

* `express` – API server
* `node-fetch` – Provider API calls
* `dotenv` – Env var management
* `compression` – Gzip compression
* `morgan` – HTTP request logging
* `cors` – Cross-origin resource sharing

**Frontend**:

* `marked.js` – Markdown parsing
* `Font Awesome` – Icons
* Custom CSS – Dark responsive UI

---

## 🔐 Security Best Practices

* Keep `.env` **out of version control**
* Restrict **CORS origins** in production
* Never expose API keys in frontend code

---

## 🤝 Contributing

PRs welcome! You can:

* Add support for new AI providers
* Improve UI/UX
* Enhance docs/tests

**Steps:**

1. Fork repo
2. Create branch (`feature/new-feature`)
3. Commit & push
4. Open PR 🎉

---

## 📜 License

MIT © [Harsh Bhardwaj](https://github.com/Harshsfd)
See [LICENSE](LICENSE) for details.

---

## 🌐 Connect

* **GitHub** → [Harshsfd](https://github.com/Harshsfd)
* **Portfolio** → [harshbhardwaj-portfolio.vercel.app](https://harshbhardwaj-portfolio.vercel.app)

```
