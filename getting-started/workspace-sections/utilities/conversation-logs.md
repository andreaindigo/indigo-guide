---
icon: comment-lines
---

# Conversation Logs

### How to track and analyze chatbot interactions

## 📌 Overview

Conversation Logs provide a centralized place in the indigo.ai platform where you can view the full list of chatbot conversations and their corresponding Evaluator results.\
This section allows teams to **analyze every single conversation,** understand how evaluators and guardrails performed, and start any necessary debugging flows.

## ✅ Benefits

* Detailed visibility → review all conversations in one place, with full evaluator and guardrail outcomes.
* Operational efficiency → quickly identify issues, user feedback, or API errors without switching tools.
* Debug-ready → inspect conversations in detail, including errors and triggers, to improve the chatbot’s performance.

## 💬 What is a Conversation Log?

A Conversation Log represents one interaction between a chatbot and an end-user.

* A conversation begins when the user starts the chat and ends when they click Close Chat.
* Multiple conversations together form a chat.
* In the Conversation Logs view, you can browse the list of conversations and check how evaluators and guardrails performed for each one.

## ⚙️ How to access and use Conversation Log

You can find Conversation Logs in the Indigo.ai platform under the Utilities section of the left-hand menu.

<figure><img src="../../../.gitbook/assets/conversation log 3.png" alt=""><figcaption></figcaption></figure>

### Available features

* Add Filter → filter conversations by properties such as Username, Messages, Session Duration, and more.
* Date filter → choose the time range of conversations (e.g., Today, From the beginning, custom ranges).
* Export → download the filtered list of logs as a CSV file for external analysis or reporting.

💡**Tip**: Combine property filters with date ranges to quickly isolate relevant conversations (e.g., all production conversations from the past week where API errors occurred).

## 📂 Logs list

Each row in the logs list corresponds to a single conversation.\
Columns display both **conversation properties** and **Evaluator outcomes**.

### Conversation properties

* **Username** → the identifier of the user who started the conversation.
* **First Message** → the first message sent by the user.
* **Messages** → total number of messages exchanged.
* **Date** → date and time the conversation started.
* **Session Duration** → total duration of the conversation.
* **Source** → environment where the conversation took place (e.g., Production or Testing).

### User feedback

* **User Feedback** → 👍 or 👎 provided by the user (zero, one, or multiple feedback items).
* **CSAT** (Customer Satisfaction Score) → numerical rating of user satisfaction (e.g., 1/5, 3/5).
* **API Errors** → number of API errors during the conversation (with details available in the log view).

### Evaluator results

There is one column for each evaluator output:

* **Score** → 1–10, with success threshold.
* **Boolean** → true/false, with success threshold.
* **Guardrail** → activated / not activated.
* **Label** → zero, one, or multiple labels.

## ⚙️ Actions available in the Logs table

* Sort conversations (ascending/descending).
* View conversation details.
* Search conversations.
* Filter by date.
* Select which columns to show/hide.
* Refresh the list to load new conversations.
* Open a detailed log view to analyze evaluator results.

## 🔎 Log details

When you open a log in the side panel, you can:

1. **View conversation details**
   1. Username (editable).
   2. Date and time of the conversation.
   3. Session duration.
   4. Number of exchanged messages.
   5. User feedback (👍/👎).
   6. API errors.
   7. Guardrail activations (e.g., jailbreak detected).\

2.  **Inspect the conversation**

    1. Read the full exchange between the user and the assistant.
    2. See API error indicators and guardrail activations tied to messages.
    3. Access extra details or flag issues.


3. **Analyze log insights**
   1. Evaluators → review evaluation results, with error conditions highlighted first.
   2. CSAT → view user satisfaction scores, comments, and feedback timestamps.

## 🔄️ Chats vs. Conversations

The Chats section now also displays the individual conversations within each chat.\
From here, you can:

* Navigate between conversations in the same chat using the right-hand sidebar or search bar.
* See at a glance where each conversation begins and ends.
* Review the full exchange, including CSAT scores and Evaluator results.
