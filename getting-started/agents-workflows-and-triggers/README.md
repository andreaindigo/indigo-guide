---
description: >-
  Learn more about our intelligent agents and triggers that initiate
  interactions.
icon: microchip-ai
---

# Agents, Workflows & Triggers

In the [introduction-to-indigo.ai](../introduction-to-indigo.ai/ "mention"), we've highlighted what makes our solution unique. Instead of relying on a traditional single AI agent managing all tasks, our platform is designed around a **collaborative AI Agents Workforce**: a team of specialized agents, each with distinct expertise and knowledge bases, working together seamlessly.

## 👮‍♀️ Agents

An AI Agent is an advanced software program capable of interacting with its environment, collecting data, and performing tasks to achieve predefined goals. From a technical perspective, each agent operates based on a **prompt template**—a structured instruction set designed by indigo.ai for optimal performance.

AI Agents are built using a series of instructions that define:

* How to respond to specific user questions.
* What tone, style, and approach to use.
* Where to source knowledge from (e.g., documentation or databases).

Each agent is goal-oriented: if a user asks a question related to a specific topic, the agent responds accordingly, using predefined information.&#x20;

💡 Think of **agents as subject matter experts** for different tasks or services. For example, in a shoe e-commerce scenario, you might have agents for shipping & returns, payments and transactions, and product recommendations.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-24 alle 15.38.17.png" alt=""><figcaption><p>The AI Agent Block</p></figcaption></figure>

#### Building a Team of Agents

There's no limit to the number of agents you can create and associate with a virtual assistant.&#x20;

However, it's crucial to strike the right **balance between granularity**—ensuring each agent has a clear, non-overlapping scope—**and manageability**, keeping the setup streamlined and avoiding excessive complexity.

#### The General Agent

Among your team of agents, one stands out as essential: the General Agent.&#x20;

The General Agent serves as a **fallback mechanism**, with the primary objective of **replying to all questions that do not pertain to the other specialized agents**.&#x20;

This agent is automatically included in every new workspace and should never be deleted.

Whether it's casual conversation, general FAQs, vague requests, or even trolling attempts, the General Agent steps in to ensure users always receive a response.&#x20;

{% hint style="info" %}
For more details on configuring this and other agents, check out the next article: [how-to-create-an-agent.md](how-to-create-an-agent.md "mention")
{% endhint %}

## 🧠 Mother Agent

<figure><img src="../../.gitbook/assets/Frame 61424.png" alt=""><figcaption><p>Visual representation of the indigo.ai architecture</p></figcaption></figure>

At the core of every AI-powered interaction is the Mother Agent, the **orchestrator** that ensures every user query is handled by the most suitable specialized agent or workflow.&#x20;

It acts as the **decision-making brain of the virtual assistant**, determining—for every single user message—which agent should respond or which workflow should be triggered before delivering an answer.

The Mother Agent is **not visible** within the workspace—it is a built-in Indigo.ai feature with a complex internal logic that cannot be modified or configured by users. However, if necessary, Indigo’s Customer Success team can adjust it in specific cases.

Behind the scenes, the Mother Agent operates through an advanced prompting system:

1. When a user sends a message, the Mother Agent ranks all available agents and workflows in the workspace based on relevance to the query.&#x20;
2. It then chooses the most suitable agent or workflow by considering various factors, such as conversation context (previous messages) and triggers (explained below).&#x20;
3. Once selected, the agent or workflow takes over and processes the response.

While its logic is intricate, the key takeaway is that the Mother Agent dynamically orchestrates interactions, allowing you to efficiently manage and control conversational flows with your users.&#x20;

## 👂 Triggers

The Mother Agent determines virtual assistant behavior primarily based on triggers.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-24 alle 15.34.13.png" alt=""><figcaption></figcaption></figure>

**A trigger defines the conditions for activating an agent or workflow**. You can specify:

* Trigger Details: When the agent/workflow should activate.
* Example Questions: Sample user queries that would activate the agent/workflow.

{% hint style="warning" %}
If an agent or workflow has no defined trigger, it is invisible to the Mother Agent.&#x20;
{% endhint %}

However, **not all agents or workflows need a trigger—only high-level agents or workflows require them.**&#x20;

In essence, the Mother Agent assigns user queries to top-level agents, which can delegate tasks to secondary agents or workflows (without needing triggers). This layered approach ensures an organized, scalable, and efficient response process.

This may seem complex, but in reality, it’s quite straightforward. The best way to approach it is by thinking in terms of **conversation flow**: the main entry points and key topics that the virtual assistant handles should have a trigger, the supporting ones not.

That is why, to make this process easier, the first step in our AI Agents creation guide ([Broken link](broken-reference "mention")) is designing the conversation flow.&#x20;

&#x20;
