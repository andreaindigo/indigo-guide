---
icon: file-check
---

# Docs & URLs

In this section, you can upload documents and add links to enrich your knowledge base. The system will use the content from your uploaded files and URLs to provide more accurate and informed responses.

<figure><img src="../../.gitbook/assets/indigo docs &#x26; urls.png" alt=""><figcaption></figcaption></figure>

#### 📄 Uploading Documents

To upload a document:

1. Click the Upload Documents button.
2. Select the file from your device.

Supported formats: .pdf, .docx, .txt, .csv, .xlsx

⚠️ Password-protected files are not supported.

#### 🔗 Adding URLs

To add a web page:

1. Paste the URL into the field.
2. Click Add URL.<br>

Once uploaded, you can **assign a Tag** to each document or URL.

<figure><img src="../../.gitbook/assets/indigo add tag to a doc.png" alt=""><figcaption></figcaption></figure>

Tags allow you to easily reference specific content later, for example when configuring your Agent.

<figure><img src="../../.gitbook/assets/indigo document to use tag.png" alt=""><figcaption></figcaption></figure>

#### 🏷️ Using Tags

The more you upload individual documents with specific tags, the better your Agent will be able to retrieve the right information from each file.

#### ♻️ Managing Your Content

You can:

* Replace an existing document with an updated version.
* Delete documents or URLs that are no longer needed.
* Refresh linked web pages to update the content used by your Agent.<br>

💡 If you make changes to a linked webpage, remember to click Refresh to ensure your Agent uses the latest version.

#### 🧩 Examples

**Example 1 – Document**

* Document: Product\_Manual.pdf – contains detailed descriptions of product features and pricing.
* Tag: product\_info
* Agent usage: When the Agent receives a question such as “How does the premium plan work?”, it retrieves the answer from Product\_Manual.pdf using the product\_info tag.<br>

**Example 2 – URL**

* URL: https://www.example.com/faq – contains the company’s Frequently Asked Questions page.
* Tag: faq
* Agent usage: When a user asks “What are the refund conditions?”, the Agent searches the content of the linked FAQ page (tagged as faq) and provides the correct answer.

#### 💡 Best Practices

* Use clear and descriptive filenames, e.g. User\_Guide\_2025.pdf instead of document1.pdf.
* Assign specific tags for each topic or category (e.g. pricing, support, technical\_specs).
* Avoid using the same tag for unrelated content.
* When updating a document, replace it instead of uploading a new file to keep the knowledge base organized.
* Periodically refresh URLs to ensure the Agent always uses the most up-to-date information.

### ⚙️ Advanced Document Processing

The advanced ingestion modal represents the first step of the **document processing workflow** and allows you to configure how documents are processed before being added to the knowledge base.

The modal is divided into two sections:

* **Left panel:** configure processing parameters (OCR, language, extraction mode, etc.) and start the process
* **Right panel:** preview of the processed document (available after processing is complete)

<figure><img src="../../.gitbook/assets/nuova rag 1.png" alt=""><figcaption></figcaption></figure>

Once processing is completed, you can:

* review the generated sections
* adjust parameters and reprocess the document
* upload the final result to the knowledge base

#### Processing Configuration

Available for supported document formats (`.pdf`, `.doc`, `.docx`):

* **Contains Handwritten Text**: enables advanced OCR for handwritten or complex table content (default: False)
* **Contains Non-English Text**: enables multilingual OCR (default: True)
* **Extraction mode**: OCR, Metadata, or Hybrid (default: OCR)
* **OCR mode**: tandard or Agentic (default: Standard)
* **OCR system**: highres, multilingual, combined, legacy (default: highres)
* **Chunking approach**: defines how content is split:
  * LLM-based (default)
  * Token-based
    * **Number of tokens**: visible only if Token-based is selected (min: 100, default: 700)
* **Process document**: starts processing (enabled only after parameter changes)

#### Document Preview

After processing, the right panel displays a structured preview of the extracted content:

* Content is divided into sections (e.g. _Section 1, Section 2_)
* Each section includes full text and character count
* Sections can be expanded or collapsed

<figure><img src="../../.gitbook/assets/nuova rag 3.png" alt=""><figcaption></figcaption></figure>

If the document has not been processed yet, the preview area remains empty with a loading state.
