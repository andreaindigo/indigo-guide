# 🚦 Is Your KB Ready? A Quick Assessment Guide

## Why assess Your Knowledge Base Before an AI Project?

Your Knowledge Base (KB) is the foundation of your AI Agents. Its quality, structure, and completeness directly impact:

* How well your AI Agents perform
* The accuracy of responses they provide
* The complexity and timeline of your AI agents implementation.&#x20;

Before proceeding with AI configuration, you need to assess what you already have and determine whether your documentation is AI-ready or requires improvement.

This guide will help you:

✅ Evaluate whether your existing knowledge is **complete** and **structured** **enough** for AI use.\
✅ Identify **gaps or issues** that may affect AI accuracy.\
✅ Understand **the effort required** to optimize your KB before integrating it with AI Agents.

Let’s go step by step!

## **Step 1: Do You Have the Necessary Content?**

Before setting up your AI Agents, start by evaluating whether you have the **necessary content for each topic** they will cover.

To ensure AI Agents can provide accurate responses, it's essential to determine which information is truly relevant and valuable. The most effective way to do this is by identifying:

1. The most common questions your users ask.
2. The key information your chatbot should provide.
3. Existing documents that contain these answers.

{% hint style="danger" %}
**Not all internal documents are useful for AI Agents!**&#x20;

Instead of uploading everything, focus on content that is **structured and directly relevant** to user interactions.
{% endhint %}

For example, legal documents, contracts, or terms & conditions are often written in complex legalese and may not be ideal for providing direct customer support.

If content is missing, it **must be created first**, which adds time and complexity to the AI implementation.&#x20;

{% hint style="warning" %}
If your only available knowledge source consists of **historical customer service tickets or chat logs**, you’ll need to build a structured Knowledge Base from scratch, as these records often contain outdated, inconsistent, or irrelevant information that isn't optimized for AI processing.
{% endhint %}

<table data-full-width="false"><thead><tr><th width="102.58203125">Topic</th><th width="170.27734375">Content Available?</th><th>Next Steps</th></tr></thead><tbody><tr><td>Topic 1</td><td>✅ Yes</td><td>Proceed with content optimization &#x26; upload</td></tr><tr><td>Topic 2</td><td>⚠️ Partially</td><td>Fill in missing details or refine content</td></tr><tr><td>Topic 3</td><td>❌ No</td><td>Create content from scratch before proceeding</td></tr></tbody></table>

#### **Where to Look for Existing KB Content**

If you’re unsure whether your content already exists, check:

* **Internal Documentation** (FAQs, product manuals, guidelines, training materials)
* **Customer Service Records** (ticketing systems, chat transcripts, common inquiries)
* **Website Content** (help center, blogs, knowledge articles, product pages)
* **Spreadsheets & Databases** (services, product specs, pricing, inventory data)

## Step 2: What is the Best Format & Integration Method?

After identifying what content is available, the next step is to assess whether the format of that content is suitable for AI Agents and determine the most appropriate integration method.

<figure><img src="../../.gitbook/assets/Screenshot 2025-01-23 alle 10.14.03.png" alt=""><figcaption><p>Overview of data formats, sources, and their effectiveness for AI Agents.</p></figcaption></figure>

### Key Factors to Evaluate

**1️⃣ Content Complexity & Volume**\
**2️⃣ Documents Structure and Format**\
**3️⃣ Data Update Frequency**

#### 1️⃣ **Content Complexity & Volume**

**Large and complex datasets should always be integrated via API** rather than uploaded as static documents.&#x20;

API Integration is ideal for managing complex data such as product catalogs (e.g.  Google Sheets, Shopify) and large databases (e.g. customer records).

On the other hand, document uploads work well for simpler, static content like FAQs, troubleshooting guides, company information, and policies.

#### **2️⃣** Documents Structure and Format

