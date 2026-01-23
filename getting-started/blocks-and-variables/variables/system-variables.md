# System Variables

System variables are **predefined, read-only variables** that are automatically managed by the indigo.ai platform. Unlike custom variables, they **cannot be edited** using blocks like [Set Value](../logic-blocks/set-values-block.md) or [Capture](../logic-blocks/capture-block.md). Instead, they provide **real-time context** about the user, session, platform environment, and conversation history, allowing you to create more intelligent and personalized experiences.

**They are always identified by the prefix `$`, e.g. `$project_id`.**

System variables help your AI Agents:

* Identify users, channels, and environments
* React based on the time and date
* Track conversation flow and user behavior
* Dynamically adapt logic based on platform state
* Access content retrieved via document search (RAG) or current workflow status

Use them to build smarter flows, trigger conditional logic, and create more relevant, responsive interactions.

## Categories and Variables

### 🌐 Platform & Session Context

* **`$install_url`** – The URL where the widget is installed (useful for multi-site setups).
* **`$project_id`** – Your workspace's unique identifier.
* **`$env`** – Returns `TEST` or `PRODUCTION`, depending on where the assistant is running.
* **`$lang`** – Language code set for the workspace (e.g., `en`, `it`).
* **`$detected_language`** – Language detected from the user's latest message.

### 👤 User Identification

* **`$user_id`** – Session-based ID for the current user.
* **`$user_ref`** – Persistent user identifier that remains consistent across sessions (ideal for CRM matching).

### 🕒 Time & Date

* **`$timestamp`** – Current time in seconds (Unix timestamp).
* **`$date`** – Full timestamp in your workspace’s timezone (`YYYY-MM-DD hh:mm:ss`).
* **`$date_year`, `$date_month`, `$date_weekday`, `$date_hour`** – Individual date components useful for business logic (e.g., trigger actions only during working hours).

### 🧠 Conversation & Context

* **`$last_user_message`** – Content of the user's most recent message or button click.
* **`$intent`** – Last recognized intent label.
* **`$message_id`** – ID of the most recent inbound message (for tracking or referencing externally).
*   **`$conversation`** – Full list of the last 100 messages in the current chat (in JSON format).

    ```json
    jsonCopiaModifica[
      {"sender": "bot", "text": "..."},
      {"sender": "user", "text": "..."}
    ]
    ```

{% hint style="info" %}
A “chat” refers to messages from the latest session, while a “conversation” spans all user interactions over time.
{% endhint %}

* `$context_1` to `$context_5` – Store the last 1 to 5 pairs of user and assistant messages in plain text. Ideal for use in prompts or as input for LLMs.

#### Behavior of the $last\_user\_message variable

**The `last_user_message` variable has a specific behavior:**

* It is aligned with other system variables by adding the `$` prefix → **`$last_user_message`**.
* It updates automatically:
  * after each user message,
  * even after a **capture block**.
* It can be used in agents and prompts always with the latest consistent value.

**Exception in the capture block**

If a capture block collects exactly the value of **`$last_user_message`**:

* a **dummy variable** is used,
* its only purpose is to allow the capture block to work,
* the captured value is **not** used later in the flow.

### 📚 Content & Workflow State

* **`$documents`** – A list of documents retrieved from your knowledge base. Use this to:
  * Display matched sources
  * Trigger logic based on content relevance
  * Chain actions across workflows using retrieved data
* **`$current_workflow`** – Label of the currently executing workflow.
* **`$previous_workflow`** – Label of the workflow executed immediately prior to the current one.

### ✅ Utility

* **`$true`** – A constant that always returns `true`. Handy for testing or creating unconditional branches in [Condition Blocks](../logic-blocks/condition-block.md).&#x20;

{% hint style="info" %}
It is possible to create **custom variables with the same name as a system variable**, but:

* modifying them does not update the system variable
* using them is not linked to the corresponding system variable
{% endhint %}
