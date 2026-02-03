---
description: Released in May - June 2025
---

# Workspace Updates - Q2 2025

We’re excited to share the latest updates from Q2 2025: a set of powerful features designed to make your workspace smarter, your assistants more flexible, and your compliance simpler. These releases give you more control over how you manage agents, collect data, handle privacy, and structure your conversational logic.

Here’s what’s new this quarter:

* [**Global Agent Settings**](workspace-updates-q2-2025.md#global-agent-settings): Centrally define common parameters for all your agents: tone of voice, brand rules, company description, and more.
* [**Collect Block**](workspace-updates-q2-2025.md#collect-block): A smarter way to gather structured data from users in natural conversations.
* [**Privacy Settings in Widget**](workspace-updates-q2-2025.md#privacy-settings-in-widget): Comply with legal requirements by linking a mandatory privacy policy before any user interaction.
* [**Optimized Prompt Block**](workspace-updates-q2-2025.md#optimized-prompt-block): Use multi-role prompt formatting (system, user, assistant) and context control for more powerful, accurate AI responses.
* [**Metadata Block**](workspace-updates-q2-2025.md#metadata-block): Add invisible JSON metadata to your flows for advanced integration, especially for Voice assistants.
* [**Streamlined Multilingual Management**](workspace-updates-q2-2025.md#streamlined-multilingual-management): Automatically translate static content and widget UI into multiple languages.

Let’s take a closer look at each feature 👇

## 🌐 Global Agent Settings

Managing multiple AI agents just got easier. With Global Agent Settings, you can **define shared configurations once and apply them across your entire workspace**.

Whether it’s your **company’s tone of voice**, **key brand instructions**, or **background context**, you no longer need to repeat these settings manually for each agent. Instead, you can centralize them, reducing setup time and ensuring consistency across all conversations.&#x20;

For use cases where brand identity or compliance rules must be preserved across every assistant, this feature ensures alignment by design.

**Each agent still supports local customization, but now you can decide what should be inherited globally and what should be unique per agent**.

{% hint style="info" %}
Read the full article → [agents-settings.md](../../getting-started/workspace/agents-settings.md "mention")
{% endhint %}

## 🧪 Collect Block

The new **Collect Block** brings flexibility and intelligence to data gathering.

Unlike rigid question-and-answer flows, the Collect Block can **extract structured data naturally from user messages**. Whether the user provides information upfront or not, the assistant can **identify missing values, ask follow-up questions, and capture the data you need**, all without disrupting the flow of the conversation.

Ideal for forms, onboarding, bookings, and more: the Collect Block makes data collection seamless and smart.

#### Highlights:

* Collect multiple variables in one block
* Provide custom descriptions, formats, or regex validations
* Define admissible values and synonyms for each field
* Choose whether to automatically prompt the user for missing inputs

{% hint style="info" %}
Explore how it works → [collect-block.md](../../getting-started/blocks-and-variables/logic-blocks/collect-block.md "mention")
{% endhint %}

## 🔐 Privacy Settings in Widget

To support regulatory compliance and build user trust, we’ve introduced **Privacy Settings** directly in the Web Chat widget configuration.

You can now:

* Add a **mandatory privacy policy link** that users must see before starting a conversation
* Optionally include a Terms of Service link
* Enable **explicit consent** (checkbox) if required by your legal team

When enabled, the assistant will not respond until the user has reviewed (and optionally accepted) the terms. The UI is clear, accessible, and automatically prevents message submission if consent hasn’t been granted.

This feature ensures your chat complies with GDPR and other data protection laws — without any coding or custom setup.

{% hint style="info" %}
View setup instructions → [#privacy-settings](../../build-your-ai-agents/configure-and-install-the-web-chat.md#privacy-settings "mention")
{% endhint %}

## ⚡**Optimized Prompt Block**

Our **Prompt Block** just got a major upgrade, making it more powerful, flexible, and aligned with how today’s [LLMs](../../getting-started/ai-knowledge-hub/large-language-models-llms-available-on-our-platform.md) work best.

You can now structure prompts using **multiple message roles** (`system`, `user`, `assistant`) instead of just a single block of text. This unlocks:

* More natural and contextual interactions
* Better performance with newer models like GPT-4o
* Clearer control of how prompts are framed, especially when simulating conversation history

In addition, you can now manage **short memory settings** directly in the block, choosing how much recent context the model should retain. This ensures cleaner prompting, especially in follow-up scenarios or when testing variations.

Use the new format to simulate conversation turns, chain-of-thought reasoning, or step-by-step classification, all while staying fully backward compatible.

{% hint style="info" %}
Deep dive on the new Prompt Block → [#message-composer](../../getting-started/blocks-and-variables/utility-blocks/prompt-block.md#message-composer "mention")
{% endhint %}

## 🎛 Metadata Block

The **Metadata Block** allows you to inject structured JSON metadata into your workflows: especially valuable for [**voice assistants**](../../getting-started/communication-channels/voice.md) and custom integrations.

This content isn't shown to users but is processed at runtime, enabling actions like:

* Sending context data to external platforms (e.g., HubSpot, analytics tools)
* Driving channel-specific behaviors in voice interactions
* Triggering internal logic based on hidden instructions

A powerful block for teams working with complex channel integrations or advanced automation.

{% hint style="info" %}
Learn how to use the new block → [metadata-block.md](../../getting-started/blocks-and-variables/utility-blocks/metadata-block.md "mention")
{% endhint %}

## 🌍 Streamlined Multilingual Management

Managing multilingual virtual assistants is now easier than ever. With our new automatic translation capabilities, **static content, such as messages in workflows and interface elements in the widget, can be instantly translated into supported languages**.&#x20;

Powered by DeepL, this feature ensures a seamless and localized user experience across all touchpoints, without requiring manual duplication or structural changes to the workflows. You can review, edit, and manage translations more easily within the platform for **full control and flexibility.**

{% hint style="info" %}
Find more details here → [multilingual-capabilities.md](../../getting-started/multilingual-capabilities.md "mention")
{% endhint %}

***

These updates are all about giving you more structure, better control, and compliance by default, whether you're building a single assistant or managing dozens at scale.

{% hint style="info" %}
As always, we’re here to support your journey toward smarter, more meaningful conversations. \
Need help using any of the new features?\
👉 [Contact our Customer Success team](../../need-help/our-customer-success-team.md) for a guided walkthrough.
{% endhint %}
