---
description: Manage and analyze events across your workspace
icon: chart-line-up
---

# Events

### Overview

Events allow you to create, track, and manage **custom actions** that happen across your workflows and agents.

An event represents a meaningful business action, such as:

* lead qualification
* appointment booking
* payment failure

Events turn conversations into measurable business data.

### Where to find Events

Go to:

**Utilities → Events**

This is the central place to manage all events in your workspace.

<figure><img src="../../../.gitbook/assets/custom event.png" alt=""><figcaption></figcaption></figure>

### What you can do

#### Create events

Define custom events to use in workflows and agents.

<figure><img src="../../../.gitbook/assets/create event.png" alt=""><figcaption></figcaption></figure>

To create a new event:

1. Click **Create event**
2. Fill in the required fields:
   * **Event name**
   * **Description**
   * **Metadata schema** (optional)
3. Click **Create Event**

The event will be automatically available in workflows and agents.

#### Monitor events

The table shows:

* Event name
* Event key (unique identifier)
* Total triggers
* Last triggered
* Status (Active / Disabled)
* Created by

#### Filter and analyze

You can filter events by:

* timeframe
* status
* creator
* usage (workflow / agent)

And sort by:

* most recent
* most triggered

<figure><img src="../../../.gitbook/assets/filtro eventi.png" alt=""><figcaption></figcaption></figure>

#### Export data

Export event triggers as a CSV file.

<figure><img src="../../../.gitbook/assets/export events.png" alt=""><figcaption></figcaption></figure>

The export includes:

* event
* timestamp
* user
* metadata
* source (workflow or agent)

Export is asynchronous and sent via email.

### Event status

Each event can be:

* **Active** → tracks occurrences and is usable
* **Disabled** → visible but does not track
* **Archived** → not usable but keeps historical data

### Metadata

Metadata allows you to enrich events with additional information.

Examples:

* transaction value
* service type
* user ID

### Advanced features

#### Set values

Automatically update variables when an event is triggered.

#### Webhooks / API

Send event data to external systems (CRM, analytics, etc.).

### Summary

Events help you:

✔ Track key actions\
✔ Analyze performance\
✔ Export data\
✔ Integrate external systems
