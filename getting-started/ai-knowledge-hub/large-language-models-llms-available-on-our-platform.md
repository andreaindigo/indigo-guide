# Large Language Models (LLMs) Available on Our Platform

Large Language Models (LLMs) play a crucial role in powering the AI Agents and workflows within **indigo.ai**. These models enable natural language understanding, reasoning, and content generation, ensuring businesses can automate interactions and provide intelligent, context-aware responses. This article explores the LLMs available in **indigo.ai**, their capabilities, and best practices for selecting the right model for your needs.

## Understanding LLMs in indigo.ai

At indigo.ai, we integrate multiple LLMs to offer a **flexible, high-performance AI ecosystem**. Different models are optimized for **speed or power**, allowing users to choose the best fit for their use case.&#x20;

Here’s how we categorize them:&#x20;

<table><thead><tr><th>Speed ⚡</th><th>Power 🚀</th><th>Reasoning 🧠</th><th data-hidden></th></tr></thead><tbody><tr><td><strong>gpt-4.1-mini</strong></td><td><strong>gpt-4.1</strong></td><td><strong>gpt-5.1</strong></td><td><strong>Balanced</strong> ⚖️</td></tr><tr><td>gpt-4.1-nano</td><td>gemini-2.5-flash</td><td>gpt-5-mini</td><td>gpt-4o-mini</td></tr><tr><td>gpt-4o-mini</td><td>claude-3.7-sonnet</td><td>gpt-5-nano</td><td>gemini-1.5-flash</td></tr><tr><td>gemini-2.0-flash</td><td>claude-4.5-sonnet</td><td>gemini-2.5-pro</td><td></td></tr><tr><td>gemini-2.5-flash-lite</td><td></td><td></td><td></td></tr><tr><td>mistral-small-3.2</td><td></td><td></td><td></td></tr><tr><td>claude-4.5-haiku</td><td></td><td></td><td></td></tr></tbody></table>

## **LLM Categories and Their Use Cases**

* **Speed:** Models that prioritize response time over advanced reasoning. Best for real-time interactions where immediate feedback is essential.
* **Power:** High-performance models with **strong generative capabilities**, designed for complex tasks but with longer response times.
* **Reasoning**: Models designed to generate a reasoning process before providing an answer. This feature makes them capable of solving complex tasks that require deep reasoning, at the cost of higher latency.

Models in **bold** within each category represent the **recommended models** based on performance and reliability.

## List of LLMs in indigo.ai

### **Available Models, Providers, and Server Locations**

