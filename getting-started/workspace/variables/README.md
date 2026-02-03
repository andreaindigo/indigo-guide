---
icon: brackets-curly
---

# Variables

Variables play a central role in **shaping the flow of a conversation** with your virtual assistant.

They **allow your assistant to store information and make decisions based on that data**, enabling a dynamic, personalized experience for users. In the context of workflow configuration, variables are especially useful for controlling logic and triggering specific actions based on **user inputs or external data**.

## What is a Variable?

A variable is essentially **a container that holds a value**. It is defined by:

* **A Name**: Used to access the value stored in the variable.
* **A Type**: Restricts and validates the type of value that can be assigned to the variable.

## How Are Variables Used?

Variables are essential for interactive, advanced conversational flows.

They can be populated in different ways:

* **External Data via APIs**: Variables can be filled with data retrieved from external systems through API calls.
* **User Input**: Information extracted from user messages can be used to populate variables.
  * [**Capture Block**](../../blocks/logic-blocks/capture-block.md): Values are extracted from user messages and stored within a variable.
  * [**Prompt Block**](../../blocks/utility-blocks/prompt-block.md): JSON data returned by a Prompt Block fills the variable with the required values.
* **Manual Configuration**: You can set the value of a variable manually during the workflow configuration process.
  * [**Set Values Block**](../../blocks/logic-blocks/set-values-block.md): The value of a variable can be manually set during the workflow configuration.
  * **Fallback Value**: A default value can be assigned to a variable during its creation or modification (as explained below), ensuring the variable has an initial value if no other value is provided.

Once a variable is populated, it influences the conversation by helping determine the next step in the workflow or the response provided to the user.

{% hint style="info" %}
A variable can either contain a value or be considered "empty." In our platform, a variable without a value may be represented as either **`null`** or `empty` , both of which indicate that the variable currently holds no usable content.

Both states allow you to reset or validate variables during the conversation flow, especially when configuring logic with the [Set Values](../../blocks/logic-blocks/set-values-block.md) or [Condition](../../blocks/logic-blocks/condition-block.md) blocks.
{% endhint %}

## Variable Categories

There are three main categories of variables:

* **System Variables**: These are **automatically created and managed by the platform**. Examples include context variables (e.g., the last message exchanged), time-based variables (such as date and time), or system-related variables like those identifying whether the conversation is occurring in a live or test environment, or the URL where the web chat is installed. \
  System variables cannot be modified through blocks such as Set Values or Capture.

{% hint style="info" %}
For a complete list of system variables, visit this page: [system-variables.md](system-variables.md "mention").
{% endhint %}

* **Custom Variables**: You can create your own custom variables tailored to your specific needs.&#x20;
* **Secrets**: Secrets are a special type of variable designed to **securely store sensitive information like API tokens, authentication keys, or credentials**. They’re encrypted, hidden from the interface, and only accessible during API calls—ensuring secure handling of confidential data.

{% hint style="info" %}
Learn more about Secrets and how to use them: [secrets-management-protecting-your-sensitive-information.md](../../security-compliance-and-trust/secrets-management-protecting-your-sensitive-information.md "mention").
{% endhint %}

## Managing Variables

Variables are managed centrally through the **link in the bottom left menu of your workspace**. From there, you can view all available variables (including system variables) and create or modify them as needed.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-29 alle 18.52.02.png" alt="" width="563"><figcaption></figcaption></figure>

### Creating a Custom Variable

To create a new variable, go to **Variables & Entities** in the left sidebar, and click **Create New**.

A variable requires two things:

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-29 alle 18.45.34.png" alt="" width="563"><figcaption></figcaption></figure>

* **Name**: A unique identifier for the variable. Il nome deve essere univoco (non possiamo creare due variabili con lo stesso nome) ma non ha particolari vincoli.
* **Type**: Defines what kind of value the variable can hold. The platform supports the following types:
  * **Text**: Any kind of content.
  * **Number**: Whole or decimal numbers.
  * **Boolean**: A binary value (true/false).
  * **Date/Time**: A date and time value.
  * **Agent/Workflow**: A reference to an agent or workflow.
  * **🆕 Map**: A JSON object (key-value pairs), ideal for structured data.
  * **🆕 List**: A collection of values (strings, numbers, or even maps).

In the **Values** section, there are two optional fields:

* **Test Value**: A value associated with the variable during API block testing.
* **Fallback Value**: The initial value assigned to the variable. If not assigned, the variable defaults to `null`.

### Deep Dive: Map & List Variables

To support advanced workflows, especially those involving **External Triggers** and **structured data exchanges**, we introduced two powerful new variable types in June 2025: Map and List.

These variable types allow your virtual assistant to handle complex, structured payloads with greater flexibility and precision. They're particularly valuable when working with JSON inputs from APIs, Zapier automations, CRM records, ERP systems, or any external tool integrated via our Platform API.

{% hint style="info" %}
These additions were introduced as part of our platform’s evolution to support **Non-Conversational Triggers**, enabling true automation from external events to intelligent actions. Learn more about this new feature here: [non-conversational-triggers.md](../../../product-updates/latest-product-releases/non-conversational-triggers.md "mention")
{% endhint %}

