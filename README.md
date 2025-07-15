# AI-Powered Email Summarizer for WhatsApp

This project demonstrates an automated workflow built in Zapier that uses Google's Gemini AI to parse, summarize, and send notifications for specific emails.

**Submitted for the AI Automation Expert role at Zapier.**

---

## 🚀 Use This Zap

You can install and use this exact workflow template by clicking the link below.

**[Click here to use this Zap!]((https://zapier.com/shared/abd846ad3c69da3375832de210008a7d92e4f353))**

---

## 🛠️ Workflow Breakdown

### 1. Trigger: New Email in Gmail
* **Event:** New Email (matching a search)
* **Details:** The workflow triggers when an email with the subject "Google Agentic AI Day" arrives. This method is efficient for filtering specific event notifications.

### 2. Action: Conversation in Google AI Studio (Gemini)
* **Event:** Conversation
* **Rationale:** The core of the automation. I chose the `gemini-2.0-flash` model for its balance of speed and text comprehension, which is ideal for this kind of notification task.
* **System Prompt Strategy:** The system prompt is engineered for consistency and reliability.
    ```
    You are an expert at creating concise and friendly notifications for WhatsApp. Your task is to take the content of an email and turn it into a short, clear message. Start the message with "New AI Event Update:".
    ```
    This prompt establishes a clear role for the AI and a strict output format, minimizing errors and ensuring a predictable result for the final step.

### 3. Action: Send Message in WhatsApp
* **Event:** Send Message
* **Details:** This step takes the clean, formatted **response** from the Gemini step and sends it directly to a specified WhatsApp number, completing the automation.
