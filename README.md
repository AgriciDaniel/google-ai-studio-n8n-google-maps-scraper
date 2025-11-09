# No-Code Google Maps Scraper with Google AI Studio & n8n

A no-code Google Maps lead scraper built with Google AI Studio (Gemini) and automated with n8n. This repository contains the n8n workflow JSON and all the resources from the full video tutorial.

**Watch the full step-by-step tutorial on YouTube:**
**https://www.youtube.com/watch?v=qBHubb2inaQ&t**

## Overview

This project demonstrates a powerful, no-code stack for building and automating custom AI applications.

  * **Google AI Studio** is used to "vibe code" an application using natural language prompts.
  * **n8n** acts as the powerful automation bridge, connecting the AI app to any other service.
  * **Google Sheets** is used as the database to store the structured data.

### How It Works

The data flow is simple:

1.  A user runs the app in **Google AI Studio**.
2.  Google AI Studio gathers the data and sends it via a `POST` request to a **n8n Webhook**.
3.  The **n8n workflow** catches the data, splits it into individual items, formats it, and appends each item as a new row in **Google Sheets**.

`[Google AI Studio App] --- (Webhook POST) ---> [n8n Workflow] --- (Append Row) ---> [Google Sheets]`

## Features

  * **No Code Required:** Build the entire application with natural language and visual workflow automation.
  * **Flexible & Scalable:** Easily modify the prompt in AI Studio to scrape different data, or change the n8n workflow to send data to a CRM, WordPress, or 400+ other apps.
  * **100% Free to Start:** All tools used in this tutorial have generous free tiers.

## 🚀 Getting Started

Follow these steps to get your own scraper running in minutes.

### 1\. Prerequisites

  * A free **Google Account**
  * A free **n8n** account (Cloud or self-hosted)

### 2\. Step 1: Set up Google AI Studio

1.  Open the Google AI Studio App Template:
    `https://aistudio.google.com/apps/drive/1aVOVu_Ij8r5xeTJnrc7pCLUITH3t6F-m`
2.  Make a copy of the app in your own Google Drive.
3.  You may need to get a Gemini API key (`Get API key` in Google AI Studio) and add it to the app.

### 3\. Step 2: Set up Google Sheets

1.  Open the Google Sheets Template:
    `https://docs.google.com/spreadsheets/d/1mOy9gQ6I_x3t5xXwZ9Fog9aMC2FGfgcq5QtbM146ua8/edit?usp=sharing`
2.  Go to `File` \> `Make a copy` to save it to your own Google Drive.

### 4\. Step 3: Set up the n8n Workflow

1.  **Download** the `google-ai-studio-scraper.n8n.json` file from this repository.
2.  **Import** the workflow into your n8n instance.
3.  **Configure the Google Sheets Node:**
      * Open the "Google Sheets" node in the workflow.
      * Create new credentials (OAuth2) and connect the Google Account where you saved your sheet in Step 2.
      * In the "Sheet" field, select the Google Sheet you just created.
4.  **Copy Your Webhook URL:**
      * Open the "Webhook" node (the first node).
      * Copy the **Production URL**.

### 5\. Step 4: Connect AI Studio to n8n

1.  Go back to your app in **Google AI Studio**.
2.  Find the part of the prompt that defines the webhook URL.
3.  **Paste** your n8n Production Webhook URL there.
4.  Save the changes to your AI Studio app.

### 6\. Step 5: Activate and Run\!

1.  **Activate** your workflow in n8n (toggle the switch on the top right).
2.  Run your app in Google AI Studio.
3.  Watch the data appear in your Google Sheet in real-time\!

## Resources

  * **Full Video Tutorial:** [https://youtu.be/qBHubb2inaQ](https://www.google.com/search?q=https://youtu.be/qBHubb2inaQ)
  * **n8n:** [https://n8n.io](https://n8n.io)
  * **Google AI Studio:** [https://aistudio.google.com](https://aistudio.google.com)

## License

This project is open-sourced under the MIT License. See the [LICENSE](https://www.google.com/search?q=LICENSE) file for more details.
