# Single Sign-On (SSO) & Multi-Factor Authentication (MFA)

Robust security is crucial for protecting your data and ensuring seamless user access. That's why we’ve integrated Single Sign-On (SSO) and Multi-Factor Authentication (MFA) into our platform. These two features work together to provide a **more secure, efficient, and user-friendly authentication experience for both admins and end-users**.

Here's how each feature works and the benefits they bring to your organization:

## 1. Single Sign-On (SSO): Simplifying Access Across Multiple Platforms

Single Sign-On (SSO) is a technology that allows users to access multiple applications or services with a single authentication, eliminating the need to remember multiple usernames and passwords. At indigo.ai, SSO enhances user convenience and security in two key ways:

### Platform SSO

With Platform SSO, users can **log in to the indigo.ai platform with a single click**, eliminating the need to enter credentials every time they access the platform. This is made possible through secure authentication methods, including Google accounts and company-specific logins via SAML.&#x20;

* **Benefit**: Users no longer need to input login credentials repeatedly, streamlining the login process while maintaining secure access to the platform.

### Chat SSO Authentication Integration

In addition to the platform SSO, we’ve integrated **Chat SSO Auth for channels where the indigo.ai agents are installed**.&#x20;

This feature **authenticates users directly within the chat, recognizing their identity based on the main platform login** and removing the need for them to enter credentials again.

* **Use Case**: A client with a restricted area wants users to access the chat without needing to re-authenticate. With Chat SSO, once the user logs into the restricted area, they can seamlessly interact with the bot in the chat without additional logins.
* **How It Works**:
  1. The user logs into a secure, restricted area with their credentials.
  2. The authentication session is used to log them into the chat automatically.
  3. The chat system recognizes the user, personalizes the experience, and allows interaction without further authentication.

{% hint style="info" %}
If you'd like to enable **Platform SSO** or **Chat SSO**, [reach out to us](../../need-help/our-customer-success-team.md).&#x20;
{% endhint %}

## 2. Multi-Factor Authentication (MFA): Strengthening Security with an Extra Layer

While SSO provides a convenient way to access multiple systems, Multi-Factor Authentication (MFA) **ensures that access is secure by requiring multiple forms of verification**.&#x20;

With MFA, users must provide more than just a password to access their accounts. This adds an **additional layer of security** to prevent unauthorized access, even if login credentials are compromised.

<figure><img src="../../.gitbook/assets/Screenshot 2025-03-27 alle 11.14.58.png" alt="" width="375"><figcaption></figcaption></figure>

**How MFA Works**

When logging into Indigo.ai, users will first enter their password, then receive a verification code via their phone or email. This code must be entered to complete the login process, providing an added layer of protection.

{% hint style="info" %}
For details on how to enable Multi-Factor Authentication (MFA), check out this page: [settings](../workspace/settings/ "mention").
{% endhint %}

**Advanced Security Features**

In addition to traditional login methods, MFA allows businesses to monitor and manage devices connected to accounts. This means you can view the devices used for logins and take action if something seems suspicious, such as blocking a device that shouldn't be accessing the platform.
