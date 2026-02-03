---
description: Customize settings and embed the widget on your site.
icon: '5'
---

# Configure & Install the Web Chat

Through the **Settings & Installation > Web Chat** page, accessible via the platform's side menu (bottom-left corner), you can:

* Customize the chat experience to reflect your brand
* Access the code and setup instructions needed to install the virtual assistant on your website
* Enable new accessibility and engagement features, including [voice interaction](../product-updates/latest-product-releases/voice-in-web-chat-more-accessible-conversations.md).&#x20;

{% hint style="info" %}
This platform feature has been completely revised and updated, with the latest release launched in February 2025. Read more about this product release here: [the-next-generation-web-chat.md](../product-updates/latest-product-releases/the-next-generation-web-chat.md "mention").&#x20;
{% endhint %}

{% hint style="info" %}
For users who require more sophisticated interaction or need to integrate the chatbot in a more controlled manner, refer to this page: [advanced-web-chat-customization-and-installation-guide.md](../tech-deep-dives/web-chat-integration-and-customization-on-your-website/advanced-web-chat-customization-and-installation-guide.md "mention")
{% endhint %}

You can find the Web Chat Settings here:

{% embed url="https://screen.studio/share/ElTrPAPi?_loop=1&autoplay=1" %}
The location of the Web Chat settings button in the menu
{% endembed %}

{% embed url="https://screen.studio/share/zOGxd2mw?_loop=1&autoplay=1" %}
An overview of the widget settings with changes applied in real time.
{% endembed %}

Like the rest of the workspace, this page allows you to see your changes in real time. On the right side, you'll find the **widget preview**, where updates appear instantly as you make modifications. However, keep in mind that the messages and buttons shown in the preview are only examples and do not reflect your actual bot’s content.

Here’s an overview of the web chat installation settings:

When you're ready, hit the "**Save and Set Live**" button to apply and activate your changes immediately.&#x20;

Below, you'll find a detailed guide on navigating the 5 widget settings tabs, along with some recommendations for optimal setup and usage.

### Style

<figure><img src="../.gitbook/assets/Screenshot 2025-03-20 alle 12.27.54.png" alt=""><figcaption><p>Style Tab</p></figcaption></figure>

In the Style section, you can customize the chatbot’s appearance to match your brand identity.&#x20;

This includes setting the **assistant’s name** (max 35 characters) and adjusting the **chat message bubbles** and **text colors** for a consistent and cohesive design. When selecting colors, you can either enter a specific color code manually or use the visual color picker, which offers a full range of colors and gradient options.&#x20;

The **avatar** is the icon that appears next to the assistant’s name and every bot response. You can personalize it in two ways:

* **Upload an image file** (SVG format recommended for the best quality, max size: 5 MB)
* **Provide an image URL** to use an external source, allowing you to upload **short videos or animations** for a more dynamic experience.&#x20;

The **launcher** is the button users click to open the chatbot. You can customize it by:

* Uploading a custom icon (same upload rules as the avatar)
* Adding a descriptive text next to the icon
* Adjusting the button background and text color to match your design.&#x20;

Lastly, in the "View settings" area, you can control **where the chatbot appears on the page**:

* Position: Choose between right or left to best fit your website layout.
* Z-Index: Determines whether the chatbot appears above or below other elements on the page.
  * A higher value brings it to the front.
  * A lower value may cause it to be hidden behind other components.

### Home

<figure><img src="../.gitbook/assets/Screenshot 2025-04-04 alle 17.25.30.png" alt=""><figcaption><p>Home Tab</p></figcaption></figure>

{% embed url="https://screen.studio/share/kR79rEIu?_loop=1&autoplay=1" %}
Homepage customization options
{% endembed %}

The Home section lets you create a **dynamic and engaging landing page** for your chatbot. When users first access your chatbot, they are greeted with a **fully customizable homepage** that introduces your bot’s capabilities and guides them on how to get started.&#x20;

Everything on this page is optional, so you have full control over how much or how little you want to customize. We highly recommend personalizing your chat to enhance user engagement, but if needed, you can toggle off any elements you don’t want to display.

Customization Features:

* **Title and Subtitle**: Set up **welcome messages** that introduce your bot in a friendly and engaging way:
  * Title - Max 35 characters
  * Subtitle - Max 85 characters.
* **AI Animation**: Customize the animated visual above the welcome messages by adjusting its color to match your brand identity.
* **Grid of Images**: You can visually enhance your homepage by adding a grid of images to highlight key topics or actions. This section supports multiple configurations and now includes optional interactivity for each image.
  * **Layout Options**: Choose from five predefined grid layouts, allowing you to display between **1 and 4 images** in various formats depending on your design needs.
  * **Image Upload**: You can upload **static images or short videos** (following the same format and size rules as the avatar upload described earlier). Once uploaded, each image can be edited or removed at any time.
  * **Text Overlay**: Add a **short text label** above each image to describe its purpose. We recommend using **concise and action-oriented titles** to improve clarity and encourage user interaction (e.g., “Book an Appointment” or “Explore Products”).
  * **Optional Clickable Actions**: Each image can be configured as a [**quick reply**](../getting-started/blocks/action-blocks/quick-reply-block.md), offering the following interaction types:
    * **Start a Conversation**: Trigger a specific **Agent** or **Workflow**. In this case, assigning a text label is mandatory, as it will be used as the message sent in chat.
      * **Open an External Link**: Redirect users to an external webpage in a new browser tab. The text label is optional in this case.
      * **No Action**: Leave the image static, simply for visual or informative purposes.

