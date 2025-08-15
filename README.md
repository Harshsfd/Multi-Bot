# 🚀 Multi-Bot

A **sleek**, **multi-provider AI chat application** with a unified browser interface.  
Supports **OpenAI**, **Groq**, **Mistral**, **Anthropic**, **Gemini**, and **xAI** — all while keeping API keys **safe on the server** (never exposed to the browser).  

🔗 **[Live Demo »](https://multi-bot-fawn.vercel.app)**

---

## ✨ Features

✅ **Provider-agnostic** – Switch between multiple AI providers effortlessly.  
🔒 **Secure API key handling** – Managed **server-side** via `.env`.  
📝 **Markdown support** – Rich text, syntax-highlighted code blocks via **Marked.js**.  
⚡ **Snappy UX** – Dark mode, compression, and HTTP logging for smooth performance.  
☁️ **Deployment-ready** – Works out-of-the-box on **Vercel** or any Node.js host.  

---

## 📂 Project Structure

```

Multi-Bot/
│
├── public/                 # Client-side app
│   ├── index.html          # Chat interface
│   ├── styles.css          # Dark-theme styling
│   └── app.js              # Chat UI logic
│
├── server.js               # Express backend with provider integrations
├── package.json            # Scripts & dependencies
├── vercel.json             # Vercel config
└── .env                    # Environment variables (ignored in git)

````

---

## 🛠 Getting Started

### 1️⃣ Prerequisites
- **Node.js** (v16+ recommended)
- **npm**

### 2️⃣ Installation
```bash
git clone https://github.com/Harshsfd/Multi-Bot.git
cd Multi-Bot
npm install
````

### 3️⃣ Configure Environment

Create a `.env` file in the root:

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

💡 *Only providers with valid API keys will appear in the UI.*

### 4️⃣ Run Locally

```bash
npm run dev
```

Then open **[http://localhost:3000](http://localhost:3000)** in your browser.

---

## 🚀 Deployment

### ▶ Deploy on Vercel

1. Push your repo to GitHub.
2. Import into [Vercel](https://vercel.com).
3. Add your environment variables in **Settings → Environment Variables**.
4. Deploy — done! ✅

### ▶ Other Hosting

Any Node.js hosting will work:

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

## 💻 UI Highlights

🎯 **Provider Selector** – Switch AI backends instantly.
🧩 **Model Input Field** – Flexible model selection.
🗒 **System Prompt** – Customize assistant behavior.
🎨 **Markdown Rendering** – Beautiful, formatted AI responses.
⚙ **Config Controls** – Adjust temperature & max tokens.
💡 **Security Reminder** – API keys never leave your server.

---

## 🏗 Tech Stack

**Backend**:

* `express` – Web server
* `node-fetch` – API calls
* `dotenv` – Env vars
* `compression` – Faster responses
* `morgan` – HTTP logging
* `cors` – Cross-origin handling

**Frontend**:

* `marked.js` – Markdown parsing
* `Font Awesome` – Icons
* Custom CSS – Dark theme + responsive layout

---

## 🔐 Security Best Practices

* Keep `.env` out of version control.
* Restrict **CORS** in production.
* Never embed API keys in frontend code.

---

## 🤝 Contributing

PRs are welcome!
You can:

* Add new AI providers
* Enhance UI/UX
* Improve docs or testing

**Steps:**

1. Fork the repo
2. Create a new branch
3. Make changes & commit
4. Open a Pull Request 🎉

---

## 📜 License

MIT © [Harsh Bhardwaj](https://github.com/Harshsfd)
See [LICENSE](LICENSE) for details.

---

## 🌐 Connect

* **GitHub**: [Harshsfd](https://github.com/Harshsfd)
* **Portfolio**: [harshbhardwaj](https://harshbhardwaj-portfolio.vercel.app)
