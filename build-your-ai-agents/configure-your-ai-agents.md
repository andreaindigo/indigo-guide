---
description: Set up agents, workflows, features and preferences for optimal performance.
icon: '3'
---

# Configure Your AI Agents

​Configuring AI Agents on the indigo.ai platform is a streamlined process designed to be accessible to users without requiring advanced technical skills. By leveraging the platform's intuitive interface, you can design, customize, and deploy AI Agents that elevate customer interactions and optimize business operations.&#x20;

{% hint style="info" %}
This article offers practical guidance to help you get started. For a complete reference on each configuration field and the functionality of all workflow blocks, refer to this detailed pages of the guide: [Broken link](broken-reference "mention"), [blocks-and-variables](../getting-started/blocks-and-variables/ "mention").&#x20;
{% endhint %}

## Getting Started in Your Workspace

Once inside your workspace, head to the configuration area, the central hub for building and managing your AI Agents. This space is divided into two separate environments:

* **Draft** **Area**: Work in progress, agents and workflows created here are inactive.
* **Live** **Area**: Active agents and workflows powering your virtual assistant.

You can start directly in the Live Area to design your conversational experiences, allowing you to test your configurations in real time as you build.

Use the **+ button** to create new agents or workflows, and organize them into **folders** based on the **topics your assistant should handle** (e.g., "Orders," "Returns," "Product Recommendations"). This structure helps maintain clarity and scalability as your assistant evolves.

## Test vs. Live Environment

As you configure your AI assistant, always work within the Test Environment. This environment is **automatically updated with every change you make** and is visible via the **Preview** button at the top-right of your workspace. It allows you to safely test and refine how your assistant behaves before making it publicly available.&#x20;

Once you're confident with the configuration and the assistant is performing as expected, click **Publish**. This action moves your latest version to the **Live Environment**, where it becomes available to end users.

This approach ensures a safe, iterative development process where you can build and optimize your AI assistant without affecting the user experience until you're ready.

## Start from the Essentials

Every workspace includes two key elements by default:

* **Welcome Workflow**: determining the first interaction with users.&#x20;
* **General Agent**: The fallback agent that handles all general queries and small talk.

We recommend starting your configuration from these two elements.&#x20;

### 👮 The General Agent

The **General Agent** is a foundational component of every workspace on the indigo.ai platform. It acts as a **fallback mechanism**, ensuring users always receive a meaningful response, even when their requests don’t match any specialized agents.

This agent is **automatically included in all new workspaces** and plays a crucial role in maintaining smooth, uninterrupted conversations. It should **never be deleted** and should always be **customized** to reflect your brand voice and support goals.

**Purpose & Functionality**

The General Agent is designed to:

* Handle **general FAQs**, casual chats, and ambiguous requests.
* Intercept and respond to **queries that don’t match any other agent’s scope**.
* Detect and professionally manage **trolling or inappropriate behavior**.
* Act as a safety net to **keep the conversation flowing**, regardless of user intent.

Whether the user is asking about your company mission, making small talk, or asking something unclear, the General Agent ensures they’re met with a helpful, consistent reply.

**Configuration Tips & Best Practices**

For detailed guidance on how to configure the General Agent and other AI agents, refer to this article: [how-to-create-an-agent.md](../getting-started/agents-workflows-and-triggers/how-to-create-an-agent.md "mention"). There, you’ll find:

* A template for filling out the **Agent Description** and **Agent Goal** sections.
* Best practices for setting up **general rules** (e.g., how to handle trolling, unsupported requests, or off-topic messages).
* Tips on defining and reusing **variables,** such as your company description or tone of voice, starting from the General Agent and applying them consistently across specialized agents.

Customizing your General Agent ensures it represents your brand effectively while covering all the gaps left by topic-specific agents.

### 👋 The Welcome Workflow

The Welcome Workflow is a built-in, non-deletable, non-renamable component of every indigo.ai workspace. It defines what happens when a user opens the chat: essentially, it's **the starting point of every new conversation**.

