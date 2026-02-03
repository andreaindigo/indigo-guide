# 🗃️ Capture Block

In any conversational flow, it's often essential to **ask users for specific information**—whether you're collecting contact details, confirming a date, or running a quick survey. The Capture Block lets you **gather user responses in a structured and efficient way** by **saving answers into variables that can be reused throughout your workflow**.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-04-01 alle 15.44.16.png" alt=""><figcaption></figcaption></figure>

## **How Does it Work**

The Capture Block guides the user through providing specific inputs and ensures data is saved in the correct format. Here's what you can configure:

#### 1. **Ask a Question**

Customize the prompt to clearly request the information you need.

#### 2. **Store the Response**

Assign a [variable](../../workspace/variables/) where the user's response will be saved. Once selected, the block automatically recognizes the variable’s data type.

#### 3. **Choose the Expected Data Type**

Supported types include:

* **Text**: For names, free-form answers, or general input.
* **Number**: Ideal for capturing ages, quantities, or other numeric values.
* **Boolean**: For yes/no questions or binary responses.
* **Date/Time**: Perfect for appointments, deadlines, or availability.

#### 4. **Mandatory or Optional Input**

* **Mandatory**: The user must provide a valid input to proceed. No alternative buttons will be shown.
* **Optional**: A **“Cancel” button** will appear, allowing the user to skip the question. You can configure this button to redirect to any agent or workflow (default is the Welcome Workflow).

#### 5. **Validation**

If the user’s input doesn’t match the expected format, the assistant will automatically ask them to try again. Once a valid value is received, the workflow continues.

{% hint style="danger" %}
The Capture Block is **blocking** by nature—this means **the conversation cannot proceed until the user provides a valid input or chooses to skip (if the question is optional)**.
{% endhint %}

## Common Use Cases

The Capture Block is highly versatile. Here are some typical scenarios:

* **User Registration**: Collect personal details like name, email, or phone number.
* **Bookings & Appointments**: Capture date and time selections for scheduling.
* **Surveys & Feedback**: Ask users for structured opinions or preferences.
