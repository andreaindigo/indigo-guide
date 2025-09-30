# Non-Conversational Triggers

### 📌 Overview

Non-Conversational Triggers allow indigo.ai agents and workflows to be activated by external events, such as calendar updates, GitLab merge requests, or tickets created via Zapier.\
This article explains how to configure the two available REST endpoints, set up webhooks, and use advanced variables (List and Map) in your payloads.



### 🔗 Endpoints

Indigo.ai provides two REST endpoints for triggering:

* **Async endpoint** →\
  https://platform.indigo.ai/rest/trigger/async/\{{project\_token\}}
  * Returns HTTP status 200 immediately upon receiving the request.
  * Does not wait for the execution of the agent or workflow.
  * Use case: when you don’t need the agent’s response.\


**Example response:**  {"status": true}

* **Sync endpoin**t →\
  https://platform.indigo.ai/rest/trigger/sync/\{{project\_token\}}
  * Waits until the agent/workflow has completed execution.
  * Returns the generated response.
  * Use case: when immediate feedback is required (validation, content generation, forwarding to another system).\


**Example response:**\
{

&#x20; "messages": \[

&#x20;   {"caption": false, "html\_text": "\<p class=\\"slate-p\\">text\</p>", "text": "text"},

&#x20;   {"caption": false, "html\_text": "\<p class=\\"slate-p\\">another text\</p>", "text": "another text"}

&#x20; ],

&#x20; "status": true

}

### ⚙️ Webhook setup

To trigger an Indigo.ai agent or workflow from an external event, you can configure a webhook in your system.

#### Example: GitLab – Triggering an agent when a Merge Request is created

1. Open Settings → go to the Webhooks section.

Enter the Indigo endpoint: https://platform.indigo.ai/rest/trigger/\{{type\}}/\{{project\_token\}}

2. &#x20;Replace:
   1. \{{project\_token\}} → your Indigo project token.
   2. \{{type\}} → sync or async.
3. Add the authentication header:
   1. Name: Authorization
   2. Value: Bearer pat-\{{personal\_access\_token\}}
4. Select events → check Merge Request events (or Releases events, Deployment events, etc., depending on your needs).
5. Add a payload including:
   1. target → the label of the agent/workflow to be triggered (use the DB label, not the platform display name. Example: Merge Request → merge\_request).
   2. data → the information to pass into Indigo.ai, available in the platform as variables.\


**Example payload:**\
\
{

&#x20; "target": "mr",

&#x20; "data": {

&#x20;   "action": "\{{object\_attributes.action\}}",

&#x20;   "user": "\{{user.name\}}",

&#x20;   "project": "\{{project.name\}}",

&#x20;   "draft": \{{object\_attributes.draft\}},

&#x20;   "detailed\_merge\_status": "\{{object\_attributes.detailed\_merge\_status\}}"

&#x20; }

}

6. &#x20;No need to predefine these variables in the platform.
7. Save and test → verify that the event correctly triggers the target agent or workflow (e.g., by adding an API block or email block).\


### 🔄 Other integrations

Besides GitLab, many external platforms can trigger Indigo.ai agents:

* Zapier → trigger on new emails, tickets, or Google Calendar updates using Webhook by Zapier → POST.
* Calendars (Google, Outlook) → trigger when a meeting starts (via Zapier or Make).
* CRM & Help Desk (e.g., Zendesk, Hubspot) → trigger on ticket creation or updates.\


### 📊 Advanced: new variable types

To support more complex payloads, Indigo.ai introduces two new variable types:

* **List** → an ordered collection of values (integers, strings, lists, or maps).
  * Example: \[1, "two", \[3], {"value": 4}]
* **Map** → a set of key–value pairs, where values can be integers, strings, lists, or maps.
  * Example: {"key\_1": 1, "key\_2": "value"}\


ℹ️ These variables behave like any other in the platform and can be inspected in the debugger.\
For details, see the[ Variable Guide](https://www.notion.so/Variabili-c8f99e8009d94af1a84f7c7066fdef06?pvs=21).
