# Debugging

The Debugging feature in the indigo.ai platform gives you **full visibility into how a message is generated**, making it easier than ever to **investigate issues**, **understand your flows**, and **optimize your assistant’s performance**.&#x20;

Whether you're **troubleshooting** an error, checking variable behavior, or **analyzing API calls**, Debugging provides a complete and accessible **toolkit right inside the platform**.

{% embed url="https://screen.studio/share/c8o9x6gu?_loop=1&autoplay=1" %}

## What It Does

The Debugging system offers a step-by-step reconstruction of what happens behind the scenes in each conversation. You can inspect:

* The full logic path through **agents and workflows**
* The **triggers**, **reroutes**, and **blocks** involved
* Detailed views of **variables**, **prompt blocks**, and **API calls**
* All components that contributed to the generation of a single message.

## Where to Access It

You can open the Debugging panel in two ways:

* From the **Chat section**: Under each assistant message, click on **"Details"**
* From the **Preview chat widget**: Debugging is integrated directly below each generated message

## The Debugging View

Once opened, you'll see a vertical timeline of the conversational flow, broken down into distinct sections:

* **Agents & Workflows Timeline**: See how the flow moved across agents and workflows.
* **Variables Panel**: Track all variable values and how they changed.
* **Prompt Blocks**: Inspect the input, output, and model details.
* **API Calls**: Analyze every call made during the conversation.

Each of these sections is organized to surface only what’s relevant for debugging, so you can focus on what matters.

## Key Debugging Elements

#### Agents & Workflows

At the top of the timeline, you’ll see how the flow moved between workflows and agents. You can follow every step, from the initial **trigger** to any **reroute**, **invocation**, or **handoff**, helping you understand the full conversation path.

#### Variables

Get a complete history of all variables involved in the flow:

* Listed in **temporal order**, showing when they were first used
* Displayed with their **value history**, showing every change
* Shows which block **influenced** each variable’s value
* For Prompt Blocks, it highlights if a variable was:
  * Used as **input**
  * Modified as **output**

#### Prompts

For every Prompt Block executed, you’ll see:

* Full **prompt content**, split into **input** and **output**
* Any **interpolated variables** with their values
* The **model** used for the generation
* **Response time** in milliseconds

This lets you understand exactly what the model saw and what it returned.

#### API Calls

Each API call is displayed with:

* Complete **logs** of headers and body
* Variable values used during the call
* **Response time** for the call execution

This is crucial when troubleshooting integrations with external systems.

#### Agent Blocks

Agent Blocks are treated like Prompt Blocks. You’ll see:

* The **prompt input and output**
* The **model** used for that agent

Since the Agent block operates like a Prompt Block, this section focuses on understanding how your AI Agent responded and what it based its answer on.

## Problem Solving Made Easy

Debugging is designed to help you troubleshoot autonomously. Whether you're fixing a broken workflow or fine-tuning performance, you can:

* Trace exactly **where and why** something went wrong
* Pinpoint issues with **variable logic**, **prompts**, or **API responses**
* Monitor execution speed for performance optimization.&#x20;
