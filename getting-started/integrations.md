---
description: Connecting the platform with your favorite tools and systems.
icon: puzzle-piece
---

# Integrations

Integrating your AI assistant with your existing business systems is key to unlocking its full potential. indigo.ai offers a comprehensive suite of integration options, enabling connections with Customer Relationship Management (CRM) platforms, e-commerce systems, Enterprise Resource Planning (ERP) tools, and other essential applications. These integrations facilitate real-time data exchange, streamline operations, and enhance both user and operator interactions.

All integrations are managed through our powerful [**API Block**](blocks-and-variables/action-blocks/api-block.md), a core component in the conversational flow builder. This feature allows your assistant to **read from and write to third-party systems**, enabling **real-time data exchange and dynamic responses**.

## Available Integrations

### 1. CRM and Ticketing System Integrations

Integrating your AI assistant with CRM and ticketing systems streamlines customer service workflows and improves agent efficiency. By leveraging these integrations, your assistant can automate tasks such as:

* Creating and updating support tickets
* Retrieving user profiles and customer history
* Providing real-time status updates
* Logging interactions for better continuity in agent handovers.

indigo.ai provides a **native integration with Zendesk** and also supports **custom integrations with virtually any CRM platform, including Salesforce, HubSpot, and others**.

### 2. E-commerce Platform Integrations

Enhancing your online store with an AI assistant can significantly improve customer engagement and support.​

* **Shopify Integration**: indigo.ai offers a native integration with Shopify, allowing your assistant to assist customers with product inquiries, order tracking, and personalized recommendations.&#x20;
* **Other E-commerce Platforms**: Integrations with platforms like Magento and PrestaShop are possible through API connections, enabling your assistant to access product catalogs, manage orders, and provide customer support.

### 3. ERP and Management System Integrations

Connecting your AI assistant to ERP systems such as **SAP** and **Microsoft Dynamics** facilitates access to organizational data, streamlining processes like inventory management, order processing, and internal communications.​

### 4. Google Workspace Integration

Integrating with Google Workspace allows your assistant to interact with tools like Google Sheets and Gmail. This enables functionalities such as **retrieving data from spreadsheets** and **sending emails**, enhancing the assistant's capabilities in managing tasks and communications.​

## Custom Integration Solutions

If your system has APIs and is not listed among the standard integrations, indigo.ai supports custom integration configurations. We evaluate integration possibilities based on API availability to ensure seamless connectivity with your proprietary interfaces or platforms.

## Integrating your Knowledge Base (KB)

One of the most impactful integration use cases is connecting your Knowledge Base (KB) and internal data sources directly to indigo.ai.&#x20;

**AI Agents rely on structured, up-to-date information to provide accurate and helpful responses—your KB acts as the foundation for this.**

By **integrating your KB via API**, you enable your **assistant to access real-time, structured data** from your internal systems or databases. This is especially beneficial when working with:

* Large or Complex Datasets
* Frequently Updated Information
* Dynamic Sources: Such as product catalogs and inventory from e-commerce platforms (e.g., Shopify, Magento), user data and historical ticket information from CRM systems (e.g., Salesforce, Zendesk, HubSpot), or data from ERP solutions and proprietary internal databases.​

This setup ensures your assistant always delivers responses that are not only relevant and consistent but also aligned with current business operations.

{% hint style="info" %}
Learn more about best practices for setting up your KB in this section of the guide: [create-your-knowledge-base](../build-your-ai-agents/create-your-knowledge-base/ "mention"), and explore how to implement API-based content integrations in detail in this article: [integrating-your-kb-via-api.md](../build-your-ai-agents/create-your-knowledge-base/integrating-your-kb-via-api.md "mention").
{% endhint %}

## Integration with User Authentication

Kick off conversations with personalized data by integrating your chatbot with your authentication systems. This allows you to **initialize the chat with user-specific information**—such as user ID, login status, or preferred contact method—making the interaction more relevant and efficient from the very first message.

This setup enables you to prefill variables, **personalize assistant responses, and tailor the experience based on who's interacting with your virtual assistant**.

For a technical deep dive, check out this article that explains **how to pass data directly to the web chat** using URL parameters in the web chat script: [#id-2.-passing-parameters-to-the-assistant](../tech-deep-dives/web-chat-integration-and-customization-on-your-website/web-chat-integration-dynamic-interaction-and-data-exchange-with-your-website.md#id-2.-passing-parameters-to-the-assistant "mention").&#x20;
