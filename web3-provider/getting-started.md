---
description: "Already have support for Web3? GREAT \U0001F389, this is the place to start."
---

# Getting Started

If you already support Web3-technology, you can improve the UX within your application by integrating the Arkane Web3 provider, a smart wrapper around the existing Web3 Ethereum JavaScript API.

By making use of our Web3 provider you are able to leverage the full potential of Arkane with minimal effort and you will be able to onboard users that are less tech-savvy without making them leave your application or download third-party plugins. Integrating just takes 2 steps and 5 minutes.

#### Don't support Web3 yet? 

Don't worry we've got you covered with our 📦 [Widget - Arkane Connect](../widget/introduction.md).

## Step 1: Add the library to your project 

Install the library by downloading it to your project via NPM

```text
npm i @arkane-network/web3-arkane-provider
```

followed by adding the script to the head of your page.

```text
<script src="/node_modules/@arkane-network/web3-arkane-provider/dist/web3-arkane-provider.js"></script>
```

After adding the javascript file to your page, a global **Arkane** object is added to your window. This object is the gateway for creating the web3 wrapper and fully integrates the [widget - Arkane Connect](../widget/introduction.md).

## Step 2: Initialize **the web3 provider**

Add the following lines of code to your project, it will load the Arkane web3 provider.

{% tabs %}
{% tab title="Simple" %}
```javascript
Arkane.createArkaneProviderEngine({clientId: 'Arketype'}).then(provider => {
    web3 = new Web3(provider);
});
```
{% endtab %}

{% tab title="Advanced" %}
```javascript
const options = {
  clientId: 'Arketype',
  rpcUrl: 'https://kovan.infura.io/v3/YOUR-PROJECT-ID', //optional
  environment: 'staging', //optional, production by default
  signMethod: 'POPUP', //optional, REDIRECT by default
  bearerTokenProvider: () => 'obtained_bearer_token', //optional, default undefined
  //optional: you can set an identity provider to be used when authenticating
  authenticationOptions: {
    idpHint: 'google'
  },
  secretType: 'ETHEREUM' //optional, ETHEREUM by default
};
Arkane.createArkaneProviderEngine(options).then(provider => {
    web3 = new Web3(provider);
});
```
{% endtab %}
{% endtabs %}

The web3 instance now works as if it was [injected by parity or metamask](https://github.com/ethereum/wiki/wiki/JavaScript-API). You can fetch wallets, sign transactions, and messages.

## Congratulations, your dapp now supports Arkane 🎉

{% hint style="info" %}
🧙 To connect to our production environment and mainnet, you will need to [register your app](https://arkane-network.typeform.com/to/hzbcGJ) and request your [Client ID](../deep-dive/authentication.md#client-id).
{% endhint %}

{% hint style="warning" %}
If you want to use the [web3js event emitter](https://web3js.readthedocs.io/en/v1.3.0/web3-eth-subscribe.html#subscribe-newblockheaders), please use version &gt;= 1.3.0 of [web3js](https://www.npmjs.com/package/web3).
{% endhint %}

## Object Types

{% page-ref page="../widget-advanced/object-type-reference/arkanesubprovideroptions.md" %}

{% page-ref page="../widget-advanced/object-type-reference/secrettype.md" %}



