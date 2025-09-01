# 📎 Upload Block

The Upload Block allows users to easily and intuitively **upload documents directly** into the conversation flow **within the chat**.&#x20;

This block provides flexibility by defining file size limits, customizing messages, and managing whether file uploads are mandatory. The Upload Block enhances user interactions by allowing users to share documents, streamlining workflows and providing greater control over file management.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-03-26 alle 10.12.24.png" alt=""><figcaption><p>The Upload Block</p></figcaption></figure>

## Key Features

*   **Easy File Upload**

    Users see a simple, intuitive interface within the chat to upload files. Once uploaded, each file is automatically saved as a [**variable**](../variables/) in your workflow. You can then:

    * Store and track the file,
    * Reuse files in downstream workflows for follow-up actions or further automation (e.g., checking if a file was provided),
    * Or forward it to external systems via integrations.
* **Custom Workflow Placement**\
  You can insert the Upload Block at any point in your workflow, choosing the exact moment when file upload should be enabled. This gives you the flexibility to align document submission with your business logic.&#x20;
* **File Access & Reuse**\
  Uploaded files are accessible in the **Chat** section of your workspace. From there, you can view the conversation and all exchanged messages, and download the uploaded documents.&#x20;

## **Operator File Sharing**

**Human operators can also upload and send files during a live chat**.&#x20;

After taking over a conversation from the virtual assistant, an operator can attach and deliver documents directly to the user, ensuring seamless, real-time support.

## How It Works

The Upload Block is designed to be simple to configure and easy for users to interact with during the conversation. Here’s how it functions:

**Customizable Sections**

* **Optional Message**: This text can be displayed in the chat to provide instructions or context for the user before they upload a file.
* **Caption (optional)**: A caption can be shown alongside the uploaded file as additional context.
* **File Variable**: The uploaded file is saved in a [variable](../variables/). By default, a standard value is defined in the block’s configuration. However, the user can select a custom variable via a dropdown menu if needed.

**File Size Limit (Toggle)**

* **Active (default)**: Limits the file size to 5MB.
* **Disabled**: Increases the file size limit to 25MB.
* **Above 25MB**: Upload is not permitted.

**Mandatory Upload (Toggle)**

* **Disabled (default)**: The user can skip the upload by selecting the “Skip” Quick Reply.
* **Enabled**: The upload becomes mandatory, and the skip option disappears.

**Quick Reply for Skip**

* **Customizable Text**: The default text is “Skip,” but this can be modified to suit your needs.
* **Custom Destination**: By default, the skip option is linked to the “Welcome” workflow, but this can be changed to fit your needs.

### Downloading Uploaded Files

The files uploaded by users can be downloaded directly from the conversation in the platform’s [chat area](../../workspace-sections/chats/). There, you’ll find the exchanged messages along with a link to download the uploaded document.

## User Experience: Process Flow

When the Upload Block is activated in the conversation, here’s what happens:

1. **Message Display**: If configured, the message you set (e.g., instructions or context) is shown in the chat.
2. **Upload Button**: A button for uploading the document is displayed.
3. **Preview of Upload**: Once the user uploads a file, a preview is shown in the chat with the file name and an appropriate icon based on the file type.
4. **File Size Validation**: If the file exceeds the set size limit, an error message is displayed. Otherwise, the file is saved in the variable defined during configuration.
5. **Skip Option**: If the upload is not mandatory, the user can skip the upload by selecting the "Skip" Quick Reply. If it is mandatory, the user cannot proceed without uploading a file.
6. **Conversation Progression**: Once the file is uploaded (or skipped if applicable), the conversation continues with the next block in the workflow.

Note: The user cannot type a message while uploading the document.

{% embed url="https://screen.studio/share/BR69CfUA?_loop=1&autoplay=1" %}
Uploading a document in the chat
{% endembed %}

## Common Use Cases

The Upload Block is useful in many scenarios. Here are some examples:

1. **Customer Support**:\
   When users need to submit screenshots or documents to support their issues, such as error reports or photos of a damaged product, the Upload Block makes it easy to attach and share files without leaving the chat.
2. **Document Submission**:\
   In processes like form submission or application submissions, users can upload required documents (e.g., identification, contracts, or images) directly through the chat, speeding up the process and eliminating the need for email.
3. **Product Warranty Claims**:\
   If a user wants to submit a warranty claim, they can easily upload receipts or proof of purchase as part of the claim process within the chat, improving efficiency and reducing the need for external communication.

## Planned Future Improvements

In the near future, you’ll be able to **filter conversations** by those that have uploaded attachments. This will allow you to easily find and manage conversations containing files, and even **download all attachments** together for efficient review.&#x20;
