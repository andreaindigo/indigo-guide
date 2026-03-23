# 📘 Digit Block

## Overview

The Digit block is a Voice Router–specific block that allows users to interact during a call using:

* Keypad input (DTMF)
* Voice responses

It is designed to create numbered voice menus, enabling users to select an option either by pressing a key or by speaking.

<figure><img src="../../../../.gitbook/assets/nuovo blocco.png" alt=""><figcaption></figcaption></figure>

### Interface

In the Indigo interface, the Digit block includes the following elements:

#### Message

The text that is read aloud to the user via text-to-speech (TTS).

It typically presents the available options in a numbered format.

Example:

_“Press 1 for Sales, 2 for Support”_

#### Keypad options

A list of selectable options that define the structure of the voice menu.

Each option includes:

* **Button label:** the numeric key the user presses (e.g. “1”, “2”, “3”)
* Connect: defines where the flow continues after selection:
  * another agent
  * a workflow
* **Variables:** allows assigning a value to a variable when the option is selected

You can add or remove options as needed (minimum: 1).

#### No match

A dedicated configuration button used to define the fallback behavior. From here, you can connect:

* a variable
* another agent
* a workflow<br>

This option is used when the user input does not match any of the defined keypad options.

Notes:

* It is always required
* It cannot be removed

### When to use it

Use the Digit block when you need to create a structured voice menu where users can:

* Choose between multiple options during a call
* Interact using keypad input (DTMF) or voice
* Be routed to different flows, agents, or variables based on their selection

**Typical use cases include:**

* IVR menus (e.g. Sales, Support, Information)
* Call routing and triage
* Guided user journeys over voice channels

