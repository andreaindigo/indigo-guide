# 🔀 Reroute Block

The Reroute Block is a powerful tool that allows you to **redirect the conversation flow to another agent or workflow**, giving you full control over how users move through the conversation.&#x20;

By using this block, you can define specific destinations, guiding the conversation from one step to the next in an efficient and logical manner. This feature is especially useful when conversation paths need to be divided based on certain criteria or user responses.

The Reroute Block helps create dynamic, flexible conversation paths, ensuring that user requests are directed to the right agent or workflow without disrupting the overall flow.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 11.17.24.png" alt=""><figcaption><p>The Reroute Block</p></figcaption></figure>

## Key Features

### Destination Setting

With the Reroute Block, you can precisely specify the destination where the conversation will be redirected. This could be:

* An **agent**: Sending the user to another AI agent.
* A **workflow**: Redirecting the conversation to another workflow for further action.
* A [**variable**](../variables/): Using variables to influence the conversation path dynamically.

### “Resume from Here” Option

When activated, the “Resume from Here” feature ensures that **after completing the redirected path** (whether an agent or workflow), **the conversation will return to the point where the Reroute Block was initially triggered**. This is particularly useful for simple workflows where, after invoking an agent or workflow, the conversation needs to return to its previous point without complex logic.

For example, if you want to return to a certain point in the conversation after completing a task or receiving an answer, “Resume from Here” allows the conversation to seamlessly continue without requiring the configuration of a complex “come back” logic.

## Best Practices

* **Including Reroute within other Blocks**

The Reroute Block is often used within other logical blocks, such as the Condition Block. For instance, if a certain condition is met, the conversation flow can be rerouted accordingly to a designated agent or workflow, enhancing the adaptability of the conversation.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 11.24.14.png" alt=""><figcaption></figcaption></figure>

* **Dynamic Testing and Debugging**

The Reroute Block is also incredibly useful during the testing phase of workflow development. \
By **manually rerouting the conversation to a particular block or agent** (such as the [Prompt Block](../utility-blocks/prompt-block.md))**, you can test and evaluate specific parts of your workflow in isolation**, without going through the entire conversation path.&#x20;

For example, if you’re working on a customer service virtual assistant, and you want to test how it handles a support ticket escalation, you can configure a Reroute Block to instantly direct the conversation to the "escalation agent" without having to simulate the entire customer interaction leading up to that point.
