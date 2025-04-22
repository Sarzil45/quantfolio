
# 🔄 Quantfolio Update Guide

This guide shows you how to update your Quantfolio site — locally and safely — without needing to manually re-upload anything.

---

## ✅ How to Add a New Project

1. Go to: `content/projects/`
2. Duplicate an existing `.json` file (like `black-scholes.json`)
3. Edit the fields:
    - `slug`: used for the project URL
    - `title`, `shortDescription`, `longDescription`
    - `renderType`: `"embed"` or `"external"`
    - `embedUrl` or external URL
    - `tags`: for filtering
    - `featured`: set `true` if you want it on the homepage
4. Save the file
5. Commit & push:

```bash
git add .
git commit -m "Added new project: [Project Name]"
git push
```

---

## 📘 How to Add a New Blog or Video

1. Go to `content/standalone/` or `content/series/[your-series-name]/`
2. Copy an existing `.md` file
3. Edit the **frontmatter** at the top:
```md
---
title: "Your Post Title"
slug: "your-post-slug"
type: "article" or "video"
youtubeId: "VIDEO_ID" (if type is video)
tags: ["quant", "tutorial"]
series: "series-name" (or null)
thumbnail: "/images/post.png"
featured: true (optional)
---
```
4. Add your content below the frontmatter
5. Commit & push

---

## 🛠 Common Git Commands

| Action | Command |
|--------|---------|
| Save changes | `git add .` |
| Write a message | `git commit -m "your message"` |
| Push to live site | `git push` |
| See status | `git status` |

---

## 🧪 Preview Your Site Locally

```bash
npm run dev
```
Then visit: http://localhost:4321

---

## 🚀 Deployment

When you push to GitHub, Netlify automatically:
- Pulls the code
- Builds the site
- Deploys to your `.netlify.app` URL

---

# You’re good to go!
