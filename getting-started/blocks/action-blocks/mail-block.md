# 🔗 Mail Block

The Mail Block is a powerful feature within the platform that provides a simple, flexible system for **automatically sending emails at specific points in your workflow**, based on user actions or system triggers, ensuring smooth integration into the conversational flow.&#x20;

This block is perfect for sending structured, static emails at specific points in the conversation. Whether you're sending a summary of a conversation, a report, or user data to a relevant department, the Mail Block simplifies the process of sending emails with customizable fields.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-25 alle 17.01.54.png" alt=""><figcaption><p>The Mail Block</p></figcaption></figure>

## Key Features

### Configurable Fields

The Mail Block allows users to easily customize several key email elements:

1. **Destination**:\
   Specify the recipient's email address (single or multiple, separated by commas). The destination field also supports the use of [variables](../../workspace/variables/) to dynamically personalize the email address.
2. **Sender**:\
   Define the display name of the sender. This can be customized to show the name of the virtual assistant, a company name, or another desired identifier. The actual email address will still be from @indigo.ai.
3. **Subject**:\
   The subject line of the email can be customized to suit the context of the message. You can also use [variables](../../workspace/variables/) in the subject line to make it more dynamic and relevant.&#x20;
4. **Reply To** (optional):\
   This field specifies the email address where replies should be directed. It only accepts a single address.
5. **Body**:\
   The content of the email can be written in either plain text or HTML format.
   * **Plain text**: If plain text is selected, any HTML tags will be automatically removed.
   * **HTML**: The HTML will be rendered (excluding JavaScript for security reasons).
6. **CC** (optional):\
   You can add recipients in copy to the email. This is managed the same way as the destination field, allowing multiple recipients to be added.&#x20;

### Constraints and Customizations

While the **Mail Block** provides a lot of flexibility, there are a few customizations that require additional configuration:

* **Logo Customization**: The logo can only be modified via a dedicated API call.
* **Modification of the "From" Address**: To send emails from an address other than @indigo.ai, a specific configuration on Postmark is required.

{% hint style="info" %}
This article contains more information on integrating with the indigo.ai API: [integrating-with-our-platform-api](../../../integrating-with-our-platform-api/ "mention")
{% endhint %}

### Handling Outcomes

Once the email is sent, the system can handle different outcomes:

* **Success Case**: If the email is sent successfully, you can define which agent or part of the workflow should handle the next step in the conversation.
* **Error Case**: If the email fails to send, the system will log the error. You can then configure the agent to either inform the user or trigger an alternative action to manage the flow interruption.

## Common Use Cases

#### Sending Conversational Summaries

After a web chat interaction, the user may receive an email with a summary of the conversation. This could include shared information or useful links. For example, you can use the [variable](../../workspace/variables/) **$conversation** in the body of the email to include a summary of the last 100 interactions, formatted in JSON and HTML-encoded.

`[{"sender": "bot", "text": "..."}, {"sender": "user", "text": "..."}, ...]`

#### Sending a Report

The AI agent can generate and send a report dynamically based on user interactions. This is useful for business or customer support scenarios, where a detailed summary or report needs to be sent to the user or internal teams.

#### Collecting Information

In cases where the AI agent gathers information (e.g., support requests or booking inquiries), the Mail Block can automatically send the collected data to the appropriate department for efficient handling.
