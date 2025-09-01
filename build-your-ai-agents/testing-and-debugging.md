---
description: Verify bot functionality and fix any issues.
icon: '4'
---

# Testing and Debugging

Thorough testing and debugging are essential steps in ensuring your AI agents perform as intended before going live. This process involves **evaluating both the final responses provided to users and the workflow sequences that lead to those responses**. By systematically testing and refining your agents, you can identify and address issues, ensuring a seamless user experience.​&#x20;

## 1. Utilize the Platform's Integrated Debugging Features

The indigo.ai platform includes a powerful debugging tool that helps you understand how each message in the chat is generated. It shows you a clear and detailed log of what happens during the conversation, including:

* The workflows the assistant went through
* Which agents were involved
* The knowledge base content (document chunks) used to answer the user
* What triggered the start of the flow
* Any reroutes or decisions made along the way.&#x20;

By reviewing these elements, you can quickly spot where things aren't working as expected and make the right changes to your workflows or agent setup.

{% hint style="info" %}
Learn more about how to use the debugging feature in detail in the next article: [debugging.md](../getting-started/workspace-sections/chats/debugging.md "mention").
{% endhint %}

## 2. Build Testing into Your Workflow Design

**Incorporating testing mechanisms directly into your workflow design** can streamline the debugging process. Consider implementing the following best practices:​

* **Conditional Debugging Messages** - Use the [Condition Block](../getting-started/blocks-and-variables/logic-blocks/condition-block.md) to **check if the environment is set to "test."** If true, configure the workflow to **display specific variable values or fixed text messages** during the conversation. This approach helps validate variable values and ensures that the workflow behaves as expected in the test environment.​
* **Prompt Blocks with Reasoning Variables** - When using prompts that return JSON to extract information from user input, it’s helpful to include a "reasoning" key in the response. This key offers visibility into how the AI agent made its decision. To make debugging easier during testing, you can add a Text Block that displays the value of the `reasoning` variable—just condition it to show only in the test environment. This gives you a clearer view of what’s happening behind the scenes and helps troubleshoot unexpected behavior.\
  For detailed guidance on utilizing reasoning in prompts, refer to this article: [prompt-block.md](../getting-started/blocks-and-variables/utility-blocks/prompt-block.md "mention").&#x20;

## 3. Testing in a Staging Environment

While the platform's Preview feature is ideal for quick, individual tests, involving others in a structured staging environment allows you to uncover issues from diverse perspectives and simulate real-world usage more accurately.

To enable **collaborative testing** before going live, you can **share controlled access to your assistant** in two ways:

* **Staging Installation**: Install the assistant in a staging environment using the [test token](../tech-deep-dives/your-project-token.md) to replicate production-like conditions.
* **Full-Page Preview**: Alternatively, generate a focused testing link by appending the [chat token](../tech-deep-dives/your-project-token.md) to this URL: `https://platform.indigo.ai/chatbot/preview/`. This creates a full-page interface ideal for streamlined external testing.

## 4. 🆕 Use the Issue Tracker for Collaborative Testing

{% hint style="warning" %}
The feature is currently in **beta**. Read more about it in the dedicated article: [issue-tracker-for-tests-and-improvements.md](../product-updates/latest-product-releases/issue-tracker-for-tests-and-improvements.md "mention")
{% endhint %}

Manual testing using the platform’s preview feature is a great starting point, but the real power of structured, collaborative testing lies in the **Issue Tracker**.

The Issue Tracker replaces the need for external spreadsheets by allowing testers to flag and document issues directly within the platform.

#### Here’s how to use it:

* **Flag issues from** [**Chats**](../getting-started/workspace-sections/chats/#issue-creation) **or the AI Preview:** During testing or review, hover over any message to create an issue. You can specify a title, description, priority, tags (e.g., Bug, Improvement), and assign it to a team member or your indigo.ai Customer Success Manager.
* [**Dashboard View**](../getting-started/workspace-sections/issue-tracker.md)**:** All flagged issues are collected in a centralized dashboard where you can sort, filter, and manage them based on priority, tag, assignee, or status.
* **Comment and Track Progress:** Use the dashboard to leave comments, track status updates, and ensure every issue is followed through to resolution.

This built-in system brings structure and speed to your testing process, making it easier to collect and act on feedback.

## 5. Implement Feedback Collection Workflows (For Advanced Users)

If you want to gather feedback from users during their interaction with the virtual assistant, directly in the chat, you can create a dedicated workflow for that.

**How it works:**

1. **Feedback Workflow**: Create a feedback request workflow composed of a [quick reply block](../getting-started/blocks-and-variables/action-blocks/quick-reply-block.md) asking users to rate the interaction with a 👍 or 👎. If the user selects 👎, ask them to provide additional details about what didn’t work or what they were expecting instead.&#x20;
2. **Feedback Workflow Routing**: At the end of the conversation flow you wish to evaluate, include a [reroute block](../getting-started/blocks-and-variables/logic-blocks/reroute-block.md) to direct users to the feedback collection workflow.​
3. **Data Integration**: Utilize integrations with tools like Zapier (note: requires an account) to **automatically save feedback data** into a Google Sheet or another database. Zapier can capture various parameters, including the conversation transcript, timestamp, and user-provided feedback, compiling them into a structured format for analysis.​&#x20;

{% hint style="warning" %}
Things to Keep in Mind:

* **User Experience Considerations**: Be mindful that **interrupting the conversation to request feedback** can disrupt the user experience. Use this approach selectively to avoid diminishing user engagement.​
* **Complex Setup**: Integrating with external tools like Zapier involves additional configuration and maintenance. If you require assistance setting up this integration, please [reach out](../need-help/our-customer-success-team.md) for guidance.​
{% endhint %}
