---
icon: share-nodes
---

# Blocks & Variables

As explained in article [agents-workflows-and-triggers](../agents-workflows-and-triggers/ "mention"), workflows are **conversational paths that define how the chatbot responds to specific questions and manages various scenarios**. They are used to validate user responses, determine how to reply, and define conditions that trigger different responses based on user input, among other things.

Workflows are **structured processes that guide how the virtual assistant interacts with users**. Before an agent responds or the assistant takes action, the workflow ensures all necessary steps are followed. These steps are designed to react to both direct (explicit) and indirect (implicit) user inputs.&#x20;

Some examples of workflows include:

* **Product Recommendation** Workflow: User requests the best product → bot retrieves and filters options from the catalog → best-fit product is passed to the agent → agent shares the recommendation.
* **Customer Support** Workflow: User asks to connect with a human → workflow gathers conversation history and user details → bot connects with the CRM → support ticket is created and confirmed to the user.

Workflows are the backbone of complex virtual assistants, yet building them is simple and intuitive.&#x20;

In your workspace, you can easily **drag and drop** workflow components from the available **blocks**, making workflow creation both intuitive and flexible.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-07 alle 14.46.02.png" alt=""><figcaption></figcaption></figure>

## 🎯 Workflow Trigger

The workflow trigger functions similarly to an agent trigger, determining **when the workflow should begin (entry point)**. This ensures smooth integration with other parts of your bot.&#x20;

As mentioned in [agents-workflows-and-triggers](../agents-workflows-and-triggers/ "mention"), a trigger should only be configured if the workflow is a primary process that the mother agent should delegate user requests to. For secondary workflows or those supporting other processes, triggers are unnecessary; these workflows can be activated in an alternative way, using a [reroute block](logic-blocks/reroute-block.md).

{% hint style="info" %}
For detailed guidance on creating workflows and building your virtual assistant, refer to this article: [Broken link](broken-reference "mention").
{% endhint %}

**What You Can Specify in the Trigger:**

* **Trigger Details** – Define when the workflow should activate.
* **Example Questions** – List common user queries that should trigger this workflow, helping refine its activation conditions.

Additionally, there is a toggle switch that allows you to **enable or disable the trigger**. This is particularly useful during testing. If a trigger is configured, make sure it is enabled to prevent unexpected behavior.

create an example of a trigger for a workflow that guides the user to find the closes store available to an indicated location.&#x20;

<details>

<summary><strong>Workflow Example</strong></summary>

**Store Finder Workflow**

* **Trigger Details**: When a user asks for the nearest store to a specific location.
* **Example User Questions**:
  * "Where is the closest store?"
  * "Can you find a store near me?"
  * "Find the nearest Lumine Jewels store."
  * "Show me the closest store to Milan."

</details>

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-24 alle 18.19.01.png" alt="" width="485"><figcaption><p>Trigger configuration</p></figcaption></figure>

## Top Section & Settings

The settings in the top right corner of the workflow area are identical to those found in the agent area.\
This section provides key information and settings to define and optimize your virtual assistant's behavior, helping you configure and fine-tune its performance.

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-24 alle 18.20.20.png" alt=""><figcaption><p>Top Section of the Worfklow Area</p></figcaption></figure>

#### Workflow Name

The workflow name should be **clear and descriptive**, making its purpose immediately obvious.

Example:&#x20;

* ✅ “Store Locator Workflow” (clearly indicates that the workflow helps users find nearby stores)
* ❌ "Search Workflow" (too vague)

#### Last Modified Information

This section automatically displays details about who last modified the workflow and when the modification occurred for version tracking.

#### Settings (Top Right Button)

The Settings menu includes essential toggles that define how users interact with the assistant.

<figure><img src="../../.gitbook/assets/Screenshot 2025-02-26 alle 09.14.22.png" alt="" width="250"><figcaption><p>Settings</p></figcaption></figure>

#### User Feedback Toggle

The User Feedback Toggle **allows users to rate the agent’s responses with a thumbs-up or thumbs-down option**. When enabled, a feedback request appears at the end of each response.&#x20;

Based on user reactions, the agent can connect to different workflows: a positive rating can trigger another agent or workflow, such as offering follow-up suggestions, while a negative rating can prompt a response, ask clarifying questions, or redirect the user to a human agent.

{% hint style="info" %}
As a best practice, it is recommended to disable feedback requests for intermediate workflows and secondary agents, ensuring that **feedback is collected only on final responses** rather than on clarification steps or data collection prompts.
{% endhint %}

{% hint style="info" %}
📊 Want to learn more about collecting and analyzing feedback? Check out our Analytics guide: [analytics.md](../workspace-sections/analytics.md "mention").&#x20;
{% endhint %}

#### Typebar Settings&#x20;

The Typebar toggle lets you control how users interact with the agent:

