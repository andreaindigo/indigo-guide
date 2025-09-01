---
description: >-
  Explore advanced techniques for integrating and customizing our chatbot on
  your website.
---

# Advanced Web Chat Customization and Installation Guide

This guide is intended for users who require more advanced interactions or greater control over the web chat integration on their website.

## Web Chat Interface Components

The installation script generates several **DOM nodes**, each representing a different part of the chat widget interface:

* <kbd>**`iaw-container`**</kbd>: The main container that holds all other web chat elements.
* <kbd>**`iaw-trigger`**</kbd>: A button that opens and closes the chat widget.
* <kbd>**`iaw-bubble`**</kbd>: A chat invitation bubble that appears initially and is removed after the first chat session begins or when the user clicks the close button.
* <kbd>**`iaw-chat`**</kbd>: The main chat interface where users can send messages and view ongoing conversations.

Clicking `iaw-trigger` opens the chat interface (`iaw-chat`), allowing interaction with the web chat.

{% hint style="warning" %}
To prevent external page styles from altering the chat's appearance, chat elements are contained within an `iframe` inside `iaw-chat`.
{% endhint %}

## Customizing Web Chat Interaction

Knowing the IDs of the web chat interface components is helpful for tailoring interactions specific to your site. For instance:

* To hide the widget, use the CSS style:

```css
#iaw-container {
    display: none;
}
```

* To toggle the widget's visibility with a button, use the following JavaScript:

```javascript
document.getElementById("id-button").addEventListener("click", function() {
    var container = document.getElementById("iaw-container");
    container.style.display = (container.style.display === 'none' ? '' : 'none');
});
```

## Custom Web Chat Initialization

### Message on Loading

By default, the newest version of our widget (v=3) **does not send a message upon page load**. Instead, it waits for the user to initiate the chat. This behavior ensures that the widget only engages when the user explicitly starts the conversation.

If you'd like the widget to **send a greeting message automatically when the page loads** , you can enable the auto-start feature by adding `autostart=on` to the widget URL:

```html
<script defer src="https://platform.indigo.ai/widget.js?token={{TOKEN}}&v=3&autostart=on"></script>
```

### Trigger-Based Loading

In scenarios where you want to **load the widget following a specific event** (e.g., page scroll, cookie policy acceptance), our widget can be dynamically installed using JavaScript rather than an HTML tag:

```javascript
const project_token = "PROJECT_TOKEN";
const script_tag = document.createElement("script");
script_tag.src = "https://platform.indigo.ai/widget.js?token=" + project_token + "&v=3";
document.body.appendChild(script_tag);
```

{% hint style="info" %}
For examples of custom widget installations, such as loading it on a button click, after a delay, or upon scrolling, you can refer to this page: [code-examples-for-common-widget-integrations-on-your-web-page.md](code-examples-for-common-widget-integrations-on-your-web-page.md "mention").
{% endhint %}

## Customizing Individual Widget Components

For enhanced customization and control over how the web chat integrates with your website, you have the option to install each component individually. Each component is assigned a fixed ID, which you can use to develop custom styles that take precedence over the default settings. This allows you to fully customize the chat's appearance and behavior.

#### Widget Components

* **JavaScript File** - Generates the interface and manages interactions.
* **Stylesheet** - Determines the widget’s visual appearance.

Each component can be inserted individually, making the chat content available in any HTML element (`<div>` or `<iframe>`), ensuring full configuration.

{% hint style="danger" %}
We recommend careful handling of the elements as improper modifications could negatively impact the user experience. Make sure to manage styles and scripts carefully to prevent conflicts with the existing styles on your page.
{% endhint %}

### Installing the Web Chat Widget on Full Page / Mobile

For direct page installation (full page or mobile through web view) add the components in order: Stylesheet, Chat Node and Chat Script, as in this example:&#x20;

```html
<!DOCTYPE html>
<html>
<head>
    <link type="text/css" rel="stylesheet" href="https://platform.indigo.ai/widget.css?v=3"/>
    <style>
    #chat {
        position: absolute;
        top: 0;
        left: 0;
        z-index: 1;
        width: 100%;
        height: 100%;
    }
    </style>
</head>
<body>
    <div id="chat">
        <div id="chat-content"></div>
    </div>
    <script id="iaw-script" src="https://platform.indigo.ai/widget_standalone.js?token={{TOKEN}}&v=3&fullpage=on&fullpage_close=off&node=chat-content"></script>
</body>
</html>
```

