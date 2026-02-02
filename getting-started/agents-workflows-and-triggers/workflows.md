---
description: >-
  Learn more about our intelligent agents and triggers that initiate
  interactions.
---

# Workflows

Workflows are **conversational paths that define how the chatbot responds to specific questions and manages various scenarios**. They are used to validate user responses, determine how to reply, and define conditions that trigger different responses based on user input, among other things.

Workflows are **structured processes that guide how the virtual assistant interacts with users**. Before an agent responds or the assistant takes action, the workflow ensures all necessary steps are followed. These steps are designed to react to both direct (explicit) and indirect (implicit) user inputs.&#x20;

Workflows represent a **step-by-step process that must be completed before an agent responds or the virtual assistant takes action**.

While it's mandatory to configure at least one agent, workflows are **optional** and can be implemented as needed. For simple setups, you can build a virtual assistant composed solely of agents.&#x20;

However, for more complex scenarios, workflows become essential. For example:&#x20;

* **Product Recommendation** Workflow: User requests the best product → virtual assistant retrieves and filters options from the catalog → best-fit product is passed to the agent → agent shares the recommendation.
* **Customer Support** Workflow: User asks to connect with a human → workflow gathers conversation history and user details → virtual assistant connects with the CRM → support ticket is created and confirmed to the user.

### Building a workflow

Workflows are the backbone of complex virtual assistants, but building them is simple.&#x20;

In your workspace, you can easily **drag and drop** workflow components from the available **blocks**, making workflow creation both intuitive and flexible.

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-24 alle 15.32.39.png" alt=""><figcaption><p>The Workflow Area and Its Building Blocks</p></figcaption></figure>

{% hint style="info" %}
Find detailed information about workflow building blocks here: [blocks-and-variables](../blocks-and-variables/ "mention")
{% endhint %}



## 🎯 Workflow Trigger

The workflow trigger functions similarly to an agent trigger, determining **when the workflow should begin (entry point)**. This ensures smooth integration with other parts of your bot.&#x20;

As mentioned in [.](./ "mention"), a trigger should only be configured if the workflow is a primary process that the mother agent should delegate user requests to. For secondary workflows or those supporting other processes, triggers are unnecessary; these workflows can be activated in an alternative way, using a [reroute block](../blocks-and-variables/logic-blocks/reroute-block.md).

{% hint style="info" %}
For detailed guidance on creating workflows and building your virtual assistant, refer to this article: [Broken link](/broken/pages/DQeY10e3ZGK3N4RsW0lq "mention").
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
📊 Want to learn more about collecting and analyzing feedback? Check out our Analytics guide: [analytics.md](../workspace-activities/analytics.md "mention").&#x20;
{% endhint %}

#### Typebar Settings&#x20;

The Typebar toggle lets you control how users interact with the agent:

