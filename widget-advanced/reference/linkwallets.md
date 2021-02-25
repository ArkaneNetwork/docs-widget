---
description: Link a user wallet to your application
---

# linkWallets

This function will allow users to link their existing wallets with your application. 

```javascript
arkaneConnect.flows.linkWallets();
```

The difference with [`manageWallets`](managewallets.md):

* A user can only link wallets, it is not possible to create or import a wallet
* A list of all wallets is returned for any chain \(it is possible to filter this\).

**Use case:** a portfolio app where a user wants to quickly link all his wallets to get an overview of his complete portfolio.

## Signature

```javascript
arkaneConnect.flows.linkWallets(options?: {
    redirectUri?: string,
    correlationID?: string
}): Promise<PopupResult | void>
```

## Returns

```javascript
Promise<PopupResult | void>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `options` | `False` | Options you want to provide |
| `options.redirectUri` | `False` | URI you want users to be redirected to after linking their wallets. Defaults to current URI. |
| `options.correlationID` | `False` | Unique correlationID allowing you to identify this specific transaction. It will be appended as a request parameter to the `redirectUri` upon return. |

## Example

```javascript
// redirects the user to the link wallets screen
// + redirects the user to https://arkane.network once he's done
// + appends the correlationID as a request parameter when being redirected back
arkaneConnect.flows.linkWallets({
    redirectUri: 'https://arkane.network',
    correlationID: 'f173a18d-7a75-4429-9df4-25153d64a921'
});
```

## Object Types

{% page-ref page="../object-type-reference/popupresult.md" %}

