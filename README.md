# Food image prompt generation tool

A small browser-based wizard that builds **detailed, Gemini-friendly prompts** for editing food and restaurant photos (delivery banners, social posts, menus). It also includes a **markdown spec** for a conversational “prompt engineer” workflow.

## Files

| File | Purpose |
|------|--------|
| `food-image-edit-prompt.html` | Open in a browser: step-through form → copy/download the generated prompt |
| `food-image-edit-workflow.md` | Full workflow text for AI assistants building the same kind of prompts in chat |

## Usage

1. Clone or download this repo.
2. Open `food-image-edit-prompt.html` in a modern browser (double-click or serve locally).
3. Complete the steps (base image description, framing, platform size, background style, enhancements, etc.).
4. **Generate prompt** → copy or download the `.txt` block for your image model.

The generated prompt includes **anti-clutter** composition rules and **output clarity / sharpness** instructions (including for slightly soft or low-res sources). In Step 6 you can optionally tick **Extra clarity & crisp detail** for stronger emphasis.

Optional **Google AI Studio** API key (stored only in your browser): auto-describe the base image after upload, and on the last step run **Prompt readiness review** to have Gemini sanity-check the prompt (and optional image) before you edit.

## Deploy on Railway

This repo is a **static site** served with [`serve`](https://github.com/vercel/serve) so Railway can bind `PORT` like any Node app.

1. Push this repo to GitHub (already set up for most users).
2. In [Railway](https://railway.app): **New project** → **Deploy from GitHub repo** → select `Food-Image-prompt-generation-tool`.
3. Railway will detect `package.json` and run **`npm install`** then **`npm start`**.
4. Open the generated **public URL** — you should land on the prompt builder (`index.html` redirects to `food-image-edit-prompt.html`).

**Gemini API from the browser:** Your key stays in the visitor’s browser (`localStorage`). Ensure your Railway URL uses **HTTPS** (Railway provides this by default). If `fetch` to Google fails, check API key restrictions in Google AI Studio (HTTP referrer / domain allowlist) and allow your Railway domain.

Local preview: `npm install` then `npm start` (or `npm run dev` on port 3000).

## License

See [LICENSE](LICENSE) (MIT).
