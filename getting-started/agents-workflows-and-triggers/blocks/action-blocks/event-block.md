---
description: Track an event within a workflow
icon: chart-line-up
---

# Event Block

## Overview

The **Event block** is a workflow component used to trigger and record an event at a specific point in the flow.

It allows you to measure when something happens during execution.

<figure><img src="../../../../.gitbook/assets/action event.png" alt=""><figcaption></figcaption></figure>

### When to use it

Use the Event block to:

* track key steps in a workflow
* measure conversions or user actions
* connect workflows to business metrics

### How it works

When the workflow reaches the block:

* the selected event is triggered
* a new occurrence is recorded
* metadata (if defined) is saved

The process is automatic and asynchronous.

### Configuration

<figure><img src="../../../../.gitbook/assets/action event 2.png" alt=""><figcaption></figcaption></figure>

#### Select event

Choose an event from the Events section.

You can select:

* Active events
* Disabled events (but they won’t be tracked)

#### Metadata (optional)

You can add dynamic data such as:

* workflow variables
* user input
* outputs from previous steps

### Metadata logic

The system combines:

* global metadata (defined in Events)
* local metadata (defined in the block)

Rule:

* values are merged
* local values override global ones

### Behavior by status

* **Active** → event is recorded
* **Disabled** → workflow continues, no tracking
* **Archived** → event not available and not tracked

The workflow is never interrupted.

### Error handling

* Tracking is asynchronous
* Automatic retries in case of failure
* Invalid metadata is still recorded with error flag
