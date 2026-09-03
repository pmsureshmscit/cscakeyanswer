# 12th CS Key Answer — Vercel Deployment

## Deploy Steps

### 1. Push to GitHub
Push this entire `cs_vercel/` folder as a GitHub repo.

### 2. Connect to Vercel
1. Go to https://vercel.com → New Project
2. Import your GitHub repo
3. Framework Preset: **Other**
4. Root Directory: *(leave blank)*
5. Click Deploy

### 3. Add API Key (Environment Variable)
1. Vercel Dashboard → Your Project → Settings → Environment Variables
2. Add:
   - Name:  `GEMINI_API_KEY`
   - Value: `AIzaSyxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx` (get one free at [Google AI Studio](https://aistudio.google.com/apikey))
   - Environment: Production + Preview + Development
3. Redeploy once after adding the key

### Done!
Your app is live at `https://your-project.vercel.app`
API key is hidden server-side — users never see it.
