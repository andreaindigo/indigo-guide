# 🔣 Condition Block

Not all conversation flows follow a linear path. Often, different paths need to be taken based on specific criteria, such as the information provided by the user. This is where the Condition Block comes into play.

The Condition Block uses conditional logic to **determine how the conversation should proceed based on certain conditions being met**. By combining logical operators and variables, this block enables specific parts of the conversation flow to be activated, allowing for **dynamic responses tailored to user inputs**. This helps in creating intelligent and adaptable conversational paths that are based on real-time data or information shared during the conversation.&#x20;

{% hint style="info" %}
The functionality of this block is driven by [variables](../../workspace/variables/ "mention"): check out the article for detailed guidance.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-27 alle 09.30.29.png" alt=""><figcaption><p>The Condition Block</p></figcaption></figure>

## How It Works

The Condition Block functions based on variables, checking if certain conditions are met before proceeding to the next step in the conversation.&#x20;

To define a condition, the block evaluates three key components:

1. **Variable**: The data or input being assessed (e.g., user preferences, choices, or responses).
2. **Operator**: The logical operator used to evaluate the condition (e.g., equals, greater than, etc.). Operators can be unary (e.g., IS NULL) or involve a condition value.&#x20;
3. **Condition Value**: The value being compared against (e.g., a specific user input or a predefined variable value).&#x20;

The available operators depend on the selected variable type: once you choose a specific variable, only the corresponding operators will appear in the dropdown. This results in different sets of operators being available depending on the variable type:&#x20;

* **Text**

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 11.59.25.png" alt="" width="370"><figcaption></figcaption></figure>

* **Number**

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 14.56.21.png" alt="" width="353"><figcaption></figcaption></figure>

* **Boolean**

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 14.55.05.png" alt="" width="375"><figcaption></figcaption></figure>

* **Date/Time**

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 14.59.11.png" alt="" width="375"><figcaption></figcaption></figure>

* **Agent, workflow or variable**

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 16.49.37.png" alt="" width="375"><figcaption></figcaption></figure>

### Multiple conditions

A single Condition Block can evaluate multiple conditions. These are processed **sequentially from top to bottom**. When a condition is true, the corresponding action is executed, and subsequent conditions are skipped. It is important to **arrange the conditions in the desired order**, as the block will execute the first satisfied condition.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-27 alle 09.22.30.png" alt=""><figcaption></figcaption></figure>

The Condition Block also provides flexibility to combine conditions using logical operators:

* **AND / NOT AND**: All conditions must (or must not) be true.
* **OR / NOT OR**: At least one condition must (or must not) be true.

{% hint style="info" %}
When resetting or initializing variables, it's best practice to explicitly set them to **`null`** OR `empty`, ensuring a clean starting state with no residual data from previous interactions.
{% endhint %}

When conditions are satisfied, the conversation proceeds to the next set of blocks based on the actions defined for each condition.

## Best Practices

### Using the “Else” Condition

In many scenarios, you might want to define an action for when none of the conditions are met. This is where the **“Else”** condition comes in. By using the **True** **variable** (a system variable that always evaluates to true), you can set up a default **action that is triggered if no other conditions are satisfied**. This ensures that there is always a fallback behavior.

{% hint style="info" %}
Since conditions are evaluated in order and only the first matching one is executed, it's best to add an "Else" condition at the end, so that it works as a fallback action for when none of the previous conditions are met.
{% endhint %}

For example:

* If condition1 is true → proceed to action1.
* If condition2 is true → proceed to action2.
* Else (if no conditions are true) → proceed to a fallback action.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-27 alle 09.31.40.png" alt="" width="375"><figcaption></figcaption></figure>

### Using Counters and Variables for Dynamic Actions

Another powerful use of the Condition Block is combining it with variables like **counters** to dynamically control the flow.&#x20;

For example, if a user asks for support, the Condition Block can check a counter variable (e.g., counter = 1) and provide an initial response. If the user asks for help again, the counter increases, and the conversation is routed to a human operator using the Handover Block.

1. If assistance\_requested = true and counter = 1 → Virtual assistant responds. Add a [Set Value](set-values-block.md) block and set counter = 2.
2. If assistance\_requested = true and counter = 2 → Handover to a human operator with an Handover block.&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-27 alle 09.49.01.png" alt=""><figcaption></figcaption></figure>

## Action Management

Once a condition is met, the associated action is executed, guiding the user through the conversation flow in a structured manner. **If the condition is not met, the block is ignored**, and the conversation continues as usual.

### Adding Blocks to the Condition

In the Condition Block, you can **add any type of action block after each condition check**. For example, you can use the Message Block to send a message or the Reroute Block to redirect the conversation. However, you cannot add another Condition Block within a Condition Block.

## Use Case Examples

#### Customer Support Personalization

A support bot can use the Condition Block to offer personalized responses based on the user’s account type:

* If user\_type = VIP → Provide priority support.
* If user\_type = Regular → Offer standard support options.

#### Product Recommendations

A bot can suggest different products based on the user’s preferences:

* If category\_interest = Technology → Show the latest tech gadgets.
* If category\_interest = Fashion → Suggest new fashion collections.

#### Dynamic Job Suggestions

An HR chatbot can suggest job offers based on the candidate’s experience:

* If years\_experience > 5 → Recommend senior-level positions.
* If years\_experience <= 5 → Suggest entry-level roles.

## A Concrete Example

Let’s take a simple example to understand how the Condition Block works:

We want the assistant to address users by their name, but only ask for it once. Here's how to set it up:

1. Create a name variable (text type) to store the user’s name. Initially, the name variable will be empty (null) - this should be defined with a [Set Values](set-values-block.md) block at the beginning of the workflow.
2. Drag the Condition Block into the workflow and define the condition: If name is null.\
   If true, ask the user for their name using the [Capture Block](capture-block.md) and store it in the name variable. \
   After that, send a welcome message using the [Message Block](../message-blocks/).&#x20;
3. Add another condition to check if the user already provided their name (condition: name is not null). If true, send a "Welcome back" message without asking for their name again.
