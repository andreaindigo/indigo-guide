# 🧠 Prompt Block

The Prompt Block is one of the most powerful tools in the indigo.ai platform. It allows your AI assistant to process and interpret user input using advanced [Large Language Models (LLMs)](../../ai-knowledge-hub/large-language-models-llms-available-on-our-platform.md), enabling smart classification, data extraction, and logic generation.

While it _can_ be used to generate natural-language replies, its most effective use is for **extracting structured data** or **classifying user messages** for downstream use in your workflow.

{% hint style="warning" %}
If your goal is to **generate responses for the user**, you should **create an agent** instead. The agent page is designed specifically for reply generation and works as a templatized, optimized prompt tailored to conversational use cases. Learn more about how to configure agents here: [configure-your-ai-agents.md](../../../build-your-ai-agents/configure-your-ai-agents.md "mention").
{% endhint %}

<figure><img src="../../../.gitbook/assets/Screenshot 2025-07-07 alle 15.08.54.png" alt=""><figcaption></figcaption></figure>

The Prompt Block is ideal for tasks like:

* Extracting specific values from free-form user input (e.g., order number, email)
* Classifying messages to determine workflow routing
* Generating structured outputs like **JSON** objects to guide assistant behavior
* Processing multi-turn context or maintaining consistent logic across flows

The **most common use case** is configuring the model to **return a JSON structure**, so you can **capture specific values and use them throughout the conversation**.

{% hint style="info" %}
Make sure to read the article [variables](../variables/ "mention") for guidance on defining, populating, and referencing variables in your workflow.
{% endhint %}

## Configuration and Customization Options

Here’s a breakdown of the main fields and settings, as shown in the Prompt Block UI:

### ✏️ Message Composer

You can now write multiple message entries inside the block:

* **System** – Used to set instructions and rules for the assistant (e.g., role, goals, tone)
* **User** – Represents the user input (you can refer to `{{$last_user_message}}` or use static text)
* **Assistant** – Can simulate previous virtual assistant's replies if you want to create continuity or test memory

This structure mimics how most LLMs interpret prompts and supports more **natural and multi-turn interactions**.

### 🧠 Short Memory

This setting controls **how many recent turns of conversation the assistant should remember within the block**. Choose **how many prior message pairs (user + assistant)** to include, making the Prompt Block context-aware and dynamic.

### ⚙️ Options Panel

The **Options** panel in the Prompt Block gives you precise control over how your AI assistant processes and interprets input. Each setting plays a key role in how the model behaves and how you handle the output. Here’s a breakdown of each configuration field:

