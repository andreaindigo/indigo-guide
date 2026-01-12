# Tools

#### Overview

Tools enable Agents to go beyond static conversational flows by connecting them to external systems and actionable services. With Tools, Indigo Agents can retrieve real-time information and execute operations directly from a conversation—such as querying databases, creating calendar events, or triggering external workflows—without requiring hardcoded paths for every user request.

\
Tools are configured centrally in Tools settings (under Agent settings) and can be based on any API service documented with the OpenAPI standard. Once created, tools become reusable building blocks: they can be assigned to specific Agents or leveraged inside API blocks, making integrations easier to manage, scalable across projects, and consistent across the workspace.

\
A key benefit of Tools is that tool usage is dynamically decided by the LLM, depending on the user’s intent and conversation context. This allows Agents to respond more flexibly to variations in user input and to handle a wider range of real-world requests. In addition, Indigo supports multi-tool orchestration within a single interaction, enabling the agent to invoke multiple tools either in parallel or sequentially to accomplish complex tasks—without the need to design rigid workflows in advance.

#### Key benefits

1. **More capable and reliable virtual assistants**   \
   Tools enable agents to access real data and execute actions when needed, reducing hallucinations and improving response accuracy. As a result, assistants become more useful in real scenarios, not only informative but also actionable.

* **More natural conversations, fewer rigid flows**  \
  Instead of relying on predefined workflows containing API Blocks, the LLM can decide when and how to use tools based on the user’s intent. This improves the agent’s ability to handle variations in user requests, making the overall experience smoother, more flexible, and closer to human-like assistance.

#### Tools Settings

The Tools settings section, located under **Agent settings**, allows you to transform any API service documented with the OpenAPI standard into a tool.\
Once created, these tools can be assigned to agents or used in API blocks, enabling seamless integration with external systems and services directly within your workspace.

<figure><img src="../../.gitbook/assets/tools settings.png" alt=""><figcaption></figcaption></figure>

#### Tools in Agents

Inside each Agent block, a new Tools section lets you assign specific tools to that agent.&#x20;

<figure><img src="../../.gitbook/assets/integration in agent.png" alt=""><figcaption></figcaption></figure>

The tools available are only those previously activated in the Integrations settings.

* The first dropdown allows you to select the provider (e.g., Google Calendar).
* The second dropdown lets you choose the action offered by that provider (e.g., Create a new event).

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

This way, the agent can perform the configured action whenever it is triggered in a conversation.\
You can also add multiple integrations using the + Add tool button.

\
**Tools in API Blocks**

External integrations can also be used in the API block. Beyond the usual custom API calls, you can now use preconfigured actions from the tools enabled in the Integrations section.

To access this feature, simply enable the new Use integrations toggle in the API block.

<figure><img src="../../.gitbook/assets/API.png" alt=""><figcaption></figcaption></figure>

Once enabled, you’ll be able to select both the provider and the action to be executed.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: within an API block, only one action per integration can be selected.
{% endhint %}

### How to Create a Custom Tool

Creating a custom tool allows your agents to connect with any external API service documented with an OpenAPI specification.

1. Go to Tools settings\
   Open the Tools settings section under Agent settings.
2. Click Create custom tool\
   Start the configuration process for a new tool.
3. Import the OpenAPI schema\
   Paste the OpenAPI specification of the service you want to connect.\
   This defines the available endpoints, methods (e.g., GET, POST), and parameters.
4. Configure authentication\
   If the external service requires authentication (e.g., API key, OAuth), specify the details during setup.
5. Save the configuration\
   The custom tool is now available in your workspace and can be assigned to agents or used in API blocks.

<figure><img src="../../.gitbook/assets/edit custom tools.png" alt=""><figcaption></figcaption></figure>



### Multi-tool orchestration within a single interaction

It is now possible to invoke multiple tools within a single interaction, with orchestration handled directly by the LLM.

Depending on the context and the goal of the request, the LLM can:

* invoke multiple tools in **parallel**, when actions are independent;
* invoke multiple tools **sequentially**, when the execution of one tool depends on the output of a previous one.

This approach goes beyond invoking a single tool per request and enables the creation of composed, dynamic, and adaptive action flows, without the need to define a rigid workflow in advance.

The result is **greater flexibility**, improved agent decision-making, and more effective use of tools within a single conversation.
