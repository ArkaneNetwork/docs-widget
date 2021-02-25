---
description: >-
  During initialization, you can define several options, such as which
  environment you would like to connect to, as well as define the way you would
  like to interact with the widget.
---

# Initializing options

```javascript
// use staging environment
// + sign transactions using the REDIRECT method
// + authentication using bearerTokenProvider supplied by the client
const arkaneConnect = new ArkaneConnect('Arketype', { environment: 'staging',
                                                      windowMode: 'REDIRECT',
                                                      bearerTokenProvider: () => auth.token});
```

## Signature

```javascript
ArkaneConnect(clientID:string, options?: ConstructorOptions)
```

## Parameters

| Parameter | Required | Description | Example |
| :--- | :--- | :--- | :--- |
| `clientID` | `true` | Client ID \(case sensitive\) | `'Arketype'` |
| `options` | `false` | [`ConstructorOptions`](object-type-reference/constructoroptions.md) | `{ windowMode: 'REDIRECT' }` |

## Object Types

{% page-ref page="object-type-reference/constructoroptions.md" %}

{% page-ref page="object-type-reference/windowmode.md" %}

{% page-ref page="object-type-reference/popupoptions.md" %}