* **Max tokens**: Defines the maximum number of [tokens](https://indigo-ai.gitbook.io/indigo.ai-guide/getting-started/ai-knowledge-hub/introduction-to-ai-a-beginners-guide#what-are-tokens) the model can generate in its response. Default: 256. Use lower values for shorter, more concise outputs, and higher values for more detailed or descriptive responses.
* **Max documents tokens**: Sets the maximum number of tokens from the documents (e.g. retrieved KB content) that fill the `{{documents}}` variable. Default: 2048. A higher value allows the model to consider longer texts when formulating its response—ideal for working with large knowledge base entries.
* **Prompt language**: Specifies the language in which the model should formulate its response.
* **Model**: Select the LLM you want to use. Example: azure-gpt-4o-mini (EU).

{% hint style="info" %}
indigo.ai supports a range of language models, giving you the flexibility to balance performance and response speed depending on your use case. Learn more about the available LLMs and how to choose the right model for your assistant in this article: [large-language-models-llms-available-on-our-platform.md](../../ai-knowledge-hub/large-language-models-llms-available-on-our-platform.md "mention").
{% endhint %}

* **Temperature**: Controls the creativity of the AI’s response.
  * Lower values (e.g., 0–0.3) make outputs more focused and predictable—ideal for structured tasks. When using **JSON extraction**, set **temperature to 0** for more deterministic and reliable output.
  * Higher values (e.g., 0.7–1) allow for more varied and creative responses—suitable for open-ended generation.
* **Error Handling (Error)**\
  Choose where the conversation should go (an agent or workflow) if the block fails to execute properly. This ensures your flow continues even when errors occur. If not defined, the default error message will be: _“Something went wrong, try again.”_
* **Variable Assignment**\
  If your prompt returns structured data (e.g., JSON), use this section to **capture specific values**.\
  **Assign each key of the JSON output to a variable using the format `response.key`**. This makes the data available for use in the rest of your workflow.
* **JSON Output Mode**\
  Enable this toggle if you expect a structured response from the model. When enabled, the output must be valid JSON.

## ✍️ How to Write a Prompt

A well-structured prompt ensures your AI assistant performs the right task, with the right tone, and returns the desired output format—especially when extracting structured data like JSON.

To maximize effectiveness, we recommend following a modular format when writing prompts. Here’s how to structure it:

#### **# Role**

Clearly define the assistant’s role and goal.

> Example
>
> “You are a virtual agent specialized in customer service. Your goal is to understand the user's request and classify it according to the issue type and urgency.”

#### **# Task**

Describe the expected outcome and format.

> Example
>
> “Extract relevant data and return it in a valid, one-line JSON format.”

#### **# Tone of Voice**

Specify the communication style: formal, professional, friendly, etc.

> Example
>
> The tone of voice is professional yet welcoming, conveying expertise without feeling cold or distant. It delivers information clearly and directly, avoiding unnecessary details. The assistant demonstrates empathy and attentiveness, maintaining a confident and reassuring tone. It communicates with clarity and precision, providing straightforward responses without unnecessary justifications.

#### **# Context**

Include any relevant background that might influence the assistant’s output.

> Example: Company description, sector, product categories, known customer intents.

{% hint style="info" %}
💡 Best Practice: If you have multiple prompts and agents and want to reuse these settings, consider storing company description and tone of voice as [variables](../variables/) for centralized management.&#x20;
{% endhint %}

#### **# General Instructions**

Provide high-level rules the assistant should follow during reasoning and generation.

> Example
>
> * Always output a valid JSON
> * If unsure, use `null` as value
> * Do not generate natural language explanations unless explicitly requested

#### **# Detailed Instructions**

List the step-by-step logic or classification rules to guide the assistant’s response.

> Example
>
> 1. Identify the topic of the user’s message
> 2. Match it to a predefined category
> 3. Assign a level of urgency based on user tone or keywords

#### **# Reference Information**

Provide data sources or variables the assistant can rely on (like documents, product tables, FAQs).&#x20;

{% hint style="info" %}
You can easily refer to specific documents in your knowledge base by using the variable `{{documents}}` to include all documents, or `{{documents_tag}}` to filter by a specific tag. For more details on uploading documents to your knowledge base, check out this article: [uploading-documents-to-your-kb.md](../../../build-your-ai-agents/create-your-knowledge-base/uploading-documents-to-your-kb.md "mention").
{% endhint %}

#### **# Response Rules**

Clarify formatting expectations.\
Example:

* Output must be a single-line valid JSON
* Mandatory keys: `issue_type`, `urgency`, `reasoning`
* Use lowercase for values
* No line breaks or additional text

**# User Message**

You can insert the latest user message here referring [system variables](../variables/system-variables.md) like `{{$last_user_message}}` or `{{message_from_mother}}`.

#### **# Output Format**

Specify the required structure.

* **Define keys**: Tell the model exactly what data points to extract.
* **Guide value selection**: You can suggest likely values or provide rules.

> Example
>
> {"issue\_type": "...",\
> "urgency": "..."}

**# Examples**

Add real use cases to help guide the model's pattern recognition.\
Example:

```json
User: “I still haven’t received my package.”  
JSON: {"issue_type":"shipment","urgency":"medium"}

User: “I was charged twice for my last order!”  
JSON: {"issue_type":"payment","urgency":"high"}
```

### Full Prompt Example

```
# Role  
You are a virtual agent from the customer support team of an e-commerce company. Your goal is to classify user messages based on the type of issue and the perceived urgency.

# Task  
Extract the required data from the user's message and return a valid JSON object, formatted as a single line without line breaks.

# Tone of Voice  
Professional and direct.

# Context  
The e-commerce store sells books, accessories, and digital products. Common issues include shipping, payments, returns, and general inquiries.

# General Instructions  
- If you're unsure about the exact value, return "null"  
- Do not generate any additional text besides the JSON  

# Detailed Instructions  
1. Analyze the user's message  
2. Identify the type of issue (using predefined categories)  
3. Assign an urgency level based on expressions like “urgent,” “ASAP,” etc.  
4. Justify your choice in the "reasoning" field

# Response Rules  
- The JSON must include three keys: `issue_type`, `urgency`, `reasoning`  
- Use lowercase for all values  
- Output should be a single line  

# User Message  
User: {{last_user_message}}

# Output JSON  
JSON:
```

## Best Practices

Writing effective prompts is both an art and a science. Follow these best practices to ensure your Prompt Blocks are consistent, reliable, and optimized for performance and cost.

#### 1. Order Matters

The **order** of your instructions and examples significantly influences the model's output.

* **Rules placed earlier** in the prompt carry more weight than those placed later.
* **Examples listed first** have greater influence on the model's behavior than those that follow.

_Tip: Always place your most important instructions and high-quality examples at the top of each section._

#### 2. Use Markdown for Clarity

Prompt Blocks support [Markdown formatting](https://www.markdownguide.org/getting-started/), which helps you visually organize sections (e.g., bold text, headers, lists) and make prompts easier to read, understand, and debug.

#### 3. Optimize for Prompt Caching

Prompt caching is a performance and cost optimization feature automatically enabled when using models hosted by OpenAI or Azure OpenAI.

How it works: if the first _N_ tokens of a prompt you send match the first _N_ tokens of a previous prompt, the model can reuse those cached tokens. This means faster processing and lower API costs.&#x20;

Best Practices:

* Place the **static, reusable instructions** (e.g., role, rules, tone, context) **at the top of your prompt**.
* Put the **dynamic elements**, like the user’s message, **at the bottom**.

#### 4. Include a "Reasoning" Key in JSON Outputs

When your prompt generates a JSON response (e.g., for classification or data extraction), make sure to include a **`reasoning`** field as the **first key in the object**. This enables **chain-of-thought prompting**, **guiding the AI to think step-by-step before delivering the result**.

Adding a "reasoning" field not only enhances the accuracy of the response but also simplifies debugging during [testing](../../../build-your-ai-agents/testing-and-debugging.md). It allows the assistant to explain the logic behind its output, making it easier to validate the reasoning and refine the accuracy, particularly when troubleshooting or improving the model.

_Tip: During_ [_testing_](../../../build-your-ai-agents/testing-and-debugging.md)_, you can show this field using a Text Block conditioned by `env = test` to better understand why the assistant made a particular choice._

#### 5. Add a “Step-by-Step” General Instruction

Add the following text to your **General Instructions** section to improve accuracy and ensure rules are followed:

```plaintext
To generate your response, take a deep breath and follow this process step by step:
1. First, read all the instructions in this prompt.
2. Ensure you understand and follow every rule in each section.
3. Generate your response.
4. Re-read the prompt to verify that your response complies with all the instructions.
5. If any part of the response breaks a rule, revise and repeat this step-by-step process.
```

### 📚 Useful Links on Prompting

If you're looking to improve how you write prompts for your AI assistant, check out these resources:

* [How to write great AI prompts](https://www.notion.so/blog/how-to-write-ai-prompts)
* [OpenAI Platform / Prompt engineering / Enhance results with prompt engineering strategies.](https://platform.openai.com/docs/guides/prompt-engineering/six-strategies-for-getting-better-results)
* [Best practices for prompt engineering with the OpenAI API](../../../).&#x20;
