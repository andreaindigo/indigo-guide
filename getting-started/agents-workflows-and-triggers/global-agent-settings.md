---
description: Released in June 2025
---

# Global Agent Settings

When building virtual assistants at scale, there are some things you want **all your agents to have in common**: your company’s tone of voice, core values, communication rules, and even specific links or phrases to mention.

Until June 2025, those shared elements had to be manually copied into each agent’s configuration, which often led to inconsistencies and extra work.

That’s why we introduced Global Agent Settings: a **centralized way to define the shared DNA of your agents**, ensuring they stay aligned with your brand and strategy while saving time.

## What Are Global Agent Settings?

Global Agent Settings let you define and manage key configuration sections once, and apply them across all agents in your workspace. These include:

* Company Description
* Tone of Voice
* Brand Rules
* General Rules
* Useful URLs
* Conversation Examples
* AI Behavior Settings (like creativity and memory)
* Custom Sections (new reusable content blocks)

**Once configured, any newly created agent will automatically inherit these settings**.&#x20;

**Existing agents will sync with them unless they’ve already been customized locally** (more on that below).

## When Should You Use Them?

If a setting is meant to be **shared across multiple agents**, define it globally. This ensures brand consistency, simplifies maintenance, and avoids repetitive edits.

Use Global Agent Settings when:

* You're setting up foundational messaging (e.g., tone, brand values). **Single source of truth** – edit once, all Agents inherit it.
* You want to share examples or behavioral rules across many agents.&#x20;
* You're collaborating with other builders and want a single source of truth.
* **Faster onboarding** – new Agents are created pre-filled with approved content.

{% hint style="info" %}
Still need flexibility? Don’t worry: you can override global settings at the agent level when specific customization is needed. More details on configuring agents can be found here: [how-to-create-an-agent.md](how-to-create-an-agent.md "mention")
{% endhint %}

## How Global and Local Settings Work Together

Each agent will **inherit** global settings **unless** it has already been edited locally. Here’s how it works:

* **New agents** created **after** configuring global settings will automatically use them.
* **Existing agents** that haven’t been edited will also adopt the global values.
* **Agents that have been edited** (even just once) will **keep their own settings** and show a **“OVERWRITTEN”** tag to indicate that local configuration is overriding the global default.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-07 alle 14.21.24.png" alt=""><figcaption></figcaption></figure>

* If you want to **revert an agent to the latest global settings**, you can use the **"Reload agent"** option: it will restore all global values without affecting the agent’s title, trigger, or flow connections.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-07 alle 12.47.56.png" alt="" width="486"><figcaption></figcaption></figure>

## What You Can Configure Globally

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-07 alle 12.44.58.png" alt=""><figcaption></figcaption></figure>

Here’s a closer look at what’s available in the **Global Agent Settings** panel:

#### ✍️ Company Description

Define your brand identity, mission, and values so agents can speak in alignment with your company ethos.

#### 🗣️ Tone of Voice

Set the communication style, whether it’s friendly, professional, playful, or formal.

#### 🚫 Brand Rules

Specify restricted terms and suggest preferred alternatives (e.g., replace “cheap” with “affordable”).

#### 📏 General Rules

List must-follow guidelines for all agents, like whether they should ask questions to the user, how to handle off-topic or unprofessional messages.

#### 🔗 Useful URLs

Add links that agents should mention when relevant, such as help centers, booking pages, or policy documents.

#### 💬 Conversation Examples

Provide example interactions to help shape your agents’ responses. These examples can be reused across all agents and activated via a toggle in each agent block.

{% hint style="info" %}
Inside each Agent block:

* Toggle **Use core examples** to silently append every example stored in Global settings.
* The UI remains uncluttered; the extra examples are only visible in the compiled prompt.
* Add Agent-specific examples underneath as usual.\
  &#xNAN;_(Core examples are exempt from the OVERWRITTEN logic – use them anywhere.)_
{% endhint %}

#### 🧩 Custom Sections

Create reusable content snippets (e.g., disclaimers, legal notes).

{% hint style="info" %}
Custom Sections behave like [variables](../blocks-and-variables/variables/), but are hidden from the regular \{{variables\}} picker.

* **Create**: Agent settings → **Add section** → give it a name and content.
* **Insert**: In any multiline text field inside an Agent, type **“/”** and pick the section from the dropdown (or keep typing its name).
* **Read-only** in Agents: edit them centrally. Perfect for legal footers, pricing disclaimers, or shared promo blurbs.
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-07 alle 12.45.42.png" alt=""><figcaption></figcaption></figure>

#### 🧠 AI Behavior Settings

Define default AI configuration, including:

* Model to use
* Creativity level
* Short memory (how many previous messages the agent considers)
* Max tokens for answers and documents
* Hypercontrol (for strict output validation)
* Fallback message for errors

{% hint style="info" %}
You can find a more detailed explanation of these settings here: [#id-4-agent-settings](how-to-create-an-agent.md#id-4-agent-settings "mention")
{% endhint %}

## How to Access Global Settings

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-07 alle 14.11.38.png" alt="" width="291"><figcaption></figcaption></figure>

1. Open your workspace.
2. Click on **“Agent Settings”** from the bottom-left sidebar.
3. You’ll land on the **Global Settings** page, where all configuration sections are available for editing.

Changes are saved per section and are instantly available for any new agents you create.

## Best Practices

1. Start by defining your **company-wide defaults** in Global Agent Settings.
2. Use **custom sections** for any content reused across many but not all agents.
3. **Create new Agents**: they inherit everything automatically.
4. **Adjust only when necessary** inside an Agent; if you modify a global field, you’ll see **OVERWRITTEN**. **Regularly audit** for this tag to ensure only necessary overrides exist.
5. Use **“Reload agent”** to reset outdated or inconsistent blocks when needed.
