---
description: Review the various channels available for deploying your agents.
icon: briefcase
---

# Web Chat Integration within CRM Platforms

Your virtual assistant can be seamlessly integrated into the web chat interface of CRM platforms like **Zendesk, Salesforce** and **Vivocha**. In this setup, the assistant works within the CRM's web chat system, supporting existing workflows and engaging with users without disruption.

#### Key Benefits

* **AI Agents on Existing Channels**: If your team is already using a CRM’s web chat, you can integrate your AI assistant into that channel, preserving the familiar interface and workflow.
* **Human Handover**: Manage human takeover efficiently within the CRM’s system, ensuring a smooth transition from the assistant to live agents when needed.
* **Ticketing System and KB Integration**: Automatically create and update support tickets, or integrate your knowledge base directly into the CRM’s system for seamless interactions.

#### Channel-Specific Features

* **Customization**: The Web Chat widget configuration and customization options are determined by the CRM platform. However, core agent features - such as the ability to create image carousels in chat using the [Card Block](https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#card-block-structured-and-interactive-content) - are typically supported across various platforms.
* **Quick Reply Options**: The typebar cannot be disabled when [quick replies](../blocks/action-blocks/quick-reply-block.md) (user response options via buttons) are used. Therefore, it’s important to account for the possibility that users may choose to type a response instead of clicking on the buttons.

{% hint style="info" %}
💡 **CRM Integration Options**

* indigo.ai offers a **native integration with Zendesk** for seamless deployment and support within its ecosystem.
* To integrate your virtual assistant with **other CRM platforms** (such as Salesforce), you can use our **Chat API** for full flexibility.
* If you also want your assistant to interact with the **CRM's ticketing system or knowledge base**, you'll need to set up an integration with that external system. Learn more about available integrations in this article: [integrations](../integrations/ "mention").
{% endhint %}
