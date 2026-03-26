# SAI 🎓

Upload any course syllabus and instantly get a clean schedule of every lecture, assignment, exam, and project — with deadline reminders.

**Free for students. No account needed.**

---

## Deploy in 5 minutes (free)

### 1. Get an Anthropic API Key
- Go to [platform.anthropic.com](https://platform.anthropic.com)
- Sign up and create an API key
- This is YOUR key — it stays secret on the server, students never see it

### 2. Push this repo to GitHub
```bash
git init
git add .
git commit -m "initial commit"
git remote add origin https://github.com/YOUR_USERNAME/sai.git
git push -u origin main
```

### 3. Deploy to Netlify (free)
- Go to [netlify.com](https://netlify.com) and sign up free
- Click **"Add new site"** → **"Import an existing project"**
- Connect your GitHub and select this repo
- Click **Deploy site**

### 4. Add your API key (secret)
- In Netlify dashboard → **Site settings** → **Environment variables**
- Click **Add a variable**
- Key: `ANTHROPIC_API_KEY`
- Value: your `sk-ant-...` key
- Click **Save** and **Redeploy**

That's it! Your site is live and free for any student to use. 🚀

---

## How it works

- Students upload a PDF or paste their syllabus text
- Your serverless function (hidden from users) calls the Claude API
- Claude extracts all dates, assignments, exams, and lectures
- Students get a clean color-coded schedule with deadline reminders

## Cost

Analyzing one syllabus costs roughly **$0.01**. For 1,000 students that's ~$10/month. Anthropic gives new accounts $5 free to start.

## Project structure

```
index.html                  ← the entire frontend app
netlify/functions/analyze.js ← serverless function (holds your API key)
netlify.toml                ← routes /api/analyze to the function
```
