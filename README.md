# AI Email Intelligence & Triage

An intelligent n8n workflow that automatically classifies, prioritizes, and organizes your Gmail inbox using Google Gemini AI.

![n8n](https://img.shields.io/badge/n8n-v1.122+-blue?style=flat-square)

## 📋 Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Workflow Overview](#workflow-overview)
- [Security Notes](#security-notes)

## ✨ Features

- **🤖 AI-Powered Classification**: Uses Google Gemini to intelligently classify emails
- **📌 Automatic Labeling**: Applies relevant Gmail labels based on email content
- **⭐ Priority Detection**: Automatically identifies and marks important emails
- **📊 Importance & Urgency Detection**: Analyzes email urgency and importance
- **🗑️ Smart Archiving**: Archives low-value promotional emails to keep inbox clean
- **🔒 Safe & Non-Destructive**: Carefully designed workflow with safety checks
- **⚡ Fully Automated**: Runs automatically on email arrival

## 🔧 Requirements

- **n8n** (v1.122+)
- **Gmail Account** with API access
- **Google Cloud Project** with Gmail API enabled
- **Google Gemini API Key** for AI classification
- **OAuth2 Credentials** for Gmail authentication

## 📦 Installation

### Step 1: Clone Repository

```bash
git clone https://github.com/Chethanreddyc/Email_manager.git
cd Email_manager
```

### Step 2: Import Workflow into n8n

1. Open your n8n instance
2. Go to **Workflows** → **Create New**
3. Import the `workflow.json` file

### Step 3: Configure Credentials

Create and configure the following credentials in n8n:

| Credential | Type | Purpose |
|-----------|------|---------|
| Gmail OAuth2 | OAuth2 | Gmail API access |
| Gemini API Key | API Key | AI classification |

### Step 4: Setup Workflow

1. Assign credentials to their corresponding nodes
2. Create required Gmail labels in your Gmail account
3. Review and adjust workflow rules for your preferences
4. Activate the workflow

## ⚙️ Configuration

### Gmail Labels

Create these labels in Gmail (optional, customize as needed):

- `AI/Important`
- `AI/Promotional`
- `AI/Classified`

### Workflow Parameters

Adjust classification rules and archiving settings in the workflow nodes before activation.

## 🚀 Usage

### Automatic Processing

Once activated, the workflow automatically:

1. **Retrieves** incoming emails from your Gmail inbox
2. **Analyzes** email content using Google Gemini AI
3. **Classifies** emails by category (work, personal, promotional, etc.)
4. **Applies** appropriate Gmail labels
5. **Marks** important/urgent emails with stars
6. **Notifies** Sends telegram notification if action required
7. **Archives** low-priority promotional emails

### Testing

1. Send a test email to your Gmail account
2. The workflow will automatically process it within seconds
3. Check your inbox for applied labels and classifications

## 📊 Workflow Overview

```
Email Received → Retrieve from Gmail → Analyze with Gemini
    ↓
Classify & Score → Apply Labels → Mark Priority → send notification(if required)
    ↓
Organize → Complete
    
```

## 🔐 Security Notes

⚠️ **Important Security Information:**

- **Credentials Not Included**: This repository does not contain any API keys or credentials
- **Replace Credential IDs**: All credential IDs in the workflow use descriptive names (you must assign your actual credentials)
- **Test Carefully**: Review all workflow rules before using with your primary Gmail account
- **Backup Your Data**: Consider backing up important emails before automation runs
- **Monitor Archiving**: Keep an eye on automated archiving to ensure no important emails are missed


## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 💬 Support

For issues or questions, please open a GitHub Issue.