When assessing your content, it’s important to look beyond the file type and focus on what the document actually contains, and how well it’s structured and formatted for AI Agents to process.

* ✅ **Best-case scenario** → Content that is **already structured** and formatted for AI use is **ideal**. \
  (For more details on the specific requirements and best practices, refer to Step 3.)

A great example is an **FAQ document** formatted in a **table with question-answer pairs**. This format is ideal because of its clear structure (e.g., Q\&A pairs, easy for AI to parse) and minimal complexity, making it straightforward for AI Agents to retrieve and process the information.

* ❌ **Worst-case scenario** → Content that **only exists on a website** can be problematic.

Websites vary widely in structure, making it difficult for AI Agents to extract relevant information due to the presence of unrelated content, such as ads, sidebars, or inconsistent layouts.&#x20;

{% hint style="warning" %}
We typically avoid scraping information from URLs, except for contextual company pages like "About Us" or "Contact."
{% endhint %}

The more **structured** and **consistent** your content is, the easier it will be for your AI Agents to extract useful information and provide accurate responses. If your content is messy or unstructured, it will require additional work to make it suitable for AI use.&#x20;

#### **3️⃣** Data Update Frequency

It's important to assess how frequently your data changes or needs to be updated.

* **Static data** (e.g., FAQs, policies) → Document uploads work well for low volumes of data, while an API integration is more suitable for larger or complex datasets.&#x20;
* **Dynamic data** (e.g., pricing, stock levels) → API integration is best for real-time data that changes frequently. This ensures that AI Agents always retrieve the latest information and eliminates the need for manual updates.

### Recap

By considering these three key factors - **content complexity, structure/format, and update frequency -** you can assess whether your content is in the ideal format and determine the best integration method for your AI project.

<table><thead><tr><th width="178.7734375">Factor</th><th width="335.6953125">✅ Ideal Format / Integration Method</th><th>⚠️ Potential Risks</th></tr></thead><tbody><tr><td><strong>Content Complexity &#x26; Volume</strong></td><td><ul><li>API Integration for large or complex datasets (e.g. product catalogs, customer records)</li><li>Upload for simple, structured documents</li></ul></td><td>Messy, unstructured content and complex data</td></tr><tr><td><strong>Document Structure &#x26; Format</strong></td><td><ul><li>Structured content like Q&#x26;A tables, clearly formatted documents</li></ul></td><td>Scraping from unstructured websites or scanned PDFs</td></tr><tr><td><strong>Data Update Frequency</strong></td><td><ul><li>API Integration for real-time retrieval of frequently updated data (e.g., pricing, inventory).</li><li>Document uploads for content that doesn't change often.</li></ul></td><td>Manual updates for frequently changing data</td></tr></tbody></table>

## Step 3: Are Your Documents AI-Ready?

Now that you've assessed your content, it's time to dive deeper into ensuring that the **documents** or data you need to upload to the platform meet the requirements for effective AI processing. There are specific **formatting and structural** best practices to follow to ensure AI Agents can easily retrieve and process the information.

Use this checklist to determine if your documents or API data sources are properly formatted and structured for optimal AI performance.

{% hint style="info" %}
For more detailed information on the best practices and requirements mentioned here, refer to the next article: [uploading-documents-to-your-kb.md](uploading-documents-to-your-kb.md "mention").&#x20;
{% endhint %}

#### AI-Ready Content Checklist

✅ **Supported File Formats** → Our platform supports: **.pdf, .docx, .txt, .csv, .xlsx**.\
✅ **Formatting & Structure** → Information must be **clearly structured**.\
✅ **Language & Readability** → Avoid complex jargon, **use clear and concise language**.\
✅ **AI Processing Compatibility** → Ensure that files are **machine-readable**.

{% hint style="warning" %}
As an example, **scanned PDFs** are **not** AI-friendly because they **aren’t machine-readable**. Consider converting such files into editable text formats.
{% endhint %}

