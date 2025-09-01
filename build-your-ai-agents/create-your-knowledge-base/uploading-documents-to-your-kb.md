# Uploading Documents to Your KB

Uploading static documents to your Knowledge Base (KB) is the best option when you need to store and manage **fixed, structured content** that doesn’t change frequently. This method is ideal for:

* FAQs and Troubleshooting Guides – Predefined answers to common questions.
* Company Policies and Guidelines – Official documents that remain relatively stable over time.
* Product Manuals and Service Descriptions – Comprehensive reference materials.
* Training Materials and Support Documentation – Guides to help internal teams or customers.

By uploading these documents, you ensure that AI Agents can efficiently retrieve and provide accurate responses based on trusted, pre-approved information.

#### 📢 Need to upload a large volume of documents?&#x20;

If your content is already stored in platforms like **Google Drive, Confluence, SharePoint, or internal document management systems**, manually uploading each file might not be the most efficient approach.

✨ **We can handle this for you!** Our team can automatically retrieve and structure content from your existing platforms, ensuring your KB is optimized for AI use.

However, whether you choose to do it yourself or with our support, **following the best practices below** will help you ensure that your KB is well-structured, AI-friendly, and effective.&#x20;

Let’s dive into the key requirements and best practices for uploading static documents. 🚀

## 1. What Types of Documents Can AI Agents Read?

AI Agents can process a variety of **text-based documents** as long as they are in a supported format and properly structured.

### ✔ Supported File Formats

Our platform supports the following document types:\
✅ **.pdf** – Standard format for documentation, but must be **machine-readable (not scanned content)**.\
✅ **.docx** – Well-structured Word documents with clear headings and formatting.\
✅ **.txt** – Plain text files, best for structured lists and simple content.\
✅ **.csv** – Useful for tabular data, FAQs, and structured responses.\
✅ **.xlsx** – Excel spreadsheets with clearly labeled columns and rows.

To ensure accurate processing and retrieval, **documents must:**

1. Be written in the **same language as the workspace**.
2. Contain **text-based content** rather than images or non-readable formats.

Additionally, you can integrate **URLs** from your website as knowledge sources. However:

* The system **only reads the text content of the specified webpage.**
* &#x20;It does **not** process **embedded links, images, or subsections** of the site.

When processing documents and URLs, the system **automatically extracts text** while filtering out images, videos, and unnecessary formatting to maintain **clean and structured content**.

### 💡 Best Practices for Readable AI Documents

* **Use Q\&A or tabular FAQ formats** – These are the most structured and readable formats for AI Agents.
* **Keep documents concise and well-structured** – Overly long documents may reduce accuracy.
* **Limit excessive images** – Documents with too many visuals may contain less AI-usable content.
* **Avoid poorly structured PDFs or DOCX files** – Unorganized content increases the risk of AI hallucinations (incorrect or misleading responses).
* **Be cautious with numerical data** – Documents with extensive figures (e.g., financial reports) can be challenging for AI to interpret correctly.

## 2. Selecting and Organizing the Right Documentation

### 📌 Prioritizing the Right Content

Before uploading documents, it’s crucial to determine which information is **truly useful** for AI Agents to provide accurate and relevant responses. You should **upload only the documents that provide value to your chatbot’s users.**&#x20;

Prioritize FAQs, support records, technical documentation, and help pages—while avoiding complex legal texts or irrelevant materials like Terms & Conditions.

### 🏷️ Organizing Content with Tags

Once the relevant content is identified, it’s important to organize it effectively by grouping your documents into **semantic topics**—referred to as **tags** on the platform.

_For example:_&#x20;

* _Shipping & Delivery – Contains all logistics and tracking details._
* _Payments – Includes refund policies, payment methods, and billing information._
* _Product Information – Covers technical specifications and troubleshooting guides._

**Each topic (tag) should contain only related information** to maintain clarity. This setup makes it easier for AI Agents to find relevant content and reduces confusion when answering user queries.

{% hint style="info" %}
There is no limit to the number of documents you can upload, so your AI Agent can grow its knowledge base over time.
{% endhint %}

## 3. Best Practices for Creating and Uploading Documents to Your Knowledge Base

Since **not all documents are processed equally**, following best practices for format, structure, and content organization will significantly enhance the AI’s ability to understand and use the uploaded information correctly.

### Formatting Documents for AI Compatibility

Generative AI works as a probabilistic model, generating responses based on word sequences in uploaded documents. Poorly formatted documents can lead to misinterpretations, incomplete responses, or AI errors.

