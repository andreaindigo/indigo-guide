---
description: Released in September 2025
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Evaluators, Guardrails & Conversation Logs

## Evaluators & Guardrails

### 📌 Overview

**Evaluators** (or evals) are automated tools in indigo.ai that **analyze conversations**.\
They help measure key aspects such as response relevance, user sentiment, tone, and topics, providing objective, timely, and scalable evaluations without relying on manual reviews.

Evaluators work together with **Guardrails**, which act as **preventive checks** during live conversations.&#x20;

Together, they provide a complete framework for monitoring, improving, and governing the virtual assistant's quality.

{% hint style="info" %}
From a technical perspective, evals run [LLM models](../../getting-started/ai-knowledge-hub/large-language-models-llms-available-on-our-platform.md) _after_ a response to check its quality and correctness, while guardrails run _before and during_ generation to constrain what the virtual assistant can or cannot say.

In simple terms:

* **Evals = post-checks** ✅ (evaluate answers after they’re produced).
* **Guardrails = pre-checks + live constraints**🚦 (control behavior before and during the reply).
{% endhint %}

<figure><img src="../../.gitbook/assets/add evaluator step 1.png" alt=""><figcaption></figcaption></figure>

### ✅ Benefits

* **Objective and fast evaluations** → continuous quality monitoring, independent from human judgment.
* **Operational efficiency** → reduce manual effort, freeing resources for higher-value tasks.
* **Trend and pattern detection** → uncover recurring issues, user sentiment trends, or escalation needs.
* **Improved perceived quality** → proactive monitoring strengthens brand reputation and service trustworthiness.

### Built-in vs Custom

indigo.ai provides both built-in evaluators and guardrails (ready-to-use “black boxes”), and the **ability to design custom ones for specific use cases**.

{% hint style="info" %}
For more details read the full guide: [evaluators-and-guardrails.md](../../getting-started/workspace-activities/utilities/evaluators-and-guardrails.md "mention")
{% endhint %}

## Conversation Logs

### 📌 Overview

Conversation Logs provide a centralized place in the indigo.ai platform where you can view the **full list of conversations and their corresponding Evaluator or Guardrail results**.

This section allows teams to analyze every single conversation, understand how evaluators and guardrails performed, and start any necessary **debugging** flows.

<figure><img src="../../.gitbook/assets/conversation log 3.png" alt=""><figcaption></figcaption></figure>

### ✅ Benefits

* **Detailed visibility** → review all conversations in one place, with full evaluator and guardrail outcomes.
* **Operational efficiency** → quickly identify issues, user feedback, or API errors without switching tools.
* **Debug-ready** → inspect conversations in detail, including errors and triggers, to improve the chatbot’s performance.

### 💬 What is a Conversation Log?

A Conversation Log represents one interaction between an AI Agent and an end-user.

* A conversation begins when the user starts the chat and ends when they click Close Chat.
* Multiple conversations together form a chat.

In the Conversation Logs view, you can browse the list of conversations and check how evaluators and guardrails performed for each one.

{% hint style="info" %}
For more details read the full guide: [conversation-logs.md](../../getting-started/workspace-activities/utilities/conversation-logs.md "mention")
{% endhint %}
