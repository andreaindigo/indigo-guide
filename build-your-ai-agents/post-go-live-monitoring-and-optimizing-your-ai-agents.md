---
icon: '6'
---

# Post-Go-Live: Monitoring and Optimizing Your AI Agents

Congratulations on deploying your AI agents! However, the journey doesn't end here. To ensure your virtual assistant continues to meet user expectations and business objectives, it's crucial to engage in **continuous monitoring and optimization**. This guide outlines best practices for post-deployment management.

## Ongoing Testing and Feedback Collection

Once your assistant is live and handling a high volume of conversations, your focus should shift to **analyzing real user interactions**. Reviewing actual chats helps you assess whether responses are accurate, relevant, and helpful.&#x20;

Use the [**Chat section**](../getting-started/workspace-activities/chats/) in the platform to browse conversation history and take advantage of the [debugging tools](../getting-started/workspace-activities/chats/debugging.md) to trace how each response was generated. You can also apply the structured feedback collection process outlined in our pre-go-live testing guide: [testing-and-debugging.md](testing-and-debugging.md "mention").&#x20;

Categorize issues by type and priority, then act quickly: adjust workflows and **publish updates** to continuously improve the user experience in your production environment.

## Monitoring Performance Metrics

Leverage analytics to gain insights into your assistant's performance. Key metrics to monitor include:​

* 👍 **Thumbs Up** **/** 👎 **Thumbs Down** **Feedback** **:** Review **conversations that received negative feedback** to understand user dissatisfaction.​
* **Agent Performance:** Identify which agents are most frequently triggered and those associated with negative feedback. This helps pinpoint **topics that require attention**.​
* **Human Handover Instances:** If human intervention is enabled, monitor **how often and why conversations are escalated to human agents**. Analyzing these instances can reveal areas where the virtual assistant needs improvement.​
* **User Satisfaction (CSAT):** At the end of a conversation, **users can rate their experience** using a five-point emoji scale. Keep in mind that response rates are typically low and tend to capture more negative feedback, as users are more likely to respond when dissatisfied. [Contact us](../need-help/our-customer-success-team.md) for strategies to encourage more user participation in CSAT surveys.​

For a detailed explanation of analytics data and metrics, refer to this section of our platform guide: [analytics.md](../getting-started/workspace-activities/analytics.md "mention").&#x20;

## Implementing Improvements

Once you’ve analyzed user feedback - especially negative responses - it’s time to take targeted action to enhance your assistant’s performance. Depending on the type of issue, here’s how you can respond:

**Misclassification**

When the assistant provides an incorrect or unrelated answer:

* **Retrain the Assistant**: Improve the affected agents or workflows so that the virtual assistant associates the query with the correct response.
* **Add New Content**: If the query isn't covered at all, consider creating a new agent—but only if it's a recurring question.
* **Build a Workflow**: If the request is too complex for a single answer, design a dedicated conversational flow to guide the user step-by-step.&#x20;

**Incomplete Responses**

When the assistant gives a correct but insufficient answer:

* **Enhance Existing Replies**: Enrich the current content with more details to fully address the user’s needs and expectations.

**External Factors (Exogenous Feedback)**

When feedback is negative despite a correct response, it may be due to issues outside the assistant's control:

* **Monitor for Patterns**: Review this type of feedback regularly to spot trends related to product, service, or usability problems that might require action beyond the assistant.

## Regular Performance Reviews with indigo.ai Customer Success Team

Depending on your contract type, we offer **ongoing support** and **recurrent performance reviews**.&#x20;

Our [Customer Success team](../need-help/our-customer-success-team.md) will schedule regular meetings to analyze your AI assistant's performance, gather insights on user interactions, and identify opportunities for improvement.​&#x20;
