---
icon: key
---

# Your Project Token

In this guide, you'll often see references to your **Project Token**—a key element for implementing advanced configurations. This token uniquely identifies your AI agents and is required for any API integration or script-based setup.&#x20;

You can find your Project Token in the installation scripts available under the **Settings > Installation** tab in your workspace.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-12 alle 17.01.37.png" alt=""><figcaption><p>Your project token</p></figcaption></figure>

{% hint style="info" %}
Throughout the documentation, we use the placeholders <kbd>`{{TOKEN}}`</kbd> or <kbd>`"project_token"`</kbd> to represent your actual token.&#x20;
{% endhint %}

### Live vs Test Environments

In the Installation section, you’ll notice two different scripts:

* **Live Script**: This script connects to the **live environment**, which reflects the latest published version of your AI agents. It’s the version your end users will interact with.
* **Test Script**: This script connects to the **test environment**, which is automatically updated every time you make a change in the workspace. It represents the version of your AI agents visible in the preview. The test script is ideal for validating new features, testing workflows, or experimenting with configuration changes before pushing them live—without affecting your users' experience.

{% hint style="info" %}
Learn more about how live and test environments work in this article: [configure-your-ai-agents.md](../build-your-ai-agents/configure-your-ai-agents.md "mention").
{% endhint %}
