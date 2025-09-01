# 🔧 Set Values Block

The Set Values Block allows you to **assign values to specific** [**variables**](../variables/) during a conversation. It’s an essential tool for **customizing the assistant’s behavior based on conditions, inputs, or internal logic**.

You can use it to:

* Assign values manually based on logic
* Preload or reset variable values at the start of a conversation
* Modify or clear data stored in the assistant’s memory.&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-02 alle 18.49.42 (1).png" alt=""><figcaption></figcaption></figure>

## How it Works

When using the Set Values Block, you define:

* **The target variable** you want to update
* **The value** to assign to it.&#x20;

Supported operations include:

* **Set to a fixed value**
* **Set to null or empty**&#x20;
* **Set to true or false**.&#x20;

## Best Practices

#### 1. Use it to **initialize variables** at the start of the conversation

We recommend using a Set Values Block in your **Welcome Workflow** to set or reset all the key variables, **ensuring every new session starts fresh**. For more on how to do this, see: [configure-your-ai-agents.md](../../../build-your-ai-agents/configure-your-ai-agents.md "mention").&#x20;

You can clear previous values by setting:

* Text variables to **empty**
* Boolean variables to **false**
* Any variable to **null**.&#x20;

#### 2. Advanced Use: Regex Functions

The Set Values Block also supports **regex-based expressions** to transform values dynamically. This is especially useful for:

* **Extracting specific patterns from a user input** (e.g., cleaning a user ID)
* **Validating or transforming data before storing it**

**Example:**

You collect a raw user ID in `user_id_raw`. Using a regex function in the Set Values Block, you can extract the clean ID: `user_id_clean = REGEX(user_id_raw, 'pattern')`

You can also apply regex to check if an email format is valid, extract postal codes, or format date strings.

To insert a regex, simply type it in the “value” field using the supported syntax.
