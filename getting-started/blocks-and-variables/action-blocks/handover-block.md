# 🤝 Handover Block

Efficiently **handle sensitive requests** by **transferring the conversation to a human operator** when needed. The Handover feature ensures a seamless transition from automated responses to human assistance, enhancing customer satisfaction and overall service quality.

The Handover Block is designed to manage requests that require further support beyond the capabilities of the virtual assistant. It enables a smooth handoff from the AI agent to a human operator, who can directly take over the conversation through the dedicated functionality in the chat section of our platform.&#x20;

{% hint style="info" %}
To learn more about how to take over conversations, refer to the guide for the chat area in our platform here: [chats](../../workspace/activities/chats/ "mention").
{% endhint %}

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-25 alle 18.29.50.png" alt=""><figcaption><p>The Handover Block</p></figcaption></figure>

## Customizable Sections

* **Waiting Message**: The message displayed by the AI Agent while the operator is about to respond.
* **Operator Availability**: Inform customers about the availability of the operator. You can add multiple dates and times for availability by clicking the "Add Time" button at the top right.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-25 alle 19.43.28.png" alt=""><figcaption></figcaption></figure>

* **No Operator Available**: A message shown when no operator is online.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-25 alle 19.44.18.png" alt=""><figcaption></figcaption></figure>

* **Contact Center Closed**: A message informing the customer that the support center is closed for the day.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-25 alle 19.39.41.png" alt=""><figcaption></figcaption></figure>

### Quick Replies and Workflow Integration

In cases where no operator is available, or the support center is closed, you can integrate [**Quick Replies**](quick-reply-block.md) into the Handover Block. This allows you to connect the user’s reply to another workflow or agent, such as collecting user details (e.g., name, email, phone number) to be contacted later by the support team.

### Notifications and Alerts

The Notification button in the Handover Block opens a dropdown menu where you can add email addresses that will receive notifications whenever the block is activated. Operators will be notified via a **sound alert in the browser tab** and **receive an email** with a call-to-action that takes them directly to the chat needing assistance.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-25 alle 19.38.34.png" alt="" width="226"><figcaption><p>Notification Options</p></figcaption></figure>

## Common Use Cases

* **Complex Requests:**\
  Some questions may require a human agent, such as technical issues or complex inquiries. The Handover Block ensures that these requests are quickly passed to a qualified operator, enhancing the user experience.
* **Assistance with Sensitive Information**:\
  When users need to share sensitive or personal information, such as financial details or medical concerns, the Handover Block ensures that the conversation is redirected to a human operator who can manage this information securely and professionally.
* **Escalated Customer Complaints**:\
  If a customer expresses dissatisfaction or frustration with the AI's responses, the Handover Block can be used to transfer the conversation to a human agent, ensuring the issue is handled with the appropriate care and attention.

## Analytics

In our Analytics section, you can track and monitor key metrics related to the Human Handover, including:

* **Handover Rate %**: The percentage of users who requested to speak with an operator by activating the Handover Block. It is calculated based on the total number of users.
* **Chats with Requests**: The number of chats where the user requested human assistance.

{% hint style="info" %}
For more information on these and other performance metrics, refer to the guide: [analytics.md](../../workspace/activities/analytics.md "mention").
{% endhint %}
