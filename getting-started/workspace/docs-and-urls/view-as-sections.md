# View as Sections

### Overview

The **View as Sections** feature introduces an advanced table view within the **Docs & URLs** section.

It allows you to switch from the default document list view to a structured table where each row represents a **knowledge section** generated during document processing.

<figure><img src="../../../.gitbook/assets/section view 1.png" alt=""><figcaption></figcaption></figure>

Each uploaded and processed document becomes a source of sections, aggregated into a single table designed to support:

* dynamic search and filtering
* navigation across documents and sections
* contextual metadata editing
* detailed inspection via side panel

#### How it works

* **Upload & Processing**\
  The document is uploaded and processed through the ingestion pipeline, generating structured knowledge sections.
* **Switch to Sections View**\
  Move from the document list to the **Sections table view** to access all generated sections.
*   **Browse & Search**\
    In the table, you can filter and search sections by:

    * ID
    * Document
    * Title
    * Type

    Keyword search also scans the full text of each section, even if not directly visible in the table.
* **View Details**\
  Click on a row to open the side panel and view the full content and metadata of the selected section.
* **Enrich Data**\
  Use the fixed right-side columns to:
  * add new fields
  * edit values
  * label and enrich section data
* **Save Changes**\
  All updates are saved and synchronized with the database, making metadata available to the model.

#### Section Details Panel

Clicking on a row opens a right-side panel with:

* section ID
* source document (with link)
* full editable text
* editable title
* content type
* additional metadata fields (single value per field)
* page range (when available, e.g. for PDFs)

This panel allows quick inspection without leaving the table and supports direct editing of section content and metadata.

<figure><img src="../../../.gitbook/assets/section view 2.png" alt=""><figcaption></figcaption></figure>

#### Custom Columns

The fixed right-side area of the table is dedicated to enriching sections:

* add custom columns (e.g. Category, Product, Notes)
* assign values directly in cells
* apply values to multiple rows using checkboxes

By default, the area shows an empty column with an add button. As columns are added, they remain fixed during horizontal scrolling.

<figure><img src="../../../.gitbook/assets/section view 3.png" alt=""><figcaption></figcaption></figure>

#### Add Sections or Import Data

From the actions menu, you can:

* add a new text section
* import files (`.csv`, `.xls`, `.xlsx`)

<figure><img src="../../../.gitbook/assets/add section.png" alt=""><figcaption></figcaption></figure>

New entries are added as grouped rows labeled **“Section added”** within the related document.

#### Manage Added Sections

Manually added sections can be easily managed from the table:

* **Delete sections** → remove selected sections
* **Hide sections** → temporarily exclude sections without deleting them

You can apply these actions to one or multiple sections using the checkboxes.

<figure><img src="../../../.gitbook/assets/hide section.png" alt=""><figcaption></figcaption></figure>
