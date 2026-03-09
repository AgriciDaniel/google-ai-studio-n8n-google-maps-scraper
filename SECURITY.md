# Security Policy

## Reporting a Vulnerability

Open a [GitHub Security Advisory](https://github.com/AgriciDaniel/google-ai-studio-n8n-google-maps-scraper/security/advisories/new) on this repo or contact the maintainer directly.

## Supported Versions

Only the latest version receives security updates.

## Credential Handling

Workflow JSON files use **placeholder values** for webhook IDs and API credentials. Before importing into n8n:

1. Replace `YOUR-WEBHOOK-ID-HERE` with your own webhook ID
2. Configure your own Google AI Studio and Google Sheets OAuth credentials in n8n's credential store
3. Never commit real API keys, webhook UUIDs, or passwords to this repository
