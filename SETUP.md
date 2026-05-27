# RouteArt — Setup & Publishing Guide

## 1. Create the GitHub Repository

1. Go to **github.com/new**
2. Repository name: `routeart`
3. Description: `Turn GPS tracks into beautiful poster art — GPX Poster Studio`
4. Set to **Public**
5. ✅ Add a README (we'll replace it)
6. License: **MIT**
7. Click **Create repository**

---

## 2. Push the Files

```bash
# Clone your new repo
git clone https://github.com/ehrenholm/routeart.git
cd routeart

# Copy the app file (rename to index.html for GitHub Pages)
cp /path/to/routeart.html index.html
cp /path/to/README.md README.md

# Commit and push
git add .
git commit -m "🚀 Initial release: RouteArt GPX Poster Studio v1.0.0"
git push origin main
```

---

## 3. Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / `/ (root)`
4. Click **Save**
5. Wait ~2 minutes → your site is live at:
   **`https://ehrenholm.github.io/routeart`**

---

## 4. Set Up Ko-fi (10 minutes)

Ko-fi is the best option for a tool like this:
- **0% platform fee** (only Stripe/PayPal ~2.9% payment processing)
- No subscription required
- Works globally
- Simple "Buy me a coffee" or custom amounts

### Steps:
1. Go to **[ko-fi.com](https://ko-fi.com)** → Create Account
2. Username: `ehrenholm` (to match the links already in the app)
3. Set up your page — add a photo, short description, goal if you want
4. Connect Stripe or PayPal for payouts
5. Done! Your page is live at `ko-fi.com/ehrenholm`

The app already has your Ko-fi button in the header — no code changes needed.

---

## 5. Set Up GitHub Sponsors (optional, for developer audience)

GitHub Sponsors shows up on your profile and repo — good for devs who find the project.

1. Go to **github.com/sponsors** → Join the waitlist / Apply
2. Requires: bank account, W-8/W-9 tax form
3. Once approved: a ❤️ Sponsor button appears on your repo
4. Takes 1-2 weeks to get approved

GitHub takes **0% fee** — you keep everything minus payment processing.

---

## 6. Add a Custom Domain (optional)

If you have a domain like `routeart.io`:

1. In GitHub Pages settings → **Custom domain** → enter your domain
2. At your DNS provider, add:
   ```
   CNAME  www  ehrenholm.github.io
   A      @    185.199.108.153
   A      @    185.199.109.153
   A      @    185.199.110.153
   A      @    185.199.111.153
   ```
3. ✅ Enforce HTTPS

---

## 7. Using Claude Code for Development

Once the repo is on your machine:

```bash
# Install Claude Code
npm install -g @anthropic-ai/claude-code

# Enter the project
cd routeart

# Start a session
claude

# Example prompts:
# "Add a dark/light mode toggle to the header"
# "Fix the lap detection for tracks shorter than 5km"
# "Add a share button that generates a URL with settings encoded"
```

Claude Code reads and edits your files directly — no copy-pasting needed.

---

## 8. Promotion Ideas

- **Strava community groups** — cyclists, runners, triathletes love this kind of tool
- **Reddit**: r/running, r/cycling, r/MTB, r/Strava, r/DataIsBeautiful
- **Product Hunt** — launch as a "maker" project
- **GitHub Awesome lists** — submit to awesome-gpx, awesome-maps
- Tweet/post with a sample poster image — visual tools spread well

---

## Update Workflow

When you make changes:

```bash
# Edit index.html with Claude Code or manually
claude  # "Fix X" or "Add feature Y"

# Deploy
git add index.html
git commit -m "✨ Add [feature] / 🐛 Fix [bug]"
git push origin main
# GitHub Pages auto-deploys in ~60 seconds
```

---

## File Structure

```
routeart/
├── index.html      # The entire app (single file)
├── README.md       # GitHub repo page
├── LICENSE         # MIT
└── SETUP.md        # This file (you can delete after setup)
```
