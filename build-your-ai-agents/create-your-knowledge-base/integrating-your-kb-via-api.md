# Integrating Your KB via API

## **Why Use API-Based KB Integration?**

Instead of manually uploading static documents, **API-based integration** allows AI Agents to **retrieve real-time, structured information** directly from your internal systems or databases.&#x20;

This method is particularly beneficial for managing **frequently updated or large-scale knowledge bases.** API integration is ideal for:

* **Large and Complex Datasets** – Efficiently handling extensive, structured information, such as product catalogs, customer data, or transactional records.
* **Real-Time Information** – Providing AI Agents with up-to-date data, such as inventory levels, pricing, customer support records, and more.

{% hint style="warning" %}
Even if your content does not change frequently, API integration may still be the **best choice** when handling **large, structured, or complex datasets**. Here’s why:

* **Product catalogs should always be integrated via API** (e.g., Google Sheets, Shopify) rather than as static documents to ensure better searchability and retrieval efficiency.
* **Complex, high-volume content** is easier to manage via integration rather than static uploaded documents.&#x20;
{% endhint %}

📌 **Note:** This article assumes a minimum level of technical knowledge, as API integration requires setup and maintenance, making it less immediate than document uploads.

## **Two Main API Use Cases**

1. **Connecting to Internal Tools or Systems** (e.g., CRM, ticketing, ERP) for real-time information access.
2. **Connecting a Google Sheet** to dynamically retrieve structured data.

## **1. API Integration with Your Internal Tools**

Instead of manually uploading large knowledge bases, API integration enables AI Agents to fetch real-time data from systems like **e-commerce platforms** (e.g. Shopify, Magento), **CRMs** (e.g. Salesforce, Zendesk, HubSpot), **ERPs, or internal databases**.

This dynamic approach is perfect for continuously updated, large-scale datasets.

_**Example 1: Integration with an E-Commerce Platform (e.g., Shopify)**_\
&#xNAN;_&#x49;magine integrating an e-commerce platform, such as Shopify, with your AI Agent to dynamically retrieve **product catalogs, pricing, and availability**. Rather than uploading static documents for each product, the AI Agent can query Shopify in real time to access the most up-to-date information on stock levels, prices, and product details whenever a customer asks about a product._

_**Example 2: Integration with CRM (e.g., Salesforce)**_\
&#xNAN;_&#x41;n AI Agent can also be connected to your CRM system (e.g., Salesforce) to retrieve **customer information, support data, and ticket history**. This allows the AI Agent to provide real-time, personalized responses based on live data rather than relying on outdated, static documents. For instance, instead of storing all past support tickets in your KB, the AI Agent can query Salesforce to fetch open ticket history for a specific user during their inquiry._

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-19 alle 11.14.13.png" alt=""><figcaption><p>An example of a API Call to a product catalog database</p></figcaption></figure>

### **Step-by-Step Integration Process**

{% stepper %}
{% step %}
### Configure the API Integration

* Start by setting up the **API integration** to connect your AI Agent with your internal tools (e.g., Salesforce, Shopify).

{% hint style="info" %}
For detailed guidance, refer to this section: [integrations.md](../../getting-started/integrations.md "mention").
{% endhint %}
{% endstep %}

{% step %}
### Define the User Request via a Prompt

* Set up a **Prompt block** in your workflow to extract the specific information needed from the user’s query. This data should be structured in a **JSON format** (e.g., customer details, product information) and saved in **variables** for use in subsequent steps.

{% hint style="info" %}
For more detailed instructions on creating Prompts, see [prompt-block.md](../../getting-started/blocks-and-variables/utility-blocks/prompt-block.md "mention"), and for using Variables, refer to [variables](../../getting-started/blocks-and-variables/variables/ "mention").&#x20;
{% endhint %}
{% endstep %}

{% step %}
### Configure API Calls to Fetch Data

* In the relevant workflow, configure the **API block** in your workflow to retrieve the necessary data, utilizing the JSON variables extracted from the user’s query in the previous step.
* Save the response of the **API SQL query** in a new variable for further processing.

{% hint style="info" %}
Instructions for configuring the API block are available here: [api-block.md](../../getting-started/blocks-and-variables/action-blocks/api-block.md "mention").
{% endhint %}
{% endstep %}

