---
icon: list-tree
---

# Audit logs

Audit Logs is a new section available in the workspace settings, dedicated to viewing logs, i.e. all actions performed within the workspace.\
Its purpose is to provide a clear, structured, and searchable overview of **user activity**.

<figure><img src="../../../.gitbook/assets/audit logs 1.png" alt=""><figcaption></figcaption></figure>

### Benefits

Audit Logs allows you to:

* track all actions performed within the workspace;
* improve transparency and control over workspace creation, editing, and management processes;
* introduce a level of analysis and investigation that was not previously available.

### Page structure

The Audit Logs page is structured into three main sections:

1. **Header**   \
   Includes the page title, a short description of the available features, and a button to export data in CSV format.
2. **Filters and actions**   \
   Allows users to filter and customize the search (for example by time range, category, or user), making it easier to find relevant information.
3. **Action list**   \
   Displays the list of recorded actions, with pagination and the ability to choose how many rows are shown per page.

<figure><img src="../../../.gitbook/assets/audit logs 2.png" alt=""><figcaption></figcaption></figure>

### Displayed data

Each recorded action in the table includes the following information:

* **User**: the user who performed the action;
* **Date/Time**: when the action was executed;
* **Action**: details of the action performed (for example, “added tag”).

### Tracked events

Tracked events include most of the actions available on the platform, providing a comprehensive view of all activity within the workspace.

<table><thead><tr><th width="164">Category</th><th width="281">Event</th><th>Log</th></tr></thead><tbody><tr><td>Publish</td><td>publish on next env</td><td>Workspace published on staging</td></tr><tr><td>Publish</td><td>publish on prod</td><td>Workspace published on production</td></tr><tr><td>Chats</td><td>start human takeokver (click su bottone in chat)</td><td>started human takeover for chat {{conversation_link}}</td></tr><tr><td>Documents</td><td>upload document</td><td>uploaded document {{document_link}}</td></tr><tr><td>Documents</td><td>insert URL</td><td>inserted URL {{url}}</td></tr><tr><td>Documents</td><td>replace document</td><td>replaced document {{document 1}} with {{document 2}}</td></tr><tr><td>Documents</td><td>add tag to document</td><td>added tag {{tag}} to {{document}}</td></tr><tr><td>Documents</td><td>delete tag to document</td><td>deleted tag {{tag}} to {{document}}</td></tr><tr><td>Utilities: Conversation Logs</td><td>export CSV</td><td>Exported Conversation Logs data</td></tr><tr><td>Utilities: Issues</td><td>create issue</td><td>Created issue {{identifier}}</td></tr><tr><td>Utilities: Issues</td><td>delete issue</td><td>Deleted issue {{identifier}}</td></tr><tr><td>Utilities: Issues</td><td>edit issue</td><td>Edited issue {{identifier}}</td></tr><tr><td>Utilities: Evaluators</td><td>add evaluator</td><td>Added evaluator {{evaluator_link}}</td></tr><tr><td>Utilities: Evaluators</td><td>edit evaluator</td><td>Edited evaluator {{evaluator_link}}</td></tr><tr><td>Utilities: Evaluators</td><td>activated evaluator</td><td>Activated evaluator {{evaluator_link}}</td></tr><tr><td>Utilities: Evaluators</td><td>export CSV</td><td>Exported Evaluators data</td></tr><tr><td>Agent settigns</td><td>change global agent settings</td><td>changed Global Agent Settings</td></tr><tr><td>Variables</td><td>add variable</td><td>Added variable {{variable}}</td></tr><tr><td>Variables</td><td>edit variable</td><td>Edited variable {{variable}}</td></tr><tr><td>Variables</td><td>delete variable</td><td>Deleted variable {variable}}</td></tr><tr><td>Variables</td><td>add secret</td><td>Added secret {{secret}}</td></tr><tr><td>Variables</td><td>delete secret</td><td>Deleted secret {{secret}}</td></tr><tr><td>Settings: Workspace</td><td>edit WS name</td><td>Edited Workspace name</td></tr><tr><td>Settings: Workspace</td><td>edit URL</td><td>Edited Workspace URL</td></tr><tr><td>Settings: Workspace</td><td>edit timezone</td><td>Edited Workspace timezone</td></tr><tr><td>Settings: Workspace</td><td>enable multilanguage</td><td>Enabled multilanguage</td></tr><tr><td>Settings: Workspace</td><td>change primary language</td><td>Changed primary language with: {{lang}}</td></tr><tr><td>Settings: Workspace</td><td>reset translations</td><td>Has reset translations</td></tr><tr><td>Settings: Workspace</td><td>export content</td><td>Exported Chats and Knowledge base data</td></tr><tr><td>Settings: Team</td><td>invite user</td><td>Invited member {{email}} as {{role}}</td></tr><tr><td>Settings: Team</td><td>change role</td><td>Changed role of {{email}} with {{role}}</td></tr><tr><td>Settings: Team</td><td>delete user</td><td>Deleted user {{email}}</td></tr><tr><td>Settings: Handover</td><td>turn handover on/off</td><td>Turned handover on/off</td></tr><tr><td>Settings: Handover</td><td>edit closing days</td><td>Edited handover closing days</td></tr><tr><td>Settings: Web Chat</td><td>edit web chat widget</td><td>Edited web chat widget</td></tr><tr><td>Builder</td><td>create agent</td><td>Created agent {{agent}}</td></tr><tr><td>Builder</td><td>create workflow</td><td>Created workflow {{workflow}}</td></tr><tr><td>Builder</td><td>edit agent</td><td>Edited agent {{agent}}</td></tr><tr><td>Builder</td><td>edit workflow</td><td>Edited workflow {{workflow}}</td></tr><tr><td>Builder</td><td>delete agent</td><td>Deleted agent {{agent}}</td></tr><tr><td>Builder</td><td>delete workflow</td><td>Delete workflow {{workflow}}</td></tr></tbody></table>
