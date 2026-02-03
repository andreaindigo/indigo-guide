---
icon: share-nodes
---

# Blocks

## Workflow Blocks

Our platform offers **4 types of workflow blocks:**

1. [**Message blocks**](message-blocks/) allow you to **deliver static content**, such as **text, images, videos, or cards**, to the user at specific points in the conversation flow, providing engaging, structured content that follows a predefined format.&#x20;
2. [**Action blocks**](action-blocks/) allow both users and the virtual assistant to **perform specific actions within the conversation flow,** such as sending emails, selecting from multiple predefined options, uploading documents, speaking with a human operator, **ending a voice call**, or **transferring a call** to an external number.
3. [**Logic blocks**](logic-blocks/) allow you to **control and shape the flow of the conversation based on conditions, user inputs, or data from external systems**. They enable your virtual assistant to make decisions, collect and process information, assign values, and connect with APIs—ensuring dynamic, responsive, and intelligent conversational experiences.
4. [**Utility blocks**](utility-blocks/) support behind-the-scenes functionality by enhancing how your assistant processes information and how your team collaborates. They include **tools for generating structured outputs with AI** (like **prompts**) and for **adding internal documentation within workflows** (like notes), helping you build more organized and intelligent assistants.

## Blocks Overview

Below is an overview of the available blocks, along with links to dedicated articles that provide detailed descriptions of their functionalities:

<table><thead><tr><th width="119.4296875">Block Type</th><th width="140.34765625">Block Title</th><th>Description</th></tr></thead><tbody><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#text-block-sending-predefined-messages"><strong>Text</strong></a></td><td>Sending predefined messages</td></tr><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#image-block-visual-content-to-enhance-conversations"><strong>Image</strong></a></td><td>Displaying visual content</td></tr><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#card-block-structured-and-interactive-content"><strong>Card</strong></a></td><td>Presenting structured, interactive content</td></tr><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#video-block-multimedia-content"><strong>Video</strong></a></td><td>Embedding multimedia content</td></tr><tr><td>Action</td><td><a href="action-blocks/mail-block.md"><strong>Mail</strong></a></td><td>Sending emails as part of the conversation flow</td></tr><tr><td>Action</td><td><a href="action-blocks/quick-reply-block.md"><strong>Quick Reply</strong></a></td><td>Providing predefined options for users to quickly select from</td></tr><tr><td>Action</td><td><a href="action-blocks/upload-block.md"><strong>Upload</strong></a></td><td>Allowing users to upload files directly in the conversation</td></tr><tr><td>Action</td><td><a href="action-blocks/handover-block.md"><strong>Handover</strong></a></td><td>Seamlessly transferring the conversation to a human operator</td></tr><tr><td>Action</td><td><a href="action-blocks/api-block.md"><strong>API</strong></a></td><td>Sends or receives real-time data from external systems via API</td></tr><tr><td>Action</td><td><a href="action-blocks/hang-up-block.md">Hang up</a></td><td>Terminates a voice call and optionally triggers a post-call workflow.</td></tr><tr><td>Action</td><td><a href="action-blocks/transfer-call-block.md">Transfer</a></td><td>Transfers a voice call to an external number with waiting and fallback management.</td></tr><tr><td>Logic</td><td><a href="logic-blocks/reroute-block.md"><strong>Reroute</strong></a></td><td>Redirects the conversation to a different agent or workflow</td></tr><tr><td>Logic</td><td><a href="logic-blocks/condition-block.md"><strong>Condition</strong></a></td><td>Branches the flow based on conditional logic and variable values</td></tr><tr><td>Logic</td><td><a href="logic-blocks/capture-block.md"><strong>Capture</strong></a></td><td>Collects user input and stores it in a variable</td></tr><tr><td>Logic</td><td><a href="logic-blocks/set-values-block.md"><strong>Set Values</strong></a></td><td>Assigns or resets the value of a variable</td></tr><tr><td>Utility</td><td><a href="utility-blocks/prompt-block.md"><strong>Prompt</strong></a></td><td>Uses AI to generate structured data or intelligent responses from user input</td></tr><tr><td>Utility</td><td><a href="utility-blocks/notes-block.md"><strong>Notes</strong></a></td><td>Adds internal comments to keep workflows organized</td></tr></tbody></table>

## Variables

Variables are the foundation of most workflow blocks. They allow your assistant to **store, recall, and act on data—enabling everything from dynamic conversations to API-based responses**. Whether you're capturing user input, setting conditions, or generating structured outputs, variables power the logic behind your assistant’s behavior.

{% hint style="info" %}
Learn more about how variables work in the next section: [variables](../workspace/variables/ "mention").
{% endhint %}