The best-performing documents are those that have a **clear, structured format** that makes it easier for AI to extract relevant information.&#x20;

AI **does not scan entire documents at once** but instead retrieves **specific sections of text**. If information is scattered across multiple pages or mixed with unrelated content, the AI may struggle to maintain context, leading to less accurate responses.

### ✅ The Most AI-Friendly Format: Tabular FAQs

* Documents formatted as **question-answer pairs in tables** are the easiest for AI Agents to process and retrieve. The structured Q\&A format allows AI to match user queries directly to predefined responses, reducing errors and improving response accuracy.
* If applicable, consider structuring your content in **tabular form**, especially for FAQs and support documentation.

**For Tabular FAQs (CSV, Excel):**

* Use two columns: one for the question and one for the answer.
* The first row should contain column headers labeled "Question" and "Answer."
* Avoid adding extra columns or blank rows, as they may interfere with AI processing.

**For Text-based FAQs (TXT, PDF, DOCX):**

* Ensure that questions and answers are written consecutively without blank lines in between.
* Separate different FAQs with one empty line to enhance readability.
* Maintain consistent font formatting throughout the document (avoid bold, italics, or underlined text).
* Make sure each question-answer pair appears on the same page rather than being split across multiple pages.

{% hint style="info" %}
If you are using **FAQs hosted on a webpage (URL)**, ensure that the content is well-structured and properly indexed. If the AI struggles with chunking the information correctly, consider converting the webpage into a text-based document before uploading it.
{% endhint %}

Some documents, like product manuals, do not naturally fit into a Q\&A structure. \
In these cases, use clear sections with well-defined headings instead of forcing tabular formatting and follow a logical content hierarchy to maintain structure and readability.

### 👌 Optimizing Documents for AI Performance

To enhance AI compatibility, follow these **best practices** when formatting your Knowledge Base documents:

1. **Use AI-Compatible File Formats**—Among supported formats, **PDFs are the most problematic** due to formatting inconsistencies—avoid scanned PDFs, irregular layouts, or text embedded in images. Whenever possible, **use .DOCX or .TXT instead**, as they provide a clear text structure for optimal AI parsing.
2. **Use structured formatting**—prefer plain text with clear sections over embedding content in tables or within document margins.
3. **Keep paragraphs intact on the same page**—avoid splitting sections across multiple pages.
4. **Follow a clear heading hierarchy**—organize content with **Title 1 > Title 2 > Subtitle**, ensuring a logical flow. Repeat key headings and subheadings where necessary for clarity.&#x20;
5. **Avoid abrupt formatting changes**—do not randomly apply bold, italics, or underlining for emphasis, as it can disrupt AI readability.
6. **Use standard list formatting**—when including bullet points, follow a structured pattern (● > ○ > -) to maintain clarity.
7. **Separate images from text**—key information should always be written as text rather than relying solely on visuals.
8. **Avoid placing images between titles and descriptions**—if necessary, position images at the end of a section instead of breaking up text flow.&#x20;
9. **Follow a Markdown-Based Formatting Style**—Large language models (LLMs) are trained to process structured text most efficiently when formatted in Markdown style.

{% hint style="info" %}
Markdown is a lightweight formatting language that uses simple symbols to structure text, making it easy to read and edit while preserving clear formatting for AI processing.

For example, instead of using a word processor to bold a phrase, in Markdown you would write:

<kbd>\*\*This is bold text\*\*</kbd>&#x20;

<kbd>#This is a main heading</kbd>&#x20;

This format helps AI Agents recognize document structure more effectively, improving the accuracy of responses.
{% endhint %}

### 📋 Guidelines for Text-Based Documents

AI Agents retrieve information by identifying specific sections of text, rather than scanning entire documents at once. To optimize text-based documents for your Knowledge Base, follow these best practices:

* The best-performing documents are those where **information is contained within a single page** rather than being scattered across multiple sections.
  * Documents that cover multiple products or topics across several pages are more challenging for AI to process accurately, as the scattered information can disrupt context and lead to misinterpretations.
