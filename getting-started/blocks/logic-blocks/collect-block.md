---
description: Released in June 2025
---

# 🧪 Collect Block

In any intelligent conversation, capturing the right information at the right moment is crucial. Whether you're asking for an order number, a user’s email, or their preferred product, the Collect Block helps you **extract meaningful, structured data from user input** in a fluid, conversational way that avoids rigid, pre-scripted flows.

**Unlike traditional Q\&A sequences**, the Collect Block understands how users naturally express themselves. It can extract relevant details from open text, prompt for missing information when needed, and guide the user seamlessly through the data collection process.&#x20;

With just a few configurations, the Collect Block helps you build smarter conversations, enabling your assistant to gather information efficiently while keeping interactions dynamic, natural, and user-friendly.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-07 alle 14.36.41.png" alt=""><figcaption></figcaption></figure>

### ✅ Why Use the Collect Block?

* **More natural conversations**: Users can provide multiple answers at once, and the virtual assistant will understand and extract relevant details.
* **Smarter fallback**: If something is missing, the assistant doesn’t stop - it asks.
* **Cleaner flows**: You can collect multiple variables without chaining multiple blocks.
* **High flexibility**: You can define what’s admissible, expected, and how it should be validated.

### Use Cases

Here are just a few examples of how you can use the Collect Block:

* **Order Support**: Extract order number, email, and issue description from a single message
* **Product Inquiry**: Capture product type, budget, and preferred style
* **Lead Generation**: Ask for name, company, and phone number in a smooth, guided way
* **Internal Routing**: Collect ticket type, priority, and user role before escalating

## What It Does

The Collect Block allows your assistant to:

* Detect and **extract information** from user input
* **Save** that information into variables for future use
* **Ask for missing details** automatically, when needed
* Guide the user through a **natural, contextual conversation** to complete data collection

This means you can efficiently gather multiple pieces of information (e.g., order number, product type, and customer email) without building separate flows for each.

## ⚙️ How It Works

Each Collect Block is composed of one or more **data points**, each of which corresponds to a variable you want to populate.

For each variable, you can configure the following:

**1. Variable to Save**

Select an existing variable from your workspace or create a new one. This is where the collected value will be stored.

**2. Data Description**

Describe what the variable represents: this helps the model understand the expected value and format.\
You can include:

* Natural language prompts (e.g., “user’s email address”)
* Format hints or patterns (e.g., a regex for validating an order number)

This field informs the assistant of **what to look for** in the user's input.

**3. Ask If Not Provided (Toggle)**

Enable this option if you want the assistant to **proactively ask** the user for the value if it isn’t detected in the conversation.

* If **enabled**, the assistant will keep prompting until a valid response is given or the context becomes irrelevant.
* If **disabled**, the assistant will only try to extract data passively from what's already been said.

**4. Admissible Values (Optional)**

You can provide a list of **valid options** for the variable.\
Each value has two fields:

* **Label**: The accepted value (e.g., "Gold", "Silver", "Platinum")
* **Description**: A short explanation or list of **synonyms** the model can use to recognize that value (e.g., “golden, G, premium” → “Gold”)

This helps standardize the output and improves accuracy, especially for structured inputs like product types, categories, or regions.

**5. Use Shots**

The Use shots feature allows you to define example conversations between the User and the Assistant to guide the model’s behavior.\
Each shot represents a sample interaction made up of one or more message exchanges.

* User Message: contains the input the user would provide.
* Assistant Message: contains the expected response from the assistant.\
  You can add multiple examples using + Add shot, or expand a single shot with additional dialogue lines using +.

This section helps demonstrate how the model should respond in similar situations, improving consistency and tone in its answers.

<figure><img src="../../../.gitbook/assets/use shots.png" alt=""><figcaption></figcaption></figure>

### 🛠️ Tips for Building

* Use **simple, natural descriptions** in the prompt to guide what the assistant should collect.
* Combine with a [**Condition Block**](condition-block.md) to branch logic based on what's been collected.
* Pair with [**Set Values**](set-values-block.md) to initialize defaults or flag missing inputs.
* Don’t overuse admissible values unless needed; keep it lean and meaningful.
