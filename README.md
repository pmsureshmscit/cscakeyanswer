# 12th CS Key Answer Finder — Static, No API

This version has **no API, no server, no API key, and no billing** — it's a single
static HTML file. Everything runs in the visitor's browser.

## How it works
- Paste (or type) your question paper into the box.
- The app looks up each question against the embedded book-back Q&A material
  (2/3/5 marks, all 16 chapters, English + Tamil).
- **Matched questions** are labelled 📚 *Book Back* and pre-filled with the book's
  answer — you can still edit it.
- **Unmatched questions** (e.g. "write a program...") are labelled ✍️ *Not in
  book — enter manually*, with a blank answer box for you to fill in yourself.
- Click **Edit** on any answer to rewrite it, **Save** to keep it. Saved edits
  are stored in the visitor's own browser (`localStorage`) so they're still
  there next time they open the page on the same device/browser — nothing is
  sent anywhere.

## Deploy on GitHub Pages
1. Push this folder's contents to a GitHub repo (just `index.html` + this
   README at the repo root, or inside `/docs` — your choice).
2. Repo → Settings → Pages → set the source branch/folder.
3. Done — no environment variables, no API key, nothing else to configure.

This will also work unchanged on Vercel, Netlify, or any static host — just
point it at `index.html`, no build step or serverless function required.

## Notes on matching
The matcher ignores common filler words ("define", "what is", "explain", etc.)
so reworded questions still find the right book answer. It's intentionally
conservative about vague/generic questions (like "find the output of the
program") to avoid confidently matching the wrong program's answer — those
will show up as "Not in book" so you can fill them in yourself.
