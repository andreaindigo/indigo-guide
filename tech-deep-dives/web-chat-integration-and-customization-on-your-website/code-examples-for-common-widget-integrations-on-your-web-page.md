# Code Examples for Common Widget Integrations on Your Web Page

In this article, you'll find a collection of practical, ready-to-use code snippets designed to help you customize your widget installations based on various user interactions and scenarios.&#x20;

Each section below details a specific use case, accompanied by the corresponding code that you can directly copy and paste for immediate implementation.

## Custom Widget Initialization

### On Button Click

```html
<!DOCTYPE html>
<html>
<head></head>
<body>
    <button id="widget-loader">Load Widget</button>
    <script>
        var widget_loaded = false;
        document.getElementById("widget-loader", function(event) {
            // Prevent double loading
            if (!widget_loaded) {
                widget_loaded = true;
                // Load the widget
                const project_token = "PROJECT_TOKEN";
                const script_tag = document.createElement("script");
                script.src = "https://platform.indigo.ai/widget.js?token=" + project_token + "&v=3";
                document.body.appendChild(script);
            }
        })
    </script>
</body>
</html>
```

### After a Specified Time Delay

```html
<!DOCTYPE html>
<html>
<head></head>
<body>
    <script>
        // Define a 3-second wait
        // Time is in milliseconds
        const timeout = 3000;
        // Define the widget
        const project_token = "PROJECT_TOKEN";
        const script_tag = document.createElement("script");
        script.src = "https://platform.indigo.ai/widget.js?token=" + project_token + "&v=3";
        // Load the widget after the timeout
        setTimeout(function() {
            document.body.appendChild(script);
        }, timeout);
    </script>
</body>
</html>
```

### **On Scroll to a Specific Element**

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        .content {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 2000px;
            width: 100%;
        }
        .content > .content {
            height: 90%;
            width: 90%;
        }
    </style>
</head>
<body>
    <div class="content" style="background-color: blue"></div>
    <div class="content" style="background-color: red">
        <div class="content" style="background-color: white"></div>
    </div>
    <div class="content" style="background-color: yellow">
        <div class="content" style="background-color: purple">
            <div class="content" style="background-color: aquamarine">
                <!-- This is the element to reach to load the widget -->
                <div
                    id="scroll-to"
                    class="content"
                    style="background-color: beige"
                ></div>
            </div>
        </div>
    </div>
    <script>
        const project_token = "TOKEN";
        const script_tag = document.createElement("script");
        script_tag.src =
            "https://platform.indigo.ai/widget.js?token=" +
            project_token +
            "&v=3";
        // Retrieve the distance from the top of the page
        // to the element we want to reach
        const scrollToElementOffset =
            document.getElementById("scroll-to").offsetTop;
        // The widget should only load once
        var widget_loaded = false;
        document.addEventListener("scroll", (event) => {
            // Check that the widget has not already been loaded
            if (
                !widget_loaded &&
                // And that the element is visible at the top of the page
                (window.pageYOffset >= scrollToElementOffset ||
                // or that we have reached the bottom of the page
                window.pageYOffset + window.innerHeight >=
                    document.body.offsetHeight)
            ) {
                widget_loaded = true;
                // Include the widget
                document.body.appendChild(script_tag);
            }
        });
    </script>
</body>
</html>
```

## Interacting with the Widget

### **Opening the Widget After a Delay**

```html
<script type="text/javascript">
    document.addEventListener('indigo-ai-widget-loaded', function () {
        const timeout = 3000;
        setTimeout(function (event) {
            event.detail.widget.setOpen(true);
        }, timeout);
    });
</script>
```

## Page Actions Triggered by Events

### **Actions Triggered by an Answer**

An interesting scenario to consider is triggering a modal when a specific response is activated in the bot.

For example, consider a situation where you want to prompt user registration after a series of message exchanges culminates in the bot delivering a <kbd>`registration`</kbd> response. In such cases, we can utilize the <kbd>`$answer`</kbd> event to catch this response and initiate corresponding actions.

{% hint style="danger" %}
Responses may be triggered multiple times if there are reroutes within the conversation flow. It's crucial to carefully manage how responses are linked within the platform to ensure that the same event isn't triggered multiple times.
{% endhint %}

```html
<!DOCTYPE html>
<html>
<head>
    <style>
    #modal {
        ...
        display: none;
    }
    </style>
</head>
<body>
    <div id="modal">...</div>
    <script>
    document.addEventListener("indigo-ai-widget-loaded", function (event) {
        event.detail.widget.on("$answer", (data) => {
            // If the answer is 'registration'
            if (data.intent == "registrazione") {
                // Show the modal
                document.getElementById("modal").style.display = "block";
            }
        });
    });
    </script>
    <script src="https://platform.indigo.ai/widget.js?token={{PROJECT_TOKEN}}&v=3"></script>
</body>
</html>
```

### Google Analytics

A common setup involves linking Google Analytics to track when the chat opens. \
Here's how you can structure the widget installation for this purpose:

```html
<!-- Step 1: Set a custom userRef before loading the widget.
     This value allows you to associate your own user identifier with Indigo.ai's system,
     enabling you to query conversations and messages using your custom ID.
     Replace 'custom_user_ref' with your actual unique user identifier. -->
<script type="text/javascript">
  window.localStorage.setItem('indigo-ai-widget-uid', 'custom_user_ref');
</script>

<!-- Step 2: Include the Indigo.ai widget.
     Make sure to replace {{TOKEN}} with your actual API token.
     The "defer" attribute ensures that the script is executed after the HTML is parsed. -->
<script defer src="https://platform.indigo.ai/widget.js?token={{TOKEN}}&v=3"></script>

<!-- Step 3: Listen for the widget's load event and track the first time the widget is opened.
     Wrap your interactions with the widget inside the "indigo-ai-widget-loaded" event listener
     to ensure that the IndigoAIChat object is available. -->
<script type="text/javascript">
  document.addEventListener('indigo-ai-widget-loaded', function (event) {
    // In this example, we track an action only when the widget is opened for the first time.
    let isFirstOpen = true;

    event.detail.widget.on('open', function () {
      // Ensure that the tracking code runs only once, on the very first open.
      if (!isFirstOpen) return;
      isFirstOpen = false;

      // Insert your Google Analytics tracking code here.
      // For example, you could use:
      // ga('send', 'event', 'Chatbot', 'open', 'Widget First Open');
      // or any other Google Analytics API call that suits your needs.
    });
  });
</script>
```
