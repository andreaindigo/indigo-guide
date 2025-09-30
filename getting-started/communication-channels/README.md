---
description: Review the various channels available for deploying your agents.
icon: comment-dots
---

# Communication Channels

indigo.ai virtual assistants can be deployed across a wide range of communication channels, allowing you to **meet your users where they are**—whether that’s on your **website**, in **messaging apps**, within **CRM systems**, or through **voice**-based interactions. Our platform gives you the flexibility to choose the channels that best support your business goals and customer needs.

## **Available Communication Channels**

1. 🌐 **Web Chat**\
   Easily deploy your assistant on your website or app using our fully customizable Web Chat widget. Designed for an intuitive, branded experience, it supports rich interactions and advanced configurations.
2. **💼 Web Chat Integration within CRM Platforms**\
   Integrate your assistant into the web chat tools of CRM platforms like Zendesk or Salesforce. This allows it to function directly within your existing support ecosystem—streamlining interactions and ensuring smooth handovers between automated and human support.
3. **📱 WhatsApp**\
   Provide fast, mobile-friendly support through WhatsApp.
4. 🗣️ **Voice**\
   Offer voice-based interactions through Voice support. Whether over the phone or, in the future, directly in web chat, this channel allows users to engage with your assistant using speech for a more natural and accessible experience.

➡️ You'll find more details on features, benefits, and technical specifics of each channel in the sections below.

{% hint style="info" %}
**Licensing Notes**

* Channels beyond Web Chat are available only with a Super or Elite license.
* Channel-specific analytics are available with the Elite license only.
* Ongoing maintenance for non-native integrations is available as an add-on.
{% endhint %}

### Custom Solutions and API Access

**In addition to our native integrations**, indigo.ai supports **custom channel configurations**.&#x20;

If your business requires integration with proprietary platforms or external systems, our **Chat API** enables a flexible connection.

We evaluate integration possibilities based on API availability.

If you'd like to integrate your AI assistant with proprietary interfaces or other platforms, you need to access our **Chat API** for a seamless connection.&#x20;

{% hint style="info" %}
For full technical guidance, please refer to our documentation here: [integrating-custom-channels-with-the-chat-api.md](../../tech-deep-dives/integrating-custom-channels-with-the-chat-api.md "mention").&#x20;
{% endhint %}

### Analytics for Each Channel

If your assistant operates across multiple channels, you'll soon be able to track and analyze performance for each one separately. This feature—planned for release in the coming months—will provide channel-specific analytics to help you measure effectiveness on each platform and optimize the user experience accordingly.

## 1. 🌐 indigo.ai Web Chat

Our Web Chat allows you to **deploy your virtual assistant directly on your website or app.**&#x20;

It’s more than just a simple chat box—it's a **feature-rich widget** designed to enhance user interaction with vibrant visuals and **extensive customization options**.&#x20;

The Web Chat offers:

* **Pre-chat Engagement**: Customizable chat launcher button and pop-up message.
* **Stylish Homepage**: Interactive image grid, clickable FAQs, and a cool design.
* **Session Persistence**: Default 10-minute session duration, restoring previous messages even after page reloads.
* **Full Customization**: Tailor the assistant to reflect your brand identity.

{% embed url="https://screen.studio/share/ku0UL9ik?_loop=1&autoplay=1" %}

➡ Learn more about our Web Chat:

* [the-next-generation-web-chat.md](../../product-updates/latest-product-releases/the-next-generation-web-chat.md "mention"): Key benefits and features of the newly revamped Web Chat (released in February 2025).
* [configure-and-install-the-web-chat.md](../../build-your-ai-agents/configure-and-install-the-web-chat.md "mention"): Step-by-step instructions on configuring it in the settings section of your workspace.
* [advanced-web-chat-customization-and-installation-guide.md](../../tech-deep-dives/web-chat-integration-and-customization-on-your-website/advanced-web-chat-customization-and-installation-guide.md "mention"): Detailed article for developers describing advanced integration and installation options.&#x20;

## 2. 💼 **Web Chat Integration within CRM Platforms**

Your virtual assistant can be seamlessly integrated into the web chat interface of CRM platforms like **Zendesk, Salesforce** and **Vivocha**. In this setup, the assistant works within the CRM's web chat system, supporting existing workflows and engaging with users without disruption.

#### Key Benefits

* **AI Agents on Existing Channels**: If your team is already using a CRM’s web chat, you can integrate your AI assistant into that channel, preserving the familiar interface and workflow.
* **Human Handover**: Manage human takeover efficiently within the CRM’s system, ensuring a smooth transition from the assistant to live agents when needed.
* **Ticketing System and KB Integration**: Automatically create and update support tickets, or integrate your knowledge base directly into the CRM’s system for seamless interactions.

#### Channel-Specific Features