More specifically, you can find a checklist of best practices based on the file type in the table below:

<table><thead><tr><th width="127.77734375">File Type</th><th width="515.31640625">Best Practices &#x26; Requirements</th><th data-type="checkbox">Check</th><th data-hidden></th></tr></thead><tbody><tr><td>All</td><td><ul><li>Content is written in the same language as the AI workspace</li><li>Each document covers one clear topic instead of mixing multiple topics in a single file</li><li>Sentences are concise, clear and to the point, avoiding unnecessary explanations or specific jargon</li><li>Maintains a consistent tone and terminology throughout</li><li>URLs are explicitly written rather than embedded in hyperlinks</li></ul></td><td>false</td><td></td></tr><tr><td>TXT</td><td><ul><li>Keep plain text with clear Q&#x26;A pairs</li><li>Use Markdown formatting to structure the document with clear titles, subheadings</li><li>Use UTF-8 encoding for compatibility</li><li>Avoid excessive line breaks or blank spaces</li></ul></td><td>false</td><td></td></tr><tr><td>DOCX</td><td><ul><li>Use proper headings &#x26; subheadings</li><li>Ensure consistent formatting (bold, lists, tables)</li><li>Remove unnecessary images or embedded elements</li></ul></td><td>false</td><td></td></tr><tr><td>CSV</td><td><ul><li>Use two-column structure (Question/Answer or Key/Value)</li><li>No empty rows or unnecessary columns</li><li>Keep headers clearly labeled and formatted</li></ul></td><td>false</td><td></td></tr><tr><td>XLSX or Google Sheet (via API)</td><td><ul><li>Structure sheets with clearly labeled columns</li><li>Each tab should focus on a single topic</li><li>Avoid merged cells and excessive formatting</li><li>Best format for for product codes, IDs, or inventory data</li></ul></td><td>false</td><td></td></tr></tbody></table>

## Step 4: What Needs to Be Done?

After completing the assessment, you should now have clear **next steps** based on your KB’s status.

<table><thead><tr><th width="229.26953125">Assessment Outcome</th><th width="367.515625">Actions Required</th><th>Effort Level</th></tr></thead><tbody><tr><td>❌ <strong>Major gaps, no structured data</strong></td><td><ul><li>Build KB from scratch</li></ul></td><td>High</td></tr><tr><td>⚠️ <strong>Some content is missing or incomplete</strong></td><td><ul><li>Create missing content</li><li>Reformat documents that are not structured properly for AI use</li></ul></td><td>Medium</td></tr><tr><td>✅ <strong>KB is ready</strong></td><td><ul><li>Proceed with documents upload</li><li>Set up API integrations for real-time data retrieval</li></ul></td><td>Low</td></tr></tbody></table>

#### Priority Recommendations

1. **First, create missing content** → Ensure at least **one structured FAQ document** in a **Q\&A tabular format** (best for AI Agents).
2. **If needed, set up API integrations** → Especially for **real-time or large, complex data sources**.
3. **Refine and optimize existing documents** → Ensure correct **structure, readability, and formatting**.

## **Need Help?**

📢 Feeling Overwhelmed? You don’t have to do this alone!

If you need assistance with managing a large volume of documents, automatically retrieving content from platforms like Google Drive, Confluence, or SharePoint, or optimizing and structuring your KB, we’re here to assist. [Reach out to us](../../need-help/our-customer-success-team.md), and we’ll ensure your KB is AI-ready with minimal effort on your part.

## Guides on Integrating or Uploading your Content

By now, you should have a clearer understanding of the next steps and the work required to build your KB. To help you move forward, explore the following articles for detailed guidance on fine-tuning and uploading your KB content using the two available methods:

1. [uploading-documents-to-your-kb.md](uploading-documents-to-your-kb.md "mention")
2. [integrating-your-kb-via-api.md](integrating-your-kb-via-api.md "mention").&#x20;