* The **AI struggles with broken paragraphs** that are split across multiple pages. Keeping complete paragraphs intact ensures better information retrieval.
* If a document includes **links** that need to be shared with users, ensure they are written in full (e.g., [www.example.com](http://www.example.com)) rather than being embedded in hyperlinked text, as AI Agents only process visible text.
* **Avoid using outdated file formats like .DOC** – only .DOCX, .TXT, and PDF are supported for optimal results.
* Since AI relies on recognizing patterns in text, **documents with codes, reference numbers, or IDs do not perform well unless specifically formatted for retrieval**.

### 📊 Handling Documents with Tables

#### **✅** When Do Tables Work Well?

If tables are used as a way to **format textual content**, they can be **effectively processed** by AI Agents. This includes:

* Tables that organize **definitions, comparisons, or structured answers** in a readable format.
* Clearly labeled column headers that provide direct meaning to the table’s content.

#### **❌** When Do Tables Perform Poorly?

**Numerical or highly technical tables** are more difficult for AI to process correctly. For example:

* Tables that contain only **codes, product IDs, or numerical data** do not perform well because the AI struggles to infer relationships between numbers without additional context.
* The AI lacks the ability to accurately **cross-reference numbers from different sections of a document**, making fragmented tables harder to process.

#### Best Practices for Tables:

* **Ensure column headers are explicit** – AI Agents rely heavily on them for context.
* **Avoid splitting important information across multiple tables** if a clear relationship needs to be maintained.
* Use only **two main columns** ("Key" and "Value") if the table is intended for AI lookup.
* For AI retrieval of product codes, inventory data, or reference numbers, **consider using an external database** (e.g., Google Sheets via API integration or an SQL database), which is often more effective than using static documents.

{% hint style="info" %}
If your data is static and rarely changes, uploading an Excel file (.xlsx or .csv) is the easiest option for storing FAQs, product specifications, or service lists.

For frequently updated data, like for example employee directories or appointment schedules, an API integration with Google Sheets (or another database) ensures AI Agents always retrieve the latest information without manual uploads.

In this article, you’ll find a step-by-step guide on setting up API integrations, including how to connect Google Sheets for real-time data access: [integrating-your-kb-via-api.md](integrating-your-kb-via-api.md "mention").
{% endhint %}

### 🌐 URLs vs. Direct Document Uploads

While URLs can be uploaded, **document uploads generally provide more control** over content formatting and readability.

When using URLs:

* Ensure the linked page **does not contain excessive hyperlinks** that could interfere with AI retrieval.
* **Webpage content is scraped only once at the time of upload**—if the website is updated later, you **must manually refresh the URL** in the platform to update the AI’s knowledge. Click the "**Update**" button in the platform whenever content changes to ensure AI Agents retrieve the latest version.

> Whenever possible, prefer **direct document uploads** over URLs, as AI processing is more reliable when working with **structured text** rather than unpredictable webpage layouts.

## 4. Uploading Documents & Managing Files

The **Docs & URLs** section of the platform allows you to upload and manage your documents efficiently.

Here’s how the process works:

{% stepper %}
{% step %}
### Upload Your Files

Select the files you want to upload. Ensure your files are **not password-protected**, as they cannot be processed.
{% endstep %}

{% step %}
### Upload URLs

In addition to documents, you can upload **multiple website URLs** as sources. URLs should be **publicly accessible** and **free from restrictions** to allow the system to extract content.
{% endstep %}

{% step %}
### File Processing & Tagging

Once uploaded, the system takes a moment to **parse and save the information**.&#x20;

After processing, you can:\
✔ Assign **one or multiple tags** to each document.\
✔ Check the **upload date** to track the latest version in the system.\
✔ **Download, replace, or delete** files as needed.

{% hint style="warning" %}
**Tagging Rules:** Tags must follow these formatting rules:

* Only **letters** (uppercase or lowercase) and **numbers** (0-9) are allowed. The order of characters does not matter.
* **Special characters** and **symbols** are not permitted.
{% endhint %}
{% endstep %}

{% step %}
### Live Updates & Accessibility

Our platform **processes documents directly in production**—meaning no separate staging environment is required.

{% hint style="info" %}
If an AI Agent has access to a document via tag settings, no additional publishing is needed.&#x20;

The content becomes immediately available.
{% endhint %}
{% endstep %}

{% step %}
### Keep Your Documents Updated

To ensure AI Agents always provide **accurate and up-to-date information**, it’s essential to establish an **internal process** for updating uploaded documents and website pages (URLs).

Whenever there is a relevant change in the content used by AI Agents—such as updated policies, revised FAQs, or modified product details—the corresponding files must be **manually updated and re-uploaded** to the Knowledge Base. This applies not only to documents but also to website URLs, as AI Agents do not automatically detect changes on web pages.

A best practice is to implement a **regular review cycle** within your team to check for outdated information and ensure all uploaded content remains accurate and relevant.
{% endstep %}
{% endstepper %}
