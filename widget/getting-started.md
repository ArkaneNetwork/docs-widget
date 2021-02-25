---
description: >-
  Getting started with Arkane Connect, our JavaScript Widget for easy
  integration.
---

# Initializing the widget

## Step 1: Including the widget

Arkane Connect has been published to [npmjs.com](https://www.npmjs.com/package/@arkane-network/arkane-connect). So by using npm, you can fetch it by executing the following:

```text
npm i @arkane-network/arkane-connect
```

You can also download it directly via [UNPKG CDN](https://unpkg.com/@arkane-network/arkane-connect).

{% hint style="info" %}
🧙 It is best to point Arkane Connect to a specific version when including its URL in your code. See [https://unpkg.com/](https://unpkg.com/) for more info.
{% endhint %}

## Step 2: Initializing the widget, with Arkane Connect

Create an ArkaneConnect instance with your [Client ID](https://arkane-network.typeform.com/to/hzbcGJ) with the following script. Your Arkane [Client ID](https://arkane-network.typeform.com/to/hzbcGJ) is required when calling this function, as it identifies your app to Arkane.

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
```

{% hint style="info" %}
🧙 You need to [register your app](https://arkane-network.typeform.com/to/hzbcGJ) to get your private [Client ID](../deep-dive/authentication.md#client-id)
{% endhint %}

The ArkaneConnect object is your entry point to the rest of the widget functionalities, below is its signature. You can connect to [several networks and environments](../deep-dive/environments.md) by using the [`ConstructorOption`](../widget-advanced/object-type-reference/constructoroptions.md) '**Environment**'. 

```javascript
//Signature ArkaneConnect
ArkaneConnect(clientID:string, options?: ConstructorOptions)
```

### Congratulations, your app is now blockchain-enabled! 🎉

After putting the 2 code snippets above into the editor, your app is now blockchain-enabled! 

