
# 20AI Malcolm – Ready-to-Deploy (Vercel)

This is a minimal, production-friendly starter to run **Malcolm** (your AI assistant) on **20ai.co.za** using the **OpenAI API**.

## 🛠 What’s included
- `api/chat.js` – serverless function that calls OpenAI
- `public/index.html` – landing page with embedded Malcolm chat
- `.env.example` – copy to `.env` and set `OPENAI_API_KEY`
- `vercel.json` – optional config for Vercel
- `package.json` – minimal (Node 18+ required)

## 🚀 Deploy on Vercel
1. Create a new Vercel project and **import this folder** (or push it to GitHub and import).
2. In Vercel → **Project Settings → Environment Variables**, add:
   - `OPENAI_API_KEY` : your OpenAI key
3. Deploy. Your chat API will be at `/api/chat` and the site at `/`.

## ▶️ Local run (optional)
You can serve `public/index.html` with any static server; the API path `/api/chat` expects a Vercel Serverless runtime.
To test locally with Vercel:
```bash
npm i -g vercel
vercel dev
```
Then open http://localhost:3000

## 🔧 Change model
Open `api/chat.js` and set:
```js
model: 'gpt-4o-mini' // or 'gpt-4o' for maximum quality
```

## 📄 Notes
- The chat widget greets by name if provided.
- The prompt is tuned for small business help and long-form content.
