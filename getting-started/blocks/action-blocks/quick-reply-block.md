# 👉 Quick Reply Block

Quick Replies are a valuable feature for improving user interaction within a virtual assistant. As the name suggests, Quick Replies provide "fast responses" by presenting **predefined buttons** that users can click to select their desired action. These buttons enable users to quickly access information or perform actions without the need to type additional questions.

While our interface and agents are powered by conversational and generative AI, there are still instances where **offering the user a limited set of clear options** can improve the experience. By offering choices that are easy to select, Quick Replies streamline the conversation and make navigation more efficient.

<figure><img src="../../../.gitbook/assets/quick replies 1.png" alt="The Quick Reply Block"><figcaption><p>The Quick Reply Block</p></figcaption></figure>

**Use Cases Examples**

* **Customer Support**:\
  After a user asks, "Can you help me with my order?", Quick Replies can present buttons such as "Track My Order," "Cancel Order," or "Contact Support," making it easy for the user to select the next step.
* **Product Recommendations**:\
  When a user inquires about "What should I buy for a gift?", Quick Replies can offer options like "Jewelry for Her," "Jewelry for Him," or "Gift Cards," directing the user to relevant product categories.

## How It Works

The **maximum number of buttons supported** per response is **10**. Quick Replies appear as buttons in the chat interface, and when clicked, they guide the user to the selected content or action.

#### Quick Replies Can Be Linked to:

* **An Agent or Workflow**: This helps create a smooth, intuitive navigation flow in the conversation.
* **A Phone Number**: For instance, to connect users to customer support contacts. Example: "Call Customer Support" (links to a phone number).
* **An External Web Page**: You can create buttons that redirect users to external websites for more detailed resources. Example: "Visit Our FAQ" (links to an FAQ page).
* **A** [**Variable**](../../workspace/variables/) <mark style="color:$danger;">**of Agent or Workflow type**</mark>: can reference dynamic content such as an Agent or Workflow, making actions flexible and context-dependent.
* **An Email Address**: For sharing an email. You would set the button to the link format: `mailto://emailaddress@domain.xxx`. Example: "Email Us" (links to the support team’s email).

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-25 alle 18.03.30.png" alt="" width="375"><figcaption><p>Quick Reply Connection Options</p></figcaption></figure>

The **titles** of Quick Replies are automatically filled in based on the title of the response they are connected to. However, these titles can be edited anytime by clicking on them.&#x20;

You can also remove a Quick Reply connection by clicking the X next to the Quick Reply box.

## Using Quick Replies with variables

In addition to linking buttons to external actions, Quick Replies can also be used to save the value of a variable<mark style="color:$danger;">.</mark> For example, imagine a Quick Reply asking “How old are you?” and showing three buttons with different age ranges (e.g., “Under 18”, “18–30”, “Over 30”). Each button is linked to the variable age, and depending on the user’s choice, can assume a different value. Consequently, the conversation flow can branch into different paths, allowing the assistant to personalize the experience based on the selected age range.

{% hint style="info" %}
Example:

{ "text": "How old are you?", "quick\_replies": \[ { "title": "Under 18", "set\_variable": { "age": "under\_18" } }, { "title": "18–30", "set\_variable": { "age": "18\_30" } }, { "title": "Over 30", "set\_variable": { "age": "over\_30" } } ] }
{% endhint %}

## Best Practices

#### Control User Input with the Typebar Setting

In the [workflow settings](https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/blocks-and-variables#settings-top-right-button), you can choose to **disable the Typebar**. This means the user will only be able to choose from the available Quick Replies and won’t be able to type any input. This is helpful when you want to control the flow of the conversation and ensure the user makes a selection from predefined options. If the Typebar is enabled, users can still type their queries freely, potentially bypassing the Quick Replies.&#x20;

#### Limit the Number of Buttons

While you can add up to 10 buttons, it's advisable to **keep the number of options minimal.** Too many choices can overwhelm the user, especially if they are looking for a quick solution.&#x20;

#### Use Clear and Descriptive Titles

The button titles should be simple and clear, indicating exactly what the user will get when they click. For example, instead of using vague labels like “Click Here,” use specific, action-driven titles like "Track My Order" or "Get Help."
