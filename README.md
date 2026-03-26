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
3. Complete the steps (base image description, framing, platform size, background style, etc.).
4. **Generate prompt** → copy or download the `.txt` block for your image model.

Optional: save a **Google AI Studio** API key in the page to auto-describe the base image via Gemini (stored only in your browser). You can always type the description manually.

## License

See [LICENSE](LICENSE) (MIT).
