# GitHub Pages Setup Instructions

Your OSU Social Work PhD FAQ app is ready, but needs one manual step to go live.

## ⚠️ Current Issue
The GitHub Actions workflow failed because GitHub Pages needs to be enabled in repository settings first.

## ✅ How to Fix (2 steps, 2 minutes):

### Step 1: Enable GitHub Pages
1. Go to: https://github.com/jyelee2021/Test/settings/pages
2. Under "Build and deployment":
   - Change **Source** from "None" to **GitHub Actions**
   - Click **Save**

### Step 2: Re-run the Workflow
1. Go to: https://github.com/jyelee2021/Test/actions
2. Click on the failed **"Deploy to GitHub Pages"** workflow run
3. Click the **"Re-run all jobs"** button
4. Wait ~30 seconds for it to complete

## 🌐 Your Live Link
Once deployed, your FAQ will be live at:
```
https://jyelee2021.github.io/Test/
```

## 🎓 FAQ Preview
The page includes:
- 🔍 Search across all questions
- 📑 Filter by category (Requirements, Application, Timeline, Other)
- 16 common admission questions
- Direct contact info for the PhD coordinator

## 📝 To Edit the FAQs
Simply edit `index.html`, update the `faqData` array, commit, and push — it will auto-deploy!

---

**Questions?** Contact: Jennifer Nakayama at nakayama.7@osu.edu or (614) 292-6188
