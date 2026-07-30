# AI Policy Explorer

A tool to help faculty draft a course-level AI use policy. It lists prohibited and allowed generative-AI uses drawn live from a shared Google Sheet, lets faculty check off the ones relevant to their course, and assembles the selections into policy language they can copy into a syllabus.

**Live site:** https://mlittmancs.github.io/ai-policy-explorer/

## How it works

- `index.html`, `styles/`, `scripts/` make up the whole site — no build step, no server.
- Prohibited uses, allowed uses (with guardrails), and the syllabus boilerplate text are fetched live from a Google Sheet at page load, so editing the sheet updates the tool without a code change. See `scripts/ai-policy-explorer.js` for the expected tab names and column layout.
- If the live fetch fails, the page falls back to a bundled snapshot (`scripts/ai-policy-explorer-fallback-data.js`) and shows a banner saying so.

## Development

Serve the directory locally and open `index.html`, e.g.:

```
python3 -m http.server 8000
```

GitHub Pages serves this repo's `main` branch at the live URL above.
