---
icon: shield
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Evaluators and Guardrails

### Measuring, controlling and improving conversation quality

## 📌 Overview

Evaluators (or evals) are automated tools in indigo.ai that analyze and assess chatbot–user conversations.\
They help measure key aspects such as response relevance, dialogue coherence, tone, and topics, providing objective, timely, and scalable evaluations without relying on manual reviews.

Evaluators work together with Guardrails, which act as preventive checks during live conversations. Together, they provide a complete framework for monitoring, improving, and governing chatbot quality.

## ✅ Benefits

* Objective and fast evaluations → continuous quality monitoring, independent from human judgment.
* Operational efficiency → reduce manual effort, freeing resources for higher-value tasks.
* Trend and pattern detection → uncover recurring issues, user sentiment trends, or escalation needs.
* Improved perceived quality → proactive monitoring strengthens brand reputation and service trustworthiness.

## Types of evaluators

### Classic evaluators

Work **at the end of a chat session**, analyzing the full conversation to assess its quality.

* Typical outputs:
  * Score (1–10, with customizable thresholds)
  * Labels (topics, outcomes)
  * Boolean values (true/false)

### Guardrails

Run in **real time during the conversation**, analyzing each user message and assistant response.

* Output: trigger activated / not activated
* Can automatically start actions (fallback, redirect, sanitization).

## Built-in vs. Custom

indigo.ai provides both built-in evaluators and guardrails (ready-to-use “black boxes”), and the ability to design custom ones for specific use cases.

### Built-in evaluators & guardrails

These are the pre-configured evaluators and guardrails available in the platform.\
Evaluators run **after a conversation ends**, while Guardrails act **in real time on each message**.

* **Chat success** _(Evaluator)_ → evaluates if the chatbot successfully handled or completed the user’s request. Outcome: score 1–10.
* **CSAT (Customer Satisfaction)** _(Evaluator)_ → assigns a satisfaction score to the conversation. Outcome: score 1–5.
* **User Sentiment** _(Evaluator)_ → analyzes user sentiment (positive, negative, neutral).
* **Tone consistency** _(Evaluator)_ → checks alignment of chatbot replies with the tone of voice defined in workspace settings. Outcome: score 1–10.
* **Repetition presence** _(Evaluator + Guardrail)_ → detects redundant answers. Outcome: true/false.
* **Escalation appropriateness** _(Evaluator)_ → determines if human handover would have been appropriate. Outcome: score 1–10.
* **Harmful content** _(Evaluator)_ → flags harmful, biased, or NSFW answers. Outcome: true/false.
* **Language coherence** _(Evaluator)_ → ensures replies are in the correct language. Outcome: true/false.
* **Hallucination** _(Guardrail)_ → checks if answers are consistent with available information and prompts. Outcome: true/false.
* **Jailbreak detection** _(Evaluator + Guardrail)_ → detects jailbreak attempts. Outcome: true/false.
* **Response Formatting Check** _(Guardrail)_ → ensures answers respect the required format (JSON, list, bullet points, etc.). Outcome: true/false.
* **Keyword presence** _(Evaluator + Guardrail)_ → identifies relevant keywords (e.g., competitors). Outcome: list of keywords.
* **Personally Identifiable Information (PII) Detection** _(Guardrail)_ → flags sensitive or confidential content. Outcome: true/false.
* **Insights extractor** _(Evaluator)_ → extracts relevant topics from the conversation. Outcome: list of topics.

### Custom evaluators &  guardrails

In addition to the built-in options, you can create **custom evaluators and guardrails** tailored to your specific use cases.

* **Custom Evaluators** let you define the goal, choose the output type (score, boolean, or label), and provide the logic (prompt) to analyze conversations.
* **Custom Guardrails** let you set rules on individual messages, with a true/false outcome, to trigger actions in real time (e.g., fallback, redirect, re-generation).

Once created, custom items appear in the same screen as the built-in ones and can be activated in the same way.

## ⚙️How to access and activate Evaluators

Evaluators can be managed directly from the indigo.ai platform.

<figure><img src="../../../.gitbook/assets/add evaluator step 1.png" alt=""><figcaption></figcaption></figure>

1. In the left-hand side menu, go to the Utilities section (top area).
2. Click on Add Evaluator.
3. Choose the type of evaluator:
   1. Built-in (Suggested) → preconfigured evaluators that can be enabled immediately.
   2. Custom → create your own evaluator by selecting the output type (Score, Label, Boolean/Trigger) and writing a prompt/description of what you want to analyze.

### If you choose Built-in Evaluator

* A list of available built-in evaluators will open.

<figure><img src="../../../.gitbook/assets/add evaluator suggested1.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/add evaluator suggested2.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/add evaluator suggested3.png" alt=""><figcaption></figcaption></figure>

* Click on the one you want to use: it will then appear in your Evaluators screen.
* To enable it, click Activate.

<figure><img src="../../../.gitbook/assets/attiva evaluator.png" alt=""><figcaption></figcaption></figure>

### If you choose Custom Evaluators

You can create your own evaluator by selecting one of the four available types:

* **Label Evaluator** → classifies the conversation into one or more categories (topics).
* **1–10 Evaluator** → assigns a score from 1 to 10 based on a parameter you define (e.g., tone of voice, accuracy, helpfulness).
* **Boolean Evaluator** → checks whether the conversation meets a preset condition, returning true or false.
* **Guardrail** → runs in real time to ensure the chatbot behaves as intended, preventing harmful or undesired outputs.

<figure><img src="../../../.gitbook/assets/add evaluator custom.png" alt=""><figcaption></figcaption></figure>

**Each evaluator type comes with its own setup fields that need to be configured (e.g., categories for the Label Evaluator, scoring parameter for the 1–10 Evaluator).**&#x20;

Once saved, the evaluator appears in your Evaluators screen and can be activated.

## 📊 Viewing results in Analytics

When you add an evaluator, you can decide whether its results should also appear in Analytics by enabling the option Show in Analytics.

* Evaluators screen → after creating or adding an evaluator, you’ll see a toggle/option to enable Show in Analytics.
* Analytics tab → located in the same screen as the Evaluators, on the right-hand side. Here you can track the performance of evaluators you’ve chosen to display.

<figure><img src="../../../.gitbook/assets/view analytics.png" alt=""><figcaption></figcaption></figure>

This allows you to:

* visualize the trend of a score (e.g., average CSAT over time),
* monitor the frequency of labels or boolean results,
* compare multiple evaluators side by side.

💡 **Tip**: Only evaluators marked as Show in Analytics will appear in the Analytics tab. You can use this option to keep the dashboard clean and focused on the most important metrics.