<table><thead><tr><th width="208.94140625">Model Name in Platform</th><th width="164.7109375">LLM Backend</th><th width="130.703125">Provider</th><th width="141.41796875">Server Location</th><th>Comment</th></tr></thead><tbody><tr><td>gpt-4.1-mini (EU)</td><td>gpt-4.1-mini-2025-04-14</td><td>Microsoft Azure</td><td>Sweden</td><td>Default</td></tr><tr><td>gpt-4.1 (EU)</td><td>gpt-4.1-2025-04-14</td><td>Microsoft Azure</td><td>Sweden</td><td></td></tr><tr><td>gpt-4.1-nano (EU)</td><td>gpt-4.1-nano-2025-04-14</td><td>Microsoft Azure</td><td>Sweden</td><td></td></tr><tr><td>gpt-4o (EU)</td><td>gpt-4o-2024-05-13</td><td>Microsoft Azure</td><td>Sweden</td><td><br></td></tr><tr><td>gpt-4o-mini (EU)</td><td>gpt-4o-mini-2024-07-18</td><td>Microsoft Azure</td><td>Sweden</td><td></td></tr><tr><td>gpt-5.1 (EU)</td><td>azure-se-gpt-5.1</td><td>Microsoft Azure</td><td>Sweden</td><td></td></tr><tr><td>gpt-5-mini (EU)</td><td>azure-se-gpt-5-mini</td><td>Microsoft Azure</td><td>Sweden</td><td></td></tr><tr><td>gpt-5-nano (EU)</td><td>azure-se-gpt-5-nano</td><td>Microsoft Azure</td><td>Sweden</td><td></td></tr><tr><td>gemini-2.5-pro (EU)</td><td>gemini-2.5-pro</td><td>Google</td><td>Belgium</td><td></td></tr><tr><td>gemini-2.5-flash (EU)</td><td>gemini-2.5-flash</td><td>Google</td><td>Belgium</td><td></td></tr><tr><td>gemini-2.5-flash-lite (EU)</td><td>gemini-2.5-flash-lite</td><td>Google</td><td>Belgium</td><td><br></td></tr><tr><td>gemini-2.0-flash (EU)</td><td>gemini-2.0-flash-001</td><td>Google</td><td>Belgium</td><td><br></td></tr><tr><td>claude-4.5-sonnet (EU)</td><td>claude-sonnet-4-5@20250929</td><td>GoogleVertex</td><td>Belgium</td><td></td></tr><tr><td>claude-4.5-haiku (EU)</td><td>claude-haiku-4-5@20251001</td><td>GoogleVertex</td><td>Belgium</td><td></td></tr><tr><td>claude-3.7-sonnet (EU)</td><td>claude-3-7-sonnet@20250219</td><td>GoogleVertex</td><td>Belgium</td><td><br></td></tr><tr><td>mistral-small-3.2 (EU)</td><td>mistral-small-2506</td><td>Mistral</td><td>Sweden</td><td></td></tr><tr><td>maestrale-chat (self-hosted)</td><td>hf.co/mii-llm/maestrale-chat-v0.4-beta-GGUF</td><td>indigo.ai</td><td>Germany</td><td></td></tr></tbody></table>

## **Default Model in indigo.ai**

By default, we use **azure-gpt-4.1-mini (EU)** in our AI Agents and workflows. This model is selected because:&#x20;

* ✅ It offers a strong balance between **performance and response time**.&#x20;
* ✅ It is hosted on **Microsoft Azure EU servers**, ensuring **compliance with European data regulations**.
* ✅ It supports **advanced reasoning capabilities** while maintaining a reasonable token cost and latency.

However, you can choose to use **different models** based on your specific requirements.

## **How to Choose the Right Model**

Selecting the best model depends on several factors, including response speed, accuracy, reasoning ability, and token consumption. Here are some guidelines:

**1. Prioritize Speed (Fastest Response Time)**

Use **gpt-4.1-mini** if:&#x20;

✔ You need real-time responses. \
✔ Your use case involves quick user interactions. \
✔ Advanced reasoning is not the top priority.

**2. Prioritize Power**&#x20;

Use **gpt-4.1** or **gpt-5.1** if: \
✔ You need deep contextual understanding. \
✔ Your use case involves complex responses (e.g., legal, medical, or technical AI agents). \
✔ You’re willing to trade speed for accuracy.

## Best Practices for Choosing an LLM in Prompts

**Impact of Model Selection on Performance**

When configuring your AI Agent in indigo.ai, the model you choose affects:

* **Response Length**: More powerful models generate more detailed responses but consume more tokens.
* **Accuracy**: Higher-end models provide better coherence and logical reasoning.
* **Speed**: Faster models provide instant replies but may lack depth in reasoning.

## **Conclusion**

The **indigo.ai platform** offers a **diverse selection of LLMs**, each optimized for different use cases. Whether you need **fast interactions, a balanced approach, or maximum reasoning power**, selecting the right model is key to optimizing your AI’s performance. By default, we recommend **azure-gpt-4.1-mini (EU)** for most workflows, but users can choose based on their specific requirements.

Understanding LLM capabilities allows businesses to build **smarter, more efficient AI Agents**, ensuring they meet customer expectations with high-quality automated interactions.
