---
description: Released in March 2025
---

# Workspace Updates - Q1 2025

We are thrilled to introduce exciting updates in the new version of our platform, designed to make **building and managing AI agents faster, easier, and more flexible than ever**.&#x20;

These updates give you more visibility, control, and efficiency as you create conversational experiences.

Here’s a quick look at what’s new:

1. [**Debugging**](https://indigo-ai.gitbook.io/indigo.ai-guide/product-updates/new-product-releases/a-new-version-of-our-platform/workspace-updates#id-1.-debugging): Visualize, step by step, what happens inside your agents and workflows—track variables, prompt history, API responses, and more to easily **troubleshoot and resolve issues**.
2. [**New Mail Block**](https://indigo-ai.gitbook.io/indigo.ai-guide/product-updates/new-product-releases/a-new-version-of-our-platform/workspace-updates#id-2.-new-mail-block): **Send personalized emails directly from your workflow** without needing to configure an external API—simple, fast, and fully integrated.
3. [**New Upload Block**](https://indigo-ai.gitbook.io/indigo.ai-guide/product-updates/new-product-releases/a-new-version-of-our-platform/workspace-updates#id-3.-upload-block): Let **users upload files directly in the chat**. Use uploaded content as workflow variables for follow-up actions like database storage or email.
4. [**Copy-Paste Blocks**](https://indigo-ai.gitbook.io/indigo.ai-guide/product-updates/new-product-releases/a-new-version-of-our-platform/workspace-updates#id-4.-copy-paste-blocks): Speed up building by **copying and pasting blocks** within or across workflows, saving time and maintaining consistency.&#x20;

Let’s explore how each of these features helps you build better virtual assistants.&#x20;

## 1. Debugging

One of the standout new features in this version of the platform is the debugging tool, designed to help you **troubleshoot and fine-tune your AI agents with ease**.&#x20;

The debugging tool allows you to **see exactly what happens at each step when an agent processes a message from a user**.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-27 alle 16.03.35.png" alt=""><figcaption></figcaption></figure>

Here's how it works:

* **Detailed Step-by-Step Breakdown**: You can now track the flow of variables, prompts, and API calls as they move through your agents and workflows.
* **Track Transformations and Responses**: You’ll be able to see how variables change, what data is processed, and the exact responses from external API calls.
* **Metrics at Your Fingertips**: In addition to tracking logic, you can also view data like the number of tokens used and response times, giving you a complete picture of the performance of your agent.

This tool is invaluable for advanced users who need to ensure that their agents are working correctly and efficiently. It also helps quickly pinpoint any issues, making it easier to improve the quality of your virtual assistant.

{% hint style="info" %}
Learn more about the new feature in our detailed article: [debugging.md](../../getting-started/workspace/activities/chats/debugging.md "mention").
{% endhint %}

## 2. New Mail Block

Another useful addition is the Mail Block, which simplifies the process of **sending personalized emails directly from your workflow**. Previously, sending emails required setting up an external API or service, but now it’s as easy as dragging and dropping the new Email Block into your workflow.

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-25 alle 17.01.54.png" alt=""><figcaption></figcaption></figure>

* **Automatic Email Sending**: The Email Block allows you to automatically send emails at specific points in your workflow, based on user actions or system triggers.&#x20;
* **Customizable Content**: The email content can be fully personalized based on the user’s data, ensuring a tailored communication experience.&#x20;
* **Streamlined Setup**: This new feature removes the need for complex API configurations, saving you time and effort while making email functionality much more accessible.

{% hint style="info" %}
For more details about the new block, check out the full article here: [mail-block.md](../../getting-started/blocks-and-variables/action-blocks/mail-block.md "mention").&#x20;
{% endhint %}

## 3. Upload Block

The Upload Block **allows users to upload files**—such as documents, images, or PDFs—directly within the chat **during a conversation with your virtual assistant**. It’s ideal for use cases like customer support, onboarding, or any interaction where sharing documents is required.

{% embed url="https://screen.studio/share/BR69CfUA?_loop=1&autoplay=1" %}

#### Key Features

* **Easy File Upload**\
  Users will see a **simple interface** within the chat where they can upload files. **Uploaded files become** [**variables**](../../getting-started/blocks-and-variables/variables/) within your workflow, allowing you to store them, use them in logic flows, or forward them to external systems.
* **Custom Workflow Placement**\
  You can insert the Upload Block at any point in your workflow, customizing the moment and context in which file sharing is enabled to match your business logic.
* **File Access & Reuse**\
  **Uploaded files can be viewed, downloaded, or reused in downstream workflows** directly from the [Chat section](../../getting-started/workspace/activities/chats/) of the workspace. This allows you to incorporate uploaded content into subsequent actions or decision points within your assistant's logic.
* **Operator File Sharing**\
  **Human operators can also upload and send files during a live chat**. After taking over a conversation from the virtual assistant, an operator can attach and deliver documents directly to the user, ensuring seamless, real-time support.

The Upload Block is already being used successfully in customer support and other workflows that require file sharing.&#x20;

{% hint style="info" %}
For more details and how to implement it, check out our deep dive article here: [upload-block.md](../../getting-started/blocks-and-variables/action-blocks/upload-block.md "mention").&#x20;
{% endhint %}

## 4. Copy-Paste Blocks

This feature is a simple yet powerful improvement that allows you to **copy and paste blocks within the same workflow, across different workflows, and even between different workspaces**.

{% embed url="https://screen.studio/share/8azapG9p?_loop=1&autoplay=1" %}

* **Quick and Easy**: Simply click 'Copy' on any block, and then use CMD+V (or the equivalent shortcut) to paste it into the desired workflow.
* **Time-Saving**: This functionality significantly reduces the time spent recreating blocks and ensures consistency across workflows and workspaces.
