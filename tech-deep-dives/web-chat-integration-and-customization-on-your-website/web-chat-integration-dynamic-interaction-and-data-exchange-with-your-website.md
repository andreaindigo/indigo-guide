# Web Chat Integration: Dynamic Interaction and Data Exchange with Your Website

This guide explores effective strategies for integrating your web application with a virtual assistant (chatbot), enhancing user interactions through dynamic communication and streamlined data exchange.

There are two main mechanisms to faciliate this communication:

1. Interacting with Widget Events
2. Passing Parameters through Script URLs.

## 1. Interacting with Widget Events

Once the script is loaded, a global variable <kbd>`IndigoAIChat`</kbd> becomes accessible on the page, enabling your web application to:

* **Listen to Events:** You can monitor specific events triggered by the chatbot, such as when it loads or responds to user interactions, which informs subsequent actions within your web environment.
* **Send Programmatic Messages:** Directly send text or command messages to the chatbot, mimicking user inputs to prompt specific responses from the chatbot.

To get started, register for the `widget-loaded` event on the `document` object to know when the chatbot becomes active:

```jsx
document.addEventListener('indigo-ai-widget-loaded', (event) => {
  console.log('The widget is loaded');
  console.log('You can find IndigoAIChat in:', event.detail.widget);
})
```

### **Opening and Closing the Chatbot**

Besides using its default button, the chatbot can be controlled using the `setOpen` method which accepts a boolean value:

```jsx
IndigoAIChat.setOpen(true);  // Opens the chat
IndigoAIChat.setOpen(false); // Closes the chat
```

This is useful when you want to utilize a custom button to toggle the chat's visibility. For instance, disabling the default open button via the `trigger=off` parameter in the script URL:

```html
<!DOCTYPE html>
<html>
<head>
    <button id="chat-trigger">Open Chat</button>
    <script>
        document.addEventListener('indigo-ai-widget-loaded', (event) => {
            var is_widget_open = false;
            document.getElementById("chat-trigger").addEventListener('click', (click_event) => {
                is_widget_open = !is_widget_open;
                event.detail.widget.setOpen(is_widget_open);
            })
        })
    </script>
    <script id="iaw-script" src="https://platform.indigo.ai/widget.js?token={{TOKEN}}&v=3&trigger=off"></script>
</body>
</html>
```

### Sending and Receiving Messages

You can send a message as if the user had typed something in the text bar using the following code:

```jsx
IndigoAIChat.sendMessage({type: 'text', text: 'A message'})
```

Similarly, you can emulate a button click:

```jsx
IndigoAIChat.sendMessage({type: 'postback', payload: 'label_answer'})
```