* **Customization**: The Web Chat widget configuration and customization options are determined by the CRM platform. However, core agent features - such as the ability to create image carousels in chat using the [Card Block](https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#card-block-structured-and-interactive-content) - are typically supported across various platforms.
* **Quick Reply Options**: The typebar cannot be disabled when [quick replies](../blocks-and-variables/action-blocks/quick-reply-block.md) (user response options via buttons) are used. Therefore, it’s important to account for the possibility that users may choose to type a response instead of clicking on the buttons.

{% hint style="info" %}
💡 **CRM Integration Options**

* indigo.ai offers a **native integration with Zendesk** for seamless deployment and support within its ecosystem.
* To integrate your virtual assistant with **other CRM platforms** (such as Salesforce), you can use our **Chat API** for full flexibility.
* If you also want your assistant to interact with the **CRM's ticketing system or knowledge base**, you'll need to set up an integration with that external system. Learn more about available integrations in this article: [integrations](../integrations/ "mention").
{% endhint %}

## 3. **📱** WhatsApp

WhatsApp is a great choice for **providing immediate support** to your users. As one of the most widely used messaging platforms globally, WhatsApp makes it easy to engage with your audience and offer on-the-go assistance.&#x20;

#### Key Features and Considerations for WhatsApp Integration

* **Customization Limitations**:
  * You cannot modify the appearance of buttons, including size, color, or icons.
  * Carousels (image sliders) are supported for interactive content.
  * There is no visual indicator (e.g., typing dots) when the assistant is preparing a response.
  * The typebar cannot be disabled when using [quick replies](../blocks-and-variables/action-blocks/quick-reply-block.md), so users may type their responses instead of clicking the buttons.
  * Button text has a limit of 20 characters, with a maximum of 3 buttons supported per message.
  * Links must be written out in full as WhatsApp doesn’t support hyperlinks.
  * Captions cannot be used for buttons or images.
* **Architecture**:\
  All WhatsApp messages are processed internally by the platform, just like messages from the web chat widget. In terms of data storage, WhatsApp (Meta) and our channel provider may store data according to their respective policies.

#### What You Need to Activate Your Virtual Assistant on WhatsApp

1. A phone number.
2. A WhatsApp Smart Business Account.
3. A Meta Business Account.
4. The phone number must be registered with Meta and associated with the WhatsApp Smart Business Account.

#### Case Study: Flou's Use of WhatsApp for Retailer Support

Flou, a furniture company with a global network of over 1,000 retailers, wanted to improve communication with its distributors. With limited direct-to-consumer sales, they opted to use a virtual assistant on WhatsApp to provide constant support to their retailers.

A typical use case: A retailer in a physical store can quickly ask the Whatsapp virtual assistant for information without needing to refer to an outdated annual catalog.&#x20;

Learn more about Flou's success [here](https://indigo.ai/it/success-stories/flou/).&#x20;

## 4. 🗣️ Voice

Our Voice Channel enables your virtual assistant to **handle conversations via voice—over the phone or, soon, directly in web chat.**

Powered by **text-to-speech (TTS)** and **speech-to-text (STT)** technologies, this channel delivers natural, fluid, and accessible interactions for users who prefer speaking over typing.

Thanks to integrations with **ElevenLabs** and **AudioCodes**, you can **personalize your assistant’s voice** to align with your brand—choosing from a range of tones, accents, and speaking styles to ensure a consistent and engaging customer experience.

{% hint style="info" %}
Learn more about this channel here: [voice.md](voice.md "mention").&#x20;
{% endhint %}

#### Key Benefits & Functionalities

* **24/7 Support**: Provide continuous support outside regular business hours, ensuring your users have assistance whenever needed.
* **Outbound Engagement**: Reach users proactively, engaging them when they’re available through voice interactions.
* **High-Quality & Low Latency**: Enjoy smooth, responsive conversations with minimal delay, improving response times and reducing waiting queues.
* **Seamless Integration**: Connect the virtual assistant with backend systems (CRM, ERP) for real-time data access, enabling complex interactions like appointment booking, FAQ handling, support ticket creation, and more—all through voice.&#x20;
* **Automated Processes**: Automate tasks that once required human agents, streamlining operations and maintaining consistency with existing workflows.
* **Accessibility**: Offer inclusive support for users who cannot type due to disabilities or literacy challenges.

#### Use Cases

* **Inbound Customer Support**: Provide instant customer service through voice interactions.
* **Outbound Surveys**: Conduct surveys via voice for gathering feedback or market research.
* **Outbound Calls for Appointment Booking**: Automate the process of qualifying hot leads and scheduling appointments with business consultants.&#x20;

#### Channel Specifics

* **Managing No Input Situations**: The voice channel requires handling situations where the user doesn’t respond or remains silent, or where the virtual assistant may not hear the user due to speaking too early or background noise.
* **Call Hang-Up**: It's important to ensure a proper termination of the call by configuring a hang-up action when the conversation ends.
* **Yes/No Replies**: STT systems struggle with short words like "yes" or "no," so it's better to avoid yes/no questions and guide the user to provide clearer, longer responses.
* **No "Quick Replies"**: Unlike other channels, where predefined options (such as buttons in web chat) may be appropriate for guiding users, it’s not ideal to restrict users to structured choices in voice interactions, as they can speak at any time and say anything.