{% hint style="info" %}
#### Image Formats and Dimensions

The images used follow standard aspect ratios for optimal display across layouts:

* **5:4 format** — almost square
* **21:9 format** — wide rectangle

Here are the recommended dimensions in pixels:

* **187 × 150 px** — small, nearly square
* **382 × 150 px** — wide rectangular format
* **317 × 298 px** — large, nearly square

Choose the appropriate format depending on your layout and visual emphasis.
{% endhint %}

*   **Typebar**: When enabled, the typebar allows users to start typing a message as soon as they enter the chat, creating a seamless and engaging experience. You can customize the placeholder text to guide users on what to type, making it easier for them to start a conversation.

    If the typebar is disabled, typically used in flows that begin with a predefined welcome message from the bot, the user will need to click "Start Chat" to initiate the conversation.
* **Example Questions**: Help users get started by providing up to 5 predefined questions (max 25 characters each). Since they are clickable, users can select a question and **receive an immediate answer**.

### Options

<figure><img src="../.gitbook/assets/Screenshot 2025-02-26 alle 14.40.32.png" alt=""><figcaption></figcaption></figure>

In the Options section, you can fine-tune how users interact with your chatbot by enabling features that enhance engagement and control its visibility.

* Auto-Start Chat: **Start the conversation automatically**, allowing the chatbot to open directly without displaying the homepage first.
* **Pop-up Message**: Display a customizable pop-up message above the bot’s launcher to invite users to interact. You can:
  * Personalize the message text
  * Set the delay time (in milliseconds) before the pop-up appears
  * Preview the pop-up before saving changes.&#x20;
* **Disable the Widget**: If needed, you can deactivate the chatbot widget without modifying your website’s code. Once disabled, the chatbot will no longer be visible on the site where it's installed.

### Voice

<figure><img src="../.gitbook/assets/Screenshot 2025-07-07 alle 12.14.07.png" alt=""><figcaption></figcaption></figure>

Add voice capabilities to make your web-chat based virtual assistant more **natural**, **accessible**, and **multimodal**.&#x20;

{% hint style="info" %}
🆕 This is a new feature released in June 2025. Check out this article to learn more: [voice-in-web-chat-more-accessible-conversations.md](../product-updates/latest-product-releases/voice-in-web-chat-more-accessible-conversations.md "mention")
{% endhint %}

#### **1. 🎙️ Voice Message**

**Allow users to speak instead of type**, even in regular chat mode.

* Enable the **"Voice Message"** toggle
* Users can record their voice from the typebar
* The system **transcribes** the speech and places it into the text input
* Users can edit or send the message directly after reviewing the transcription

#### 2. 🎧 **Listen Message**

Allow users to **hear any message the virtual assistant sends**, using a realistic voice powered by your selected provider.

* Enable the **"Listen Message"** toggle
* Select your **voice provider** (e.g., ElevenLabs) and desired voice
* Users will see a **speaker icon** beside each message. Tapping it plays the audio
* A loading animation appears before playback begins
* Users can **pause or stop** the audio at any time

### Installation

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

The Installation tab provides all the necessary information to seamlessly integrate your chatbot into your website.

#### **Web Chat Installation**

This is the primary code needed to display the chatbot on your site.\
Copy and paste the code snippet just before the closing `</body>` tag on each webpage where you want the chatbot to appear.&#x20;

#### **Test Script**

Use this script to test the chatbot’s functionality before officially installing it on your website. The test version will include any **debugging messages** configured during the setup process. \
Place the script in the **HTML of a test page** to ensure the chatbot is working correctly before deploying it live.

#### **Privacy Settings**

To help your organization comply with privacy regulations (such as GDPR), you can configure **Privacy Settings** directly in this tab.&#x20;

{% hint style="warning" %}
These settings are designed to support the **legal requirement to present a Privacy Policy before the user can interact with the virtual assistant**.
{% endhint %}

When enabled:

* You must provide a **URL to your Privacy Policy**, which will appear as a clickable link within the chat interface.
* You may also add a **link to your Terms of Service** (optional).
* You can optionally activate **explicit consent**, requiring users to check a box before sending a message or interacting with the assistant. \
  N.B. If only the Privacy Policy is provided (with explicit consent disabled), the policy link will still appear as required, but users can start chatting without checking any box.

When explicit consent is activated:

* The user will see a sentence such as: _"I agree to the terms of service and the privacy policy"_, with both items linked to the URLs you provide.
* The message input field remains active, but users won’t be able to send a message until they check the consent box.
* If a user tries to send a message without accepting the terms, the consent text will be highlighted in red to indicate the requirement.
* The banner appears **before** any message is shown, ensuring compliance from the first interaction.
* Consent is stored **per session**, meaning users won’t be asked again unless they reload the page or start a new session.

This banner will also prevent users from interacting with any quick replies, buttons, or other interaction elements until consent has been given.

{% hint style="info" %}
In platform Preview mode, the privacy banner is automatically hidden so it doesn’t interfere with the editing experience. It will be fully visible and functional in the live environment.
{% endhint %}