* **Disabled: Users can only choose from pre-set buttons (useful for structured flows).**&#x20;
* Enabled: Users can freely type their queries. If the typebar is enabled, you can add multiple placeholder texts (separated by commas), which will be displayed randomly to guide user input.

## Workflow Blocks

Our platform offers **4 types of workflow blocks:**

1. [**Message blocks**](message-blocks.md) allow you to **deliver static content**, such as **text, images, videos, or cards**, to the user at specific points in the conversation flow, providing engaging, structured content that follows a predefined format.&#x20;
2. [**Action blocks**](action-blocks/) allow both users and the virtual assistant to **perform specific actions within the conversation flow,** such as sending emails, selecting from multiple predefined options, uploading documents, speaking with a human operator, **ending a voice call**, or **transferring a call** to an external number.
3. [**Logic blocks**](logic-blocks/) allow you to **control and shape the flow of the conversation based on conditions, user inputs, or data from external systems**. They enable your virtual assistant to make decisions, collect and process information, assign values, and connect with APIs—ensuring dynamic, responsive, and intelligent conversational experiences.
4. [**Utility blocks**](utility-blocks/) support behind-the-scenes functionality by enhancing how your assistant processes information and how your team collaborates. They include **tools for generating structured outputs with AI** (like **prompts**) and for **adding internal documentation within workflows** (like notes), helping you build more organized and intelligent assistants.

## Variables

Variables are the foundation of most workflow blocks. They allow your assistant to **store, recall, and act on data—enabling everything from dynamic conversations to API-based responses**. Whether you're capturing user input, setting conditions, or generating structured outputs, variables power the logic behind your assistant’s behavior.

{% hint style="info" %}
Learn more about how variables work in the next section: [variables](variables/ "mention").
{% endhint %}

## Blocks Overview

Below is an overview of the available blocks, along with links to dedicated articles that provide detailed descriptions of their functionalities:

<table><thead><tr><th width="119.4296875">Block Type</th><th width="140.34765625">Block Title</th><th>Description</th></tr></thead><tbody><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#text-block-sending-predefined-messages"><strong>Text</strong></a></td><td>Sending predefined messages</td></tr><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#image-block-visual-content-to-enhance-conversations"><strong>Image</strong></a></td><td>Displaying visual content</td></tr><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#card-block-structured-and-interactive-content"><strong>Card</strong></a></td><td>Presenting structured, interactive content</td></tr><tr><td>Message</td><td><a href="https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables/message-blocks#video-block-multimedia-content"><strong>Video</strong></a></td><td>Embedding multimedia content</td></tr><tr><td>Action</td><td><a href="action-blocks/mail-block.md"><strong>Mail</strong></a></td><td>Sending emails as part of the conversation flow</td></tr><tr><td>Action</td><td><a href="action-blocks/quick-reply-block.md"><strong>Quick Reply</strong></a></td><td>Providing predefined options for users to quickly select from</td></tr><tr><td>Action</td><td><a href="action-blocks/upload-block.md"><strong>Upload</strong></a></td><td>Allowing users to upload files directly in the conversation</td></tr><tr><td>Action</td><td><a href="action-blocks/handover-block.md"><strong>Handover</strong></a></td><td>Seamlessly transferring the conversation to a human operator</td></tr><tr><td>Action</td><td><a href="action-blocks/api-block.md"><strong>API</strong></a></td><td>Sends or receives real-time data from external systems via API</td></tr><tr><td>Action</td><td><a href="action-blocks/hang-up-block.md">Hang up</a></td><td>Terminates a voice call and optionally triggers a post-call workflow.</td></tr><tr><td>Action</td><td><a href="action-blocks/transfer-call-block.md">Transfer</a></td><td>Transfers a voice call to an external number with waiting and fallback management.</td></tr><tr><td>Logic</td><td><a href="logic-blocks/reroute-block.md"><strong>Reroute</strong></a></td><td>Redirects the conversation to a different agent or workflow</td></tr><tr><td>Logic</td><td><a href="logic-blocks/condition-block.md"><strong>Condition</strong></a></td><td>Branches the flow based on conditional logic and variable values</td></tr><tr><td>Logic</td><td><a href="logic-blocks/capture-block.md"><strong>Capture</strong></a></td><td>Collects user input and stores it in a variable</td></tr><tr><td>Logic</td><td><a href="logic-blocks/set-values-block.md"><strong>Set Values</strong></a></td><td>Assigns or resets the value of a variable</td></tr><tr><td>Utility</td><td><a href="utility-blocks/prompt-block.md"><strong>Prompt</strong></a></td><td>Uses AI to generate structured data or intelligent responses from user input</td></tr><tr><td>Utility</td><td><a href="utility-blocks/notes-block.md"><strong>Notes</strong></a></td><td>Adds internal comments to keep workflows organized</td></tr></tbody></table>