The payload is a label that represents a specific response set up in the project. You can also attach parameters to this payload, as described in the next section[#id-2.-passing-parameters-to-the-assistant](web-chat-integration-dynamic-interaction-and-data-exchange-with-your-website.md#id-2.-passing-parameters-to-the-assistant "mention"),  without needing to encode these values:

```jsx
IndigoAIChat.sendMessage({type: 'postback', payload: 'label_answer?value1=a&value2=cdb'})
```

### Monitoring Chat Events

You can listen for various events triggered by the widget by adding a _**callback**_ through the `on` method of <kbd>`IndigoAIChat`</kbd>:&#x20;

```jsx
IndigoAIChat.on('$message-sent', (data) => {
  // Here we define the behavior of the callback
})
```

To ensure that the <kbd>`IndigoAIChat`</kbd> object has been created on the page, it is recommended to place all the events in the _callback_ of the <kbd>`widget-loaded`</kbd> event:

```jsx
document.addEventListener('indigo-ai-widget-loaded', function (event) {
    event.detail.widget.on('$message-sent', (data) => {
      // Here we define the behavior of the callback
    })
})
```

{% hint style="info" %}
A callback is a function that is executed when a specific event occurs. For instance, in the example above, the event we are listening for is `$message-sent`, and our callback is the function provided after the comma.
{% endhint %}

* `$message-received` is triggered when a message arrives at the widget from the assistant.
* `$message-sent` is triggered when a message is sent from the widget to the assistant. This event also occurs for invisible system messages, which can be filtered by checking if the event data contains a _system_ field.
* `$answer` is triggered each time a user input leads through an answer on the platform. If there are [reroute](../../getting-started/blocks-and-variables/logic-blocks/reroute-block.md) blocks within an answer, multiple events are triggered.
* `$user-data-sent` is triggered when user data is updated.
* `$set-open` is triggered when the widget is opened or closed (does not apply if the chat is installed full screen).

Besides the `on` method, you can use the `once` method to register for an event only once. After receiving the event, the callback is executed and then removed:

```jsx
IndigoAIChat.once('$message-sent', (data) => {
  // Here we define the behavior of the callback
})
```

To manually remove event registration, you can rely on `off`:

```jsx
IndigoAIChat.on('$message-sent', (data) => {
  // Here we define the behavior of the callback
  // ...
  // Here we remove the event registration
  IndigoAIChat.off('$message-sent')
})
```

## 2. Passing Parameters to the Assistant

You can also pass data directly to the chatbot by including parameters in the chatbot script’s URL. This method allows you to preset the chatbot’s responses or personalize the chat based on user data:

```html
<script defer src="https://platform.indigo.ai/widget.js?token=PROJECT_TOKEN&v=3&init=init%3Fuser_id%3D1234%26contact_method%3Demail"></script>
```

This setup is beneficial for initializing the chatbot with specific information, such as user ID or preferred contact methods, enhancing personalized interactions right from the start.

The <kbd>**`init`**</kbd> parameter determines the first response provided to the user when they open the widget. The default value is **init**, which corresponds to the **Welcome** response on the platform. In addition to indicating other responses, it is possible to add parameters that the virtual assistant can then read and use to retrieve information or provide personalized responses. The parameters are passed in a _query-string_ format and _urlencoded_ (for more details on this, see the next paragraph). You can pass as many parameters as you want.

In the example, 2 parameters are passed:

* **user\_id** with the value _1234_
* **contact\_method** with the value _email_

Each parameter must have a variable with the same name in the workspace on the platform. This variable will contain the values passed to the widget and can be used to create flows.

### Understanding Query Strings and URL Encoding for Web Integration

#### **What is a Query String?**

A query string is a segment of a URL that assigns values to specified parameters. It starts with a "?" followed by key-value pairs connected by "=" and separated by "&". For example, the URL `https://www.example.com?user=mario&source=site` uses parameters `user=mario` and `source=site`.

#### **Handling Reserved Characters in URLs**

URLs contain reserved characters that have special functions and cannot be directly used in a query string. These include characters like `?`, `=`, and `&`, which need to be URL encoded to avoid misinterpretation by web browsers. Encoding changes these characters into a format suitable for transmission over the internet.

For instance, to incorporate the parameter `init=init?user_id=1234&contact_method=email` in a URL, it must be encoded due to its reserved characters. Tools like [URL Encoder](https://www.urlencoder.org/) can convert it to `init%3Fuser_id%3D1234%26contact_method%3Demail`.

#### Proper Formatting of Query Strings in Scripts

It's important to correctly format and encode query strings when embedding parameters in a script URL. Rather than directly appending parameters to the widget's URL, they should be added to the `init` parameter as a query string, effectively creating a URL within a URL. Here's the correct way to do it:

* Incorrect method: `<script defer src="https://platform.indigo.ai/widget.js?token=PROJECT_TOKEN&v=3&email=user@company.com"></script>`
* Correct method: `<script defer src="https://platform.indigo.ai/widget.js?token=PROJECT_TOKEN&v=3&init=init%3Femail%3Duser@company.com"></script>`

**Example of Dynamic Parameter Passing**

To dynamically pass parameters via code, you can use this JavaScript example:

```jsx
const project_token = "PROJECT_TOKEN";
const variables = new URLSearchParams({
  user_id: "1234",
  contact_method: "email"
});
const init = encodeURIComponent("init?" + variables.toString());

const script_tag = document.createElement("script");
script_tag.src = `https://platform.indigo.ai/widget.js?token=${project_token}&v=3&init=${init}`;
document.body.appendChild(script_tag);
```

This approach ensures that all parameters provided are automatically stored as variables in the user’s profile. To use these parameters in responses, simply declare variables with corresponding names in your project. These variables can then be used to tailor responses within the chatbot.

For instance, in the provided example, you would need to declare variables named `user_id` and `contact_method` in your project settings. These variables can then interact with the chatbot to provide personalized user experiences based on the data received.

### Passing Parameters to the Assistant in Real-Time

You can also update the user profile values in real-time using widget events.

The widget object exposes a `setVariables` method that accepts a map with keys as the names of the variables to be overwritten. Like other widget methods, the correct way to query them is within the `widget-loaded` event:

```jsx
document.addEventListener("indigo-ai-widget-loaded", (event) => {
  event.detail.widget.setVariables({ variable_1: "value_1", variable_2: "value_2" });
});
```

We can create a mechanism to update the user's language, for example:

```html
<!DOCTYPE html>
<html>
<head></head>
<body>
    <button id="changeLang">Change Language</button>
    <script>
    const langs = ["IT", "EN", "FR"];
    let langIndex = 0;
    document.addEventListener("indigo-ai-widget-loaded", (event) => {
      document.getElementById("change").addEventListener("click", () => {
        langIndex = (langIndex + 1) % langs.length;
        IndigoAIChat.setVariables({ lang: langs[langIndex] });
      });
    });

    const project_token = "PROJECT_TOKEN";
    const variables = new URLSearchParams({
      lang: langs[langIndex]
    });
    const init = encodeURIComponent("init?" + variables.toString())

    const script_tag = document.createElement("script");
    script.src = "https://platform.indigo.ai/widget.js?token=" +
        project_token +
        "&v=3&init=" +
        init;
    document.body.appendChild(script_tag);
    </script>
</body>
</html>
```

## Notes on User ID

Understanding and managing user IDs is crucial for personalizing interactions over multiple sessions.&#x20;

User IDs passed as parameters help initialize chatbot interactions with personalized data, while IDs used in event interactions enhance the tracking and personalization of the user journey.

### Managing User Identity Across Sessions with the Chatbot

Every user interaction with the chatbot generates a **unique alphanumeric identifier.**

This identifier is stored in the browser's _localStorage_ under the key _indigo-ai-widget-uid_ and helps maintain user identity across different sessions. If a user interacts with the widget today and returns tomorrow using the same browser, we can recognize them by this identifier.

{% hint style="warning" %}
If a user clears their browser cache, the identifier will be lost, and we will no longer be able to recognize them in future sessions.
{% endhint %}

#### **Overriding the User Identifier**

It is possible to manually override this identifier if you need to implement specific logic, such as linking chatbot users to an in-house authentication system. Proper management of this mechanism allows for extending user recognition across multiple devices.

{% hint style="warning" %}
**Setup Requirement:** The identifier must be set before the chatbot widget is loaded onto the page:
{% endhint %}

```jsx
localStorage.setItem("indigo-ai-widget-uid", "custom-user-id");
```

#### **Advantages of Linking Chat ID with System User ID**

Linking the chatbot's user ID with a system-specific user ID allows for easy tracking and association of chat conversations with specific users. This connection can greatly simplify how interactions are monitored and analyzed, providing a more integrated user experience across your services.

### Overriding Usernames

In our platform, you've likely visited the **Chats** section to see how the assistant can help your users. You've also noticed that users are anonymous and that we assign them a friendly animal name as a recognition for the chat.

You can override the username by passing a new parameter <kbd>`custom_user_ref`</kbd> with the value of the new name as illustrated in the section [Passing Parameters to the Assistant](web-chat-integration-dynamic-interaction-and-data-exchange-with-your-website.md#id-2.-passing-parameters-to-the-assistant).

If necessary, you can manually override the default user ID, useful for aligning users across different systems or devices:

```jsx
<script defer src="https://platform.indigo.ai/widget.js?token=f1be469c-6e57-4fa9-a00a-acd03e0445f2&v=3&init=init%3Fcustom_user_ref%3DBEAUTIFUL_NAME"></script>
```

This approach is particularly beneficial for integrating chat interactions with existing user databases, allowing for a unified user experience across platforms.

### Customizing the User Reference

In addition to overriding the displayed username, it is also possible to **customize the internal user reference (`user_ref`)**.\
This feature, recently introduced, is particularly useful for customers who need to align chat users with identifiers coming from external systems (such as CRM, authentication systems, or internal databases).

By passing the `uid` parameter when loading the widget, you can explicitly set the `user_ref` associated with the user session.

Example:

```html
<script defer
  src="http://localhost:4001/widget.js?token=f1f18a18-ea8a-481b-a3f0-9c6dbd8b0d4f&v=3&uid=user_ref_custom">
</script>
```

When provided, the value of `uid` will be used as the user’s unique reference instead of the automatically generated one.
