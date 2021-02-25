---
description: Type of Authentication
---

# Authentication

Authenticating to Arkane is done using [OpenID Connect](https://openid.net/connect/), which combines the OAuth 2.0 protocol together with a simple identity layer. We use OpenID Connect's [Authorization Code Flow](https://openid.net/specs/openid-connect-core-1_0.html#CodeFlowAuth) for our authentication and authorization.

{% hint style="info" %}
🧙 An application requires a specific [Client ID](https://arkane-network.typeform.com/to/hzbcGJ) to connect to our [environments](environments.md). This not only improves security but also allows custom branding.
{% endhint %}

## Authentication code

If you provide your own implementation of `bearerTokenProvider`, the web3 provider will not attempt to obtain an authentication code, but rather use the one provided by you.

## Client ID

In order to communicate with Arkane, a Client ID is required. To connect to our [staging environment](environments.md#staging) and use the testnets, we provide a public Client ID **`Arketype`** which is **free to use and available to anyone**.  

{% hint style="warning" %}
The Client ID **`Arketype`** only accepts requests from the following domains:

* http://localhost:\*
* http://127.0.0.1:\*

When you require access through your personal domain then please request a private Client ID by [registering your app](https://arkane-network.typeform.com/to/hzbcGJ).
{% endhint %}

To connect to our [production environment](environments.md#production) and the different mainnets, a private Client ID is required. By using a Client ID that is linked to your application, an extra level of security is added, as it allows transaction filtering based on domain. It also allows for custom branding of the [Widget](../widget/introduction.md).

{% hint style="info" %}
🧙 To connect to our production environment and mainnet, you will need to [register your app](https://arkane-network.typeform.com/to/hzbcGJ) to get a Client ID. 
{% endhint %}