#### 1. Stylesheet

The CSS file provides the essential styles for displaying the chat widget's components, ensuring an optimal user experience.&#x20;

However, sometimes the chat’s appearance on your webpage may differ from its preview on the platform. This discrepancy typically occurs when custom styles on your site override or conflict with the widget's default styles. To avoid such issues, it is recommended to **load the widget's stylesheet last**, after all other custom style files on your website. This ensures that the widget's styles take precedence.

For instance, if you'd like to **change the font displayed in the web chat**, you can inject custom CSS and include additional fonts. **Both the homepage and chat fonts can be customized.**

Here are some examples of how you can modify the widget’s configuration to apply custom styles:

*   **Customizing the title in the homepage**: This style targets the title and changes its font to Arial.

    ```css
    .iaw-home-container>div>[class*='_title'] { font-family: arial !important; }
    ```
*   **Customizing the subtitle in the homepage**: This style changes the subtitle font to serif.

    ```css
    .iaw-home-container>div>p { font-family: serif !important; }
    ```

By including these custom styles, you can ensure that the widget fits seamlessly with your website's design and branding.

#### 2. Chat Container Node

The container node is an element identified by an ID and targeted by the script. As shown in the example above, this node is nested within another container. This structure offers greater flexibility in **managing your page layout**, ensuring that the chat's styles do not override or conflict with your page's existing styles.&#x20;

The external container (called `chat` in our example) can be customized to fit the style of your website, while the internal container (`chat-content`), which contains the actual chat interface, should typically remain unchanged to preserve the chat functionality and design as intended.

#### 3. Chat Script

The script contains three additional attributes that extend beyond the standard setup:

* **fullpage:** Enables full-page chat mode when set t&#x6F;**`on`**; defaults to the standard chat interface if omitted.
* **fullpage\_close:** Adds a close button to the full-page chat interface when set to **`on`**.
* **node:** Specifies the ID of the HTML node for chat installation (e.g., `node="chat-content"`).

## Isolating the Widget

To prevent interference with other page elements, isolate the widget using an iframe:

```html
<!DOCTYPE html>
<html>
	<body>
		<iframe id="frame"></iframe>

		<script>
		  let frame = document.querySelector('#frame');
		  frame.srcdoc = `
				<!DOCTYPE html>
				<html lang="it">
					<head>
						<link type="text/css" rel="stylesheet" href="https://platform.indigo.ai/widget.css?v=3"/>
					</head>
					<body>
						<div id="chat">
							<div id="chat-content"></div>
						</div>
					</body>
				</html>`;
			const token = 'PROJECT_TOKEN';	
		  let script = document.createElement('script');
		  script.id = 'iaw-script';
		  script.src = 'https://platform.indigo.ai/widget_standalone.js?token=' + token + '&v=3&fullpage=on&fullpage_close=off&node=chat-content';
		  frame.addEventListener('load', function addScript() {
		    frame.contentDocument.body.appendChild(script);
		  });
		</script>
	</body>
</html>
```

## Web chat Installation Using Third-Party Tools

Our widget is highly adaptable and can be installed using tools commonly utilized across web pages.

### Google Tag Manager

You can deploy our widget via **Google Tag Manager** by creating an **HTML** tag. This tag will contain the widget's script or its individual components, as outlined earlier. For guidance on creating an **HTML** tag, refer to the [official Google guide](https://support.google.com/tagmanager/answer/6107167?hl=en\&sjid=10655303235011344164-EU).&#x20;

### Mobile App Installation

Although we do not offer an **SDK** for direct installation on mobile devices, our chat can be integrated into a mobile app using a **webview**. This method allows the widget to operate seamlessly within mobile applications, ensuring a consistent user experience across devices.

## Uninstalling the Widget

If you need to remove the widget from a page—for example, to reinstall it and restart the conversation after logging into a Single Page Application (SPA)—simply delete the node that contains the widget (usually identified as `iaw-container`) along with any related script. This will effectively clear the widget from your page, allowing you to set it up again from scratch as needed.