{% step %}
### Pass the Data to the AI Agent or use it in a Workflow

* Configure the AI Agent to reference the stored variable and incorporate the API data into its responses by specifying the variable in a dedicated custom section of the AI Agent block. This ensures that the AI Agent uses **real-time data** instead of relying on static KB documents.

{% hint style="info" %}
For more information on setting up AI agents, refer to [how-to-create-an-agent.md](../../getting-started/agents-workflows-and-triggers/how-to-create-an-agent.md "mention").
{% endhint %}

* If additional checks or data manipulations are required before the agent provides a final response, the variables containing the API-fetched data can be used in any other workflows.&#x20;

{% hint style="info" %}
Here you can find more information about workflows, blocks and variables: [blocks-and-variables](../../getting-started/blocks-and-variables/ "mention").&#x20;

Additionally, in the [next article](../configure-your-ai-agents.md) of this practical guide to building AI agents, you will find detailed guidance on configuring conversational flows.
{% endhint %}
{% endstep %}
{% endstepper %}

### ✅ Best Practices for KB Integration via API

* **Limit API requests** to specific, relevant queries to avoid unnecessary data fetching.
* **Filter information** within the API call to retrieve only the necessary data, improving efficiency.
* Use **variables** to store and dynamically handle API responses, ensuring smooth integration into AI workflows.
* **Ensure API security** by using **authentication tokens** and **encrypting sensitive data** to protect privacy and maintain data integrity.

## **2. API Integration with Google Sheets**

**Sometimes, directly calling external system APIs isn’t feasible**. This can occur in two situations:

1. The data is stored in a custom management system that doesn’t expose APIs.
2. The exposed APIs are too slow, negatively impacting the chat user experience.

In these cases, we offer a simple and effective solution: **Google Sheets**. We treat the spreadsheet like a database: by adding the data you want to retrieve into the sheet, you can access it in real time through the agent.

#### How does it work in the workspace?

We provide an **internal API** that allows you to run SQL queries on a Google Sheet, managing access via Google authorization. You can choose between using a publicly accessible spreadsheet or a private one, accessing it with a Google service account.&#x20;

Google Sheets offers a flexible way to structure and retrieve KB data. This method works particularly well for e-commerce catalogs, support knowledge bases, or structured company FAQs.

_**Example: Product Information for an E-Commerce Store**_\
&#xNAN;_&#x49;magine an AI agent providing product details for an online store with 1,000 products that have a slow update rate. Instead of having to expose a dedicated API, just upload the data to the sheet and the API connection will allow real-time retrieval of product information._

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-19 alle 11.16.24.png" alt=""><figcaption><p>Example of a API block with an integration to a Google Sheet</p></figcaption></figure>

Here’s a detailed overview of this service.

### **Step-by-Step Integration Process**

{% stepper %}
{% step %}
### Configure the API Integration with your Google Workspace

* Start by configuring the API integration to connect indigo.ai with your Google Workspace. This allows the AI Agent to retrieve data from your Google Sheets.&#x20;
{% endstep %}

{% step %}
### Create Your Google Sheet

* Organize content into **separate tabs**, each corresponding to a different AI Agent or topic.
* Structure the **columns** to allow easy filtering through SQL queries, ensuring that column names are **clear and consistent** for efficient data retrieval (e.g., "Product Name," "Price," "Stock Level").
{% endstep %}

{% step %}
### Configure API Calls in Your Workflow

* Use **indigo.ai’s internal document processing service** for structured data retrieval and ensure that information is extracted in a well-organized manner.
* Insert the **API block** into your **AI workflows** to enable data retrieval from Google Sheets.
* **Customize the SQL query** based on the workflow's requirements to fetch only **relevant information** for specific tasks (e.g., fetching product details when a customer asks about a particular item).&#x20;

{% hint style="info" %}
For more info on configuring a API call to connect with a Google Sheet, refer to this article: [api-block.md](../../getting-started/blocks-and-variables/action-blocks/api-block.md "mention").
{% endhint %}
{% endstep %}
{% endstepper %}

### ✅ Best Practices for Google Sheets API Integration

* **Use structured tabs** for different data sets (e.g., Product Info, Pricing, Stock) to keep data organized and easy to query.
* **Minimize unnecessary API calls** to avoid excessive processing load, ensuring faster retrieval times and optimized performance.
