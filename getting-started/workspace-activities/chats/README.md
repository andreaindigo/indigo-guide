---
icon: comments
---

# Chats

Curious about what users are saying and how they interact with your virtual assistant? You’re in the right place.

The Chat section gives you a **complete view of all conversations between your AI assistant and users**. It's a powerful tool to **monitor real-time interactions**, **analyze chatbot performance**, and **gather insights** to improve the user experience.

{% embed url="https://screen.studio/share/4Z1vl6ph?_loop=1&autoplay=1" %}
The Chat Area
{% endembed %}

## Filtering and Consulting Conversations

### Chat Details

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-03 alle 08.37.10.png" alt=""><figcaption></figcaption></figure>

This section collects and organizes every user conversation, offering essential details for each chat:

* **User ID** – A unique identifier for every user, displayed with a pseudonym to protect privacy. You can rename this pseudonym by clicking the ✏️ icon.
* **Start Time** – The exact date and time the conversation began.
* **User Email** – If the experience is designed to capture it.

### Chat Categories

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-03 alle 08.25.53.png" alt="" width="258"><figcaption></figcaption></figure>

You can browse conversations by the following categories:

* **All** – Every chat, no filters.
* **Open** – Conversations still ongoing or unresolved, possibly requiring human takeover (if enabled - see below for more details).
* **Closed** – Completed chats that the assistant has handled autonomously.
* **Test** – Chats created during platform testing or via the **Preview AI** feature.

{% hint style="info" %}
Chats initiated from within the workspace (e.g., during testing) appear in the “Test” tab, while user-initiated conversations from live environments appear in “All.”
{% endhint %}

### Available Filters

To simplify the search and analysis of chats, you can apply a series of filters. These filters allow you to quickly find the conversation you're looking for based on various variables:

<figure><img src="../../../.gitbook/assets/filtri disponibili.png" alt=""><figcaption></figcaption></figure>

* **Variables:** Filter conversations by the value of one or more variables used in the interaction.
* **CSAT (Customer Satisfaction Score):** Filter by score (equals, not equals, more than, less than).
* **CSAT Comment:** Filter chats with or without user comments.
* **Feedback**: Sort by user feedback (👍 or 👎: only positive, only negative, more positive than negative, etc.).
* **Agent/Workflow**: Filter by which agent or workflow was involved in the conversation.
* **User Email**: Filter chats with or without user email addresses.
* **Keyword**: Search chats for specific words or phrases.
* **Need Support**: Quickly identify chats flagged as needing help from a human operator.
* **Date:** View chats from a specific time range.

### Sorting Options

You can sort conversations by:

* **Newest** → Oldest
* **Oldest** → Newest
* **User A–Z**
* **User Z–A**

### Advanced Search

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-03 alle 08.34.50.png" alt=""><figcaption></figcaption></figure>

Looking for something specific? Use the **keyword search** to locate particular themes, user messages, or recurring issues across all conversations.

## ⭐️ Special Features

The Chats section of your workspace isn't just for browsing conversation history—it also includes two advanced tools designed to give you greater control and visibility: **Human Takeover**, **Debugging**, and the new **Issue Tracker integration**.

### 🤝 Human Takeover

Human Takeover **allows your team to step into live conversations whenever human intervention is required**. This is especially useful in **complex or sensitive cases** that go beyond what the virtual assistant can handle on its own.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-03 alle 08.48.17.png" alt="" width="294"><figcaption></figcaption></figure>

AI Agents are great at managing most incoming queries autonomously, but there are always scenarios where **a personal touch is needed**—whether it's to reassure a customer, resolve an edge case, or provide high-priority support.

Once activated, your operators can:

* Jump into active chats in real time.
* Take over directly from the AI to assist the user.
* View full chat history and user context for a seamless handover.

{% hint style="info" %}
Interested in enabling Human Takeover? [Contact our team](../../../need-help/our-customer-success-team.md) to activate this feature in your workspace.
{% endhint %}

### 🛠 Debugging

The Debugging panel gives you a **detailed, step-by-step breakdown of how a particular message was generated within the platform**. It's an essential tool for anyone building and [testing](../../../build-your-ai-agents/testing-and-debugging.md) AI assistants.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-03 alle 08.53.56.png" alt=""><figcaption></figcaption></figure>

When a conversation doesn’t go as expected, Debugging allows you to:

* View which agent and workflow generated the message.
* Trace the path taken through your workflow (including reroutes).
* See how variables were handled and prompts were processed.
* Understand any missteps in the response logic.

This feature is incredibly powerful for **troubleshooting** and optimizing your assistant's performance—**without needing external support**.

{% hint style="info" %}
Learn how to make the most of this feature in our dedicated guide: [debugging.md](debugging.md "mention").
{% endhint %}

### 🚩 Issue Creation 🆕

The new **Issue Tracker** feature allows you to efficiently **flag conversations needing improvement** directly from the Chats section.&#x20;

{% hint style="info" %}
Learn more about the new feature here: [issue-tracker-for-tests-and-improvements.md](../../../product-updates/latest-product-releases/issue-tracker-for-tests-and-improvements.md "mention")

**Please note:** This feature is currently in beta testing. To request activation, please [contact our Customer Success team](../../../need-help/our-customer-success-team.md).
{% endhint %}

Hover over any chat message to flag it as an issue. A dedicated panel appears, enabling you to quickly enter:

* **Issue Title**: A concise summary of the issue.
* **Description**: A detailed explanation of the problem.
* **Priority Level**: Choose from Low, Medium, or Urgent.
* **Tags**: Categorize the issue clearly (e.g., Bug, Improvement, API Error, Bad Tone of Voice).
* **Assignee**: Assign the issue to a team member or your indigo.ai Customer Success Manager by default.

<figure><img src="../../../.gitbook/assets/create issue from chat.png" alt=""><figcaption></figcaption></figure>

* **Visual Indicators:** Messages flagged as issues are clearly marked within the conversation view, allowing immediate visibility.
* **Tracking and Resolution:** All flagged issues are centrally managed within the dedicated Issue Tracker dashboard, offering full visibility into issue status (To Do, In Progress, Done, Review), comments, historical updates, and easy access to debugging information.
