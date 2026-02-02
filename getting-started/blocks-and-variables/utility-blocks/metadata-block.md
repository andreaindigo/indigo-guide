---
description: Released in June 2025
---

# 🧾 Metadata Block

The Metadata Block is a Utility Block **designed specifically for voice-enabled virtual assistants**. It allows you to **insert structured metadata into your workflow using JSON format**.&#x20;

**These metadata entries are not visible to the end user, but they play a critical role behind the scenes by enabling advanced, context-aware behavior**, especially in [Voice channels](../../communication-channels/voice.md).

Whether you're integrating with external systems (like CRMs or analytics platforms), coordinating actions with analytics tools, or triggering downstream automations, the Metadata Block gives you a powerful, flexible way to pass key information through your flow.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-07 alle 14.58.16.png" alt=""><figcaption></figcaption></figure>

## Key Use Cases

* **Voice Assistant Enhancements**: Pass structured flags to control voice behavior, manage flow logic, or enable fallback handling
* **System Integrations**: Send metadata to external systems (e.g., CRM, analytics, Nebuly) at specific points in the conversation
* **Invisible Flow Annotations**: Add contextual data that modifies backend behavior without impacting user experience
* **Conditional Metadata**: Use inside conditions to send metadata only in specific scenarios

## What Are Metadata in This Context?

Metadata are structured pieces of information that describe or influence the behavior of your assistant, without being part of the conversational output.\
In the case of voice assistants, metadata can be used to:

* Pass **contextual flags** or instructions to the voice engine
* Trigger **external services or integrations** (e.g., sending data to HubSpot)
* Annotate flow steps with hidden signals or logic parameters
* Transmit **flow-level state data** not visible in chat

The assistant interprets this metadata during execution to drive additional actions, integrations, or behaviors, without altering what the user hears.

## ⚙️ How the Metadata Block Works

The Metadata Block:

* Accepts input in **valid JSON format**
* Metadata are **not printed in chat** and remain invisible to users
* They are still visible in the [**debugging**](../../workspace/activities/chats/debugging.md) **console**, allowing builders to test and trace their impact
* [Variables](../variables/) (e.g., `{{user_email}}`) can be used inside the JSON to make the metadata dynamic
* Can be conditionally executed if placed within a [**Condition Block**](../logic-blocks/condition-block.md) (N.B.: Metadata Blocks inside unverified conditions will not be processed; only blocks in satisfied conditions are executed)

### Editor Features

To support both technical and non-technical users, the Metadata Block offers **three editing modes**:

1. **Text (default)** – Plain JSON editor with syntax highlighting
2. **Tree** – A visual, collapsible structure for easier navigation
3. **Table** – Key-value table view for a spreadsheet-like editing experience

You can switch between these modes at any time depending on your comfort level and the complexity of your data.

## Best Practices

* Always validate your JSON syntax: malformed input will be ignored or could break integrations
* Use variables to keep metadata dynamic and relevant to the user's context
* Include Metadata Blocks only where necessary to avoid cluttering the workflow
* When using within Condition Blocks, be mindful of logic paths: metadata will **only be processed** when the condition is met.

***