By default, this workflow contains a **standard static welcome message**, which you can customize using the platform’s workflow blocks. Like any other workflow, it can be edited to reflect your assistant's personality and objectives.

#### Default Trigger

The Welcome Workflow is automatically triggered at the **start of a conversation**. It's your assistant's first impression, an opportunity to:

* **Introduce itself** (e.g., name and role)
* **Clarify what it can help with** (e.g., “I'm here to assist you with orders, returns, and book recommendations!”)
* **Guide users** toward the most useful queries or features

#### Best Practice: Initialize Variables

A key use of the Welcome Workflow is to **initialize all variables** at the beginning of the user interaction. This ensures each new conversation starts with a clean slate, without any leftover data from previous sessions.

* Use the **Set Values Block** to reset all variables used across your workspace.
* Specify whether a variable should be cleared (e.g., `= null`, `= false`, `= empty`) or initialized with a specific value.

{% hint style="info" %}
When resetting or initializing variables, it's best practice to explicitly set them to either `null` OR `empty`
{% endhint %}

#### Final Checklist

Once your assistant is fully configured, revisit the Welcome Workflow and ensure:

* All workspace variables are included and properly initialized.
* Any new variables added during development are accounted for.
* Your welcome message sets the right tone and expectations for the user.

## Best Practices for Agent & Workflow Configuration

#### Start from the Goal and Build Backwards

Before diving into blocks and flows, make sure you’re clear on the **end goal** of the interaction: what answer the assistant needs to provide or what action it should trigger.\
From there, design the **skeleton of the conversation** using the core workflow blocks, laying out the main steps that lead to that goal.\
Start simple and only add detail once the core structure is in place. Don’t build a full flow unless you already know when and why it will be triggered.

#### Use Triggers Thoughtfully

As mentioned in [agents-workflows-and-triggers](../getting-started/agents-workflows-and-triggers/ "mention"), a trigger should only be configured if the workflow is a primary process that the mother agent will delegate user requests to. If the workflow is secondary or supports other processes, a trigger is unnecessary.

#### Set Initial Variables

At the beginning of each workflow, use the [Set Values](../getting-started/blocks-and-variables/logic-blocks/set-values-block.md) block to initialize variables. This avoids accidentally carrying over values from previous user sessions.

#### Define a Clear End

* For agents, define what happens after their response using the Connection section.
* For workflows, always end with a [Reroute Block](../getting-started/blocks-and-variables/logic-blocks/reroute-block.md) that redirects the flow to another agent or process.
* Also consider resetting variables at the end of a flow, unless you explicitly need to retain their values for subsequent steps.

#### Streamline User Journeys

Minimize the number of steps a user needs to take to reach their goal. Avoid asking for information that’s already been provided.\
For example:

* If the user includes their order number in the first message, the assistant should **extract it proactively** rather than asking again.
* When escalating a case, **analyze the conversation history** to collect all relevant details instead of repeating questions.

Use techniques like:

* **Prompt blocks** to collect multiple values in one go.
* **Conditional checks** to detect and use data already mentioned in the conversation.
* **Reuse Existing Components**

To save time and ensure consistency, [duplicate existing blocks](https://indigo-ai.gitbook.io/indigo.ai-guide/product-updates/latest-product-releases/workspace-updates#id-4.-copy-paste-blocks) when only minor changes are needed. This is especially helpful when creating variants of similar experiences.

#### Number Your Workflow Steps

For longer workflows, number the blocks or steps (e.g., Step 1, Step 2…) to maintain a clear sequence and avoid confusion during design or editing.

#### Centralize Shared Logic

If a specific action or sequence needs to be repeated in multiple flows, centralize it in a single workflow (e.g., a “Utility” folder) and use Reroute blocks to direct users there when needed.\
This helps maintain consistency and makes updates easier—change it once, and the update applies everywhere.
