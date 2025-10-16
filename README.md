# AI News RSS Feed Demo

This is a **live working demo** of an automated AI news aggregation system.

## What This Demo Shows

- **17 Google Alert RSS feeds** aggregating AI news from multiple sources
- **Automatic categorization** into 17 topic areas (Business, Tech, OpenAI, etc.)
- **Updates every 3 hours** via GitHub Actions
- **Generates JSON** that can be consumed by any website
- **Zero infrastructure costs** - runs entirely on GitHub's free tier

## Live Demo

Once GitHub Pages is enabled, the news data will be available at:
```
https://jaystarz1.github.io/chatbotgenius-rss-feed-demo/data/news.json
```

## How It Works

1. **GitHub Actions** runs every 3 hours (or manually)
2. Fetches articles from 17 RSS feeds (Google Alerts for AI topics)
3. Parses and cleans the articles
4. Categorizes each article using keyword matching
5. Removes duplicates and sorts by date
6. Saves top 100 articles to `data/news.json`
7. Website loads this JSON and displays the news

## Categories

The demo automatically categorizes articles into:
- **Companies:** Microsoft, Meta, OpenAI, NVIDIA, Y Combinator
- **Topics:** Business, HR, Jobs, Tech, ML, Ethics, Privacy, Security, Policy, Legal, Healthcare, Education, Stocks
- **General:** Anything that doesn't match other categories

## Files in This Demo

- `.github/workflows/update-news.yml` - The automation workflow
- `data/news.json` - Generated news data (created by workflow)
- `test-page.html` - Standalone demo page to test the feed
- `README.md` - This file

## Setup Instructions

### Step 1: Enable GitHub Pages
1. Go to repo **Settings**
2. Click **Pages** (left sidebar)
3. Source: Deploy from `main` branch
4. Click **Save**
5. Wait 1-2 minutes for deployment

### Step 2: Run Workflow Manually
1. Go to **Actions** tab
2. Click "Update AI News Feed"
3. Click "Run workflow" button
4. Wait 1-2 minutes
5. Check if `data/news.json` was created

### Step 3: Test It
Open `test-page.html` in a browser, or visit:
```
https://jaystarz1.github.io/chatbotgenius-rss-feed-demo/test-page.html
```

You should see AI news articles loading with category filters.

## For Rapidfire Web

This demo shows exactly how the system would work for your clients:

1. Each client gets their own repo (like this one)
2. Configured with RSS feeds for their industry
3. Categories customized to their topics
4. Updates automatically
5. They integrate into Webflow with simple HTML/JS

**See `FOR-RAPIDFIRE/` folder for:**
- Test instructions
- Webflow integration code
- Explanation of what's happening

## Technical Details

- **Cost:** $0/month (GitHub Actions free tier: 2,000 minutes/month, this uses ~120)
- **Update frequency:** Every 3 hours (configurable)
- **Article limit:** 100 most recent (configurable)
- **Categories:** 17 + General (customizable)
- **No backend server needed** - it's just static JSON
- **Works with any website** - Webflow, WordPress, custom HTML

## Questions?

Contact: Jay Tarzwell
- Website: https://thechatbotgenius.com
- Email: [your email]

---

**Built with Claude Code** by Anthropic
