# Sleeping-Beauty-Demo-UI
Custom chat interface for an AI bot 
# SMS AI Demo - Reactivation Campaign Chatbot

A demo tool that simulates AI-powered SMS conversations for client reactivation campaigns. Built with an iMessage-style interface so you can show clients exactly how the AI would text their leads.

![SMS Demo Screenshot](screenshot.png)

## What This Does

- **iMessage-style chat interface** - Looks like a real text conversation
- **Customizable AI personality** - Set system message and context
- **Live AI responses** - Powered by OpenAI's GPT
- **Typing indicator** - Shows realistic "..." when AI is responding
- **Perfect for demos** - Show clients how AI reactivation campaigns work

---

## Quick Start (15 minutes)

### Step 1: Get an OpenAI API Key

1. Go to [platform.openai.com](https://platform.openai.com)
2. Sign up or log in
3. Go to **API Keys** (left sidebar)
4. Click **"Create new secret key"**
5. Copy the key (starts with `sk-`)
6. Add some credits ($5-10 is plenty for demos)

### Step 2: Deploy to Render (Free)

1. **Fork this repo** to your own GitHub account

2. Go to [render.com](https://render.com) and sign up with GitHub

3. Click **"New" → "Web Service"**

4. Select this repo from the list

5. Configure the service:
   - **Name:** `your-demo-name` (this becomes your URL)
   - **Region:** Choose closest to you
   - **Branch:** `main` or `master`
   - **Build Command:** `npm install`
   - **Start Command:** `node server.js`

6. Add Environment Variable:
   - Click **"Add Environment Variable"**
   - **Key:** `OPENAI_API_KEY`
   - **Value:** *(paste your OpenAI API key)*

7. Select **Free** tier

8. Click **"Create Web Service"**

9. Wait 1-2 minutes for deployment

10. Your demo is live at `https://your-demo-name.onrender.com`

---

## How to Use

1. **Open the sidebar** (hamburger menu, top-left)

2. **Configure the AI:**
   - **Business Name** - The company name (shows in chat header)
   - **Customer Name** - The lead's name (AI uses this to personalize)
   - **System Message** - AI personality, tone, and rules
   - **Prompt/Context** - Customer details, services, promos, appointment slots

3. **Click "Apply & Start New Chat"** - AI sends the first outreach message

4. **Type responses** as the customer to demo the conversation

---

## Customization Examples

### System Message (Personality & Rules)
```
You are a friendly SMS assistant for [Business Name], reaching out to past customers.

Your goal is to:
- Be warm, professional, and concise (SMS style)
- Remind them it's been a while since their last service
- Offer a special discount for returning customers
- Try to book an appointment

Keep messages under 160 characters. Be conversational, not salesy.
```

### Prompt/Context (Knowledge Base)
```
Customer Info:
- Last service: March 2024 (AC tune-up)
- Equipment: Carrier central AC

Current Promotions:
- 15% off tune-ups for returning customers
- Free inspection with any repair

Available appointments:
- Tuesday 2-4pm
- Thursday 10am-12pm
```

---

## Running Locally (Optional)

If you want to run it on your computer instead of deploying:

1. Clone the repo
2. Run `npm install`
3. Create a `.env` file:
   ```
   OPENAI_API_KEY=your-key-here
   ```
4. Run `node server.js`
5. Open `http://localhost:3000`

---

## Tech Stack

- **Backend:** Node.js + Express
- **AI:** OpenAI GPT-4o-mini
- **Frontend:** Vanilla HTML/CSS/JS
- **Styling:** iMessage-inspired design

---

## Cost

- **Render hosting:** Free tier
- **OpenAI API:** ~$0.01-0.05 per demo conversation (very cheap)

---

## Questions?

Built for the Flexxable community. If you have questions, drop them in the group!
