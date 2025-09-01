# Secrets Management: Protecting Your Sensitive Information

Managing sensitive information like **API tokens**, **authentication keys**, and other **credentials** is crucial.

That's why we’ve introduced **Secrets Management**—a feature that securely stores sensitive information within the platform while ensuring it’s never exposed in an unprotected format.

{% embed url="https://screen.studio/share/k6QB63up?_loop=1&autoplay=1" %}

## Key Benefits

Without a secure system in place to manage sensitive information, organizations often struggle to protect critical data like API authorization tokens. When these tokens are exposed in the front-end or stored insecurely, they become vulnerable to compromise, creating a significant security risk.&#x20;

Secrets Management ensures that **sensitive data remains encrypted, securely stored, and only accessible by authorized systems or users**, mitigating the potential for data breaches and unauthorized access.

Secrets Management offers:&#x20;

* **Improved Security**: By storing tokens and sensitive credentials securely, we reduce the risk of unauthorized access and data breaches.
* **Ease of Management**: The system simplifies the process of handling, updating, and managing secrets, making it easier for admins and owners to control sensitive data.
* **Visibility Control**: Secrets are only visible to authorized users, ensuring that sensitive data remains hidden from those who shouldn’t have access.
* **Better Security Compliance**: Ensures that sensitive information is handled according to industry-standard security practices.

## How It Works

Secrets management allows you to **create** **encrypted** **secret variables** that are securely stored within your workspace. These secrets are only accessible during specific API calls and cannot be viewed by users or logged in plain text.

For example, rather than storing an integration token for services like Zendesk directly in a workflow, you can now store it as a secret. This ensures the token is protected and remains hidden from unauthorized users, while still enabling you to use it within your API calls.

### **Creating a Secret**

The Secrets Creation and Management feature is integrated into the platform’s [**Variables**](../blocks-and-variables/variables/) **Management Panel**, where it functions as a special type of variable designed to be more secure. Here’s how it works:

* **Admin/Owner Role**: Only users with an Admin or Owner role can create, edit, or delete secrets.
* **Editor Role**: Editors can view secrets but cannot create or edit them.

Admins and Owners can create new secrets by clicking on the “Create New” button. A side panel will open where they can input the following information:

* **Secret Name**: A unique identifier for the secret. This is mandatory and cannot be edited once created.
* **Visibility**: The secret’s visibility can be set to either **masked** (where users can temporarily view the value by clicking an eye icon) or **restricted** (where the value is hidden entirely).

Once created, the value of the secret will be obfuscated (replaced with dots), ensuring it cannot be copied, pasted, or exposed in the platform.

### Using Secrets in API Calls

The use of secrets within the platform is exclusively limited to the [**API Block**](../blocks-and-variables/action-blocks/api-block.md).&#x20;

You can add secrets to your API calls, making it easy to securely pass authentication tokens or other sensitive data within requests. Here’s how it works:

* **Add Secret to API Call**: When configuring an API call, you can choose to add a secret by selecting it from a dropdown menu. This dropdown allows you to search for existing secrets, create new ones, or edit the values of existing secrets.
* **Single Secret per Field**: Each API call can only have one secret at a time in the specified field. If you need to use a different secret, simply click “Add Secret” again to replace the current value.

### Managing Existing Secrets

When managing an existing secret, users will be able to see the secret’s value in its masked or restricted state, but the **visibility setting cannot be changed after creation**. Admins and owners can also update or delete secrets as needed, ensuring full control over the lifecycle of sensitive data.

Upon deletion of a secret, a confirmation modal will appear to ensure the secret is being removed intentionally.
