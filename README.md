# 📌 BBC Tech News Automation

This workflow automatically fetches **technology news** from BBC RSS
feed, sends it to a **Telegram channel**, and saves a copy into a
**Google Sheet** for reference.

------------------------------------------------------------------------

## 🔧 Workflow Components

### 1️⃣ **RSS Feed**

-   Source: [BBC Technology
    RSS](https://feeds.bbci.co.uk/news/technology/rss.xml)\
-   Fetches the latest technology news items (title, link, publish date,
    description).\
-   Optional filter: Match only items related to **AI / Machine Learning
    / Robotics** etc. using regex.

------------------------------------------------------------------------

### 2️⃣ **Telegram Bot**

-   Module: **Send a Message**\

-   Sends each fetched news item into the channel:\
    **Channel Name**: `BBC Tech News`\

-   Message format used:

        💡 Tech Today:

        📰 {{1.title}}
        📎 Details: {{1.url}}
        🗓️ Published on: {{1.rssFields.pubdate}}

-   News gets delivered instantly to subscribers.

------------------------------------------------------------------------

### 3️⃣ **Google Sheets**

-   Each news item is also logged into a Google Sheet.\
-   Stored fields:
    -   **Title**\
    -   **URL**\
    -   **Published Date**\
-   Purpose: keep a historical archive of all news to review later.

------------------------------------------------------------------------

## 📂 Scenario Structure (in Make.com)

    RSS Feed → Telegram Bot (Send Message) → Google Sheets (Add Row)

------------------------------------------------------------------------

## 🚀 Usage

1.  Add your **Telegram Bot Token** in Make.\
2.  Link your **Google Sheets account**.\
3.  Activate the scenario.\
4.  News will start flowing automatically every time a new article is
    published.

------------------------------------------------------------------------

## ✅ Benefits

-   Instant delivery of BBC tech news to your Telegram audience.\
-   Automatic backup of all news in Google Sheets for later use.\
