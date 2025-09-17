---
icon: phone-hangup
---

# Hang up Block

The Hang up block allows you to end a voice call at specific points in the flow. It is available among the Action blocks and works only in voice workflows (it is skipped in text chats and web calls).

<figure><img src="../../../.gitbook/assets/kb_hangup 1.png" alt=""><figcaption></figcaption></figure>

You can add **multiple Hang up blocks** in the same workflow, but only the first one executed will actually close the call and, if configured, trigger a post-call workflow.

\
Additionally, the block can be set to start a workflow right after the call ends, enabling follow-up actions such as call classification, API requests, or sending emails.

<figure><img src="../../../.gitbook/assets/kb_hangup 2.png" alt=""><figcaption></figcaption></figure>

### Hang up Block – Functional Requirements

* **Placement**: The block can be used at any point in a workflow and can appear multiple times. However, the call will end as soon as the block is executed the first time.
* **Call termination**: When executed, the block immediately closes the voice call.
* **Post-call actions**:
  * If no destination workflow is selected, the call simply ends.
  * If a destination workflow is selected, it starts right after the call ends. In this case, the block internally performs a reroute to the chosen workflow.
* **Deleted workflows**: If the destination workflow linked to a Hang up block is deleted, it will no longer appear as a selectable option.



**Important note on multiple Hang up blocks**

The reroute action linked to a Hang up block can only happen if the call is still active when the block is executed.

This means that:

* If you add more than one Hang up block in the same workflow, only the first one will actually close the call and (optionally) trigger a post-call workflow.
* If the post-call workflow started by a Hang up block also contains another Hang up, that second block won’t do anything—because the call has already ended.\


💡 **In short**: once the call is closed, it’s not possible to trigger new flows with other Hangup blocks. Each Hangup can be used only once to end the call and optionally start a post-call workflow.

