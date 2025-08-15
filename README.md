#  Multi-Bot

A sleek, multi-provider AI chat application with a unified browser interface. Supports chat across OpenAI, Groq, Mistral, Anthropic, Gemini, and xAI, while keeping all API keys securely on the server (never exposed in the browser).

[Live Demo](https://multi-bot-fawn.vercel.app)

---

##  Features

- **Provider-agnostic interface** — Choose from OpenAI, Groq, Mistral, Anthropic, Gemini, or xAI.
- **Secure API key handling** — All API keys are managed server-side via `.env`.
- **Markdown support** — Rich text formatting and syntax-highlighted code snippets using Marked.js.
- **Snappy UX** — Responsive UI with a modern dark theme, compression, and HTTP logging for smooth performance.
- **Ready for deployment** — Configured for deployment on Vercel or any other Node.js hosting platform.

---

##  Project Structure

Multi-Bot/
│
├── public/                 # Client-side app
│   ├── index.html          # Chat interface
│   ├── styles.css          # Dark-theme styling
│   └── app.js              # Chat UI logic
│
├── server.js               # Express backend with modular provider support
├── package.json            # Scripts and dependencies
├── vercel.json             # Vercel deployment config
└── .env                    # Environment variables (.gitignored)

---

##  Getting Started

### Prerequisites

Make sure you have **Node.js** and **npm** installed.

### Installation

```bash
git clone https://github.com/Harshsfd/Multi-Bot.git
cd Multi-Bot
npm install
```

### Setup Environment Variables

Create a `.env` in the project root:

```env
OPENAI_API_KEY="YOUR_OPENAI_KEY"
GROQ_API_KEY="YOUR_GROQ_KEY"
MISTRAL_API_KEY="YOUR_MISTRAL_KEY"
ANTHROPIC_API_KEY="YOUR_ANTHROPIC_KEY"
GEMINI_API_KEY="YOUR_GEMINI_KEY"
XAI_API_KEY="YOUR_XAI_KEY"

# Optional:
CORS_ORIGIN="*"    # Adjust in production
PORT=3000
```

> Only providers with valid API keys will be enabled by the UI.

### Run Locally

```bash
npm run dev
```

Visit: `http://localhost:3000`

---

## Deployment

### Deploy via Vercel

1. Push the repo to your GitHub (or fork it if desired).
2. Import the project on [Vercel](https://vercel.com).
3. Configure your Environment Variables under *Project Settings → Environment Variables*.
4. Deploy — it’s ready out of the box with `vercel.json`.

### Other Options

For any Node.js environment or hosting provider:

```bash
npm start
```

---

## API Reference

### `POST /api/chat`

* **Request Body**:

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

* **Response**:

  ```jsonc
  {
    "provider": "mistral",
    "model": "mistral-large-latest",
    "text": "Hi there! How can I help?"
  }
  ```

---

## UI Highlights

* **Provider Selector** – Choose your AI backend.
* **Model Input Field** – Easily specify model names.
* **Optional System Prompt** – Prime the assistant’s behavior.
* **Temperature & Max Tokens** – Control response creativity and length.
* **Chat History** – Markdown-rendered responses with code styling.
* **Pro Tip Footer** – Reminds you to never expose your API keys.

---

## Tech Stack

* **Backend**:

  * `express` — Lightweight Node.js server
  * `node-fetch` — HTTP client for provider APIs
  * `dotenv` — Env var management
  * `compression` — Response compression
  * `morgan` — HTTP request logging
  * `cors` — Cross-origin access control

* **Frontend**:

  * `marked.js` — Markdown parsing
  * `Font Awesome` — Icons for UI
  * CSS variables and dark theme styling

---

## Security Best Practices

* Never expose API keys in client-side code or version control.
* Use secure CORS policies in production.
* Keep `.env` in `.gitignore` and limit access to sensitive keys.

---

## Contributing

Contributions are welcome! Feel free to:

* Add new AI providers or streamline existing integrations.
* Enhance UI/UX or expand chat features.
* Improve documentation, error handling, or test coverage.

Please open issues or pull requests—happy to collaborate!

---

## License

Licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## Connect with Me

* [GitHub](https://github.com/Harshsfd)
* [Portfolio](https://harshbhardwaj-portfolio.vercel.app)

---

**Why this README works:**

* Clear structure with headings for navigation (`Features`, `Setup`, `Usage`, `Contributing`).
* Unique touches like the API example and tech stack outline developer expectations.
* It’s deployment-ready and user-friendly—whether someone clones it locally or hits “Deploy” on Vercel.