#### 🗺️ Map Variables

A **Map** variable stores key-value pairs in JSON format. Think of it as a mini-database your assistant can use to retrieve structured information. For example:

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "status": "active"
}
```

#### Creating a Map Variable

You can create a Map variable like any other variable using the **JSON editor** to define fallback and test values.

#### Writing to a Map

Map variables must be updated by **overwriting the entire map**; individual fields cannot be modified directly. You can populate a Map variable through:

* The variable creation modal
* A **Set Value** block
* An **API block** (via capture variable)

{% hint style="danger" %}
You cannot assign values to a Map variable directly from a [Capture block](../../blocks/logic-blocks/capture-block.md).
{% endhint %}

**Example update:**

```json
mappa1 = {
  "key1": "value1",
  "key2": "value2"
}
```

#### Reading from a Map

Use **dot notation** to retrieve values:

* `{{mappa.key1}}` → returns "value1"
* Nested access is supported: `{{mappa.nested1.nested2}}`

#### Using Map Variables in [Condition Blocks](../../blocks/logic-blocks/condition-block.md)

Map variables support the following conditions:

* **IS / IS NOT**: Checks if two maps are (or aren’t) identical. Key order does not matter
* **IS NULL / IS NOT NULL**: True if the variable is null (not just empty `{}`)
* **CONTAINS / DOES NOT CONTAIN**: Checks whether a key exists in the map
  * Example: `mappa1 CONTAINS key1` → `true`

{% hint style="danger" %}
When using a Map in a Condition block, you must refer to the **entire map**; you cannot condition directly on an internal value.
{% endhint %}

#### 📋 List Variables

A **List** variable holds an array of elements — such as strings, numbers, or even maps. For example:

```json
lista = ["stringa”, 1, {”key”: “value”}]
```

#### Writing to a List

Lists are created and updated using the same **JSON editor** as maps. Like maps, the **entire list** must be updated; individual elements can’t be edited directly.

#### Reading from a List

You can access the elements of a list using the syntax `listName[index]`.\
Using the example above:

* `list[0] = "string"`
* `list[1] = 1`
* `list[2] = {"key": "value"}`

You can also access the values of **objects inside a list**.\
For example:

* `list[2].key = "value"`

⚠️ **Limitation**: Due to a Drop limitation, when printing or passing a variable of type _List_ as a parameter, it is handled as a single concatenated string containing all list values.

Example:

```json
list = [1, 2, 3, "four"]
```

will be treated as:

```json
"123four"
```

✅ **Workaround**: Use the `format_list` function.

### **Conditional Block – Supported Operations for Lists**

When using _List_ variables as conditions in a Conditional block, the following operations are supported:

* **IS**: checks if two lists are equal (**order matters**).
  * Example:
    * `list1 = [1,2,3]`
    * `list2 = [2,1,3]`
    * `list1 IS list2` → `false`
* **IS NOT**: the negation of **IS**.
* **IS NULL**: checks if the value is **NULL**.
  * Example: if the list is empty `[]`, then `IS NULL` → `false`.
* **IS NOT NULL**: the negation of **IS NULL**.
* **CONTAINS**: checks if a **value** is contained in a list.
  * Example:
    * `list = ["string", 1, {"key": "value"}]`
    * `list CONTAINS "string"` → `true`
* **DOES NOT CONTAIN**: the negation of **CONTAINS**.

💡 **Tip**: When comparing lists with **IS**, the order of elements always matters. Two lists with the same values but in a different order are considered different.

## Best Practices

### Set Variables at the Start of the Conversation&#x20;

It’s a best practice to initialize all variables (usually to `null`) at the beginning of the conversation, in the [Welcome workflow](https://indigo-ai.gitbook.io/indigo.ai-guide/build-your-ai-agents/configure-your-ai-agents#configuring-a-welcome-message). This ensures that the **virtual assistant doesn't retain values from a previous user interaction**.&#x20;

{% hint style="info" %}
For more on configuring your agents, refer to this article: [Broken link](/broken/pages/DQeY10e3ZGK3N4RsW0lq "mention").
{% endhint %}

### Passing User Information or Other Data to Your Web Chat

At the beginning of the conversation, you may want to populate variables with data from external systems, such as your CRM.

A common use case is **passing user-related information, like login status or identifying details**.

This can be achieved by including parameters in the web chat script's URL. Doing so allows you to preset responses or **personalize the chat based on user data**, such as their ID or preferred contact methods. This approach enhances personalized interactions from the very start of the conversation.

{% hint style="info" %}
For detailed instructions on setting this up, refer to this article: [web-chat-integration-dynamic-interaction-and-data-exchange-with-your-website.md](../../../tech-deep-dives/web-chat-integration-and-customization-on-your-website/web-chat-integration-dynamic-interaction-and-data-exchange-with-your-website.md "mention").
{% endhint %}

### Variables in Chats

Variables can also be used in the [Chats](../activities/chats/) section as filters, allowing you to quickly find conversations based on their values.
