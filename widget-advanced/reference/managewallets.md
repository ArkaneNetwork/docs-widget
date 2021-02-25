---
description: Manage a user's wallets for a specific application
---

# manageWallets

This function will allow users to manage the wallets they use within your application. 

```javascript
arkaneConnect.flows.manageWallets('ETHEREUM');
```

As an application, it is possible to have a user manage his wallets for a specific chain. During this action, the user can link existing wallets or import a wallet. When the user returns to the app, a wallet of a specific chain will be linked to the application. When a user does not have any wallets yet, a user can indicate to create a new wallet.

## Signature

```javascript
arkaneConnect.flows.manageWallets(
    chain: string,
    options?: {
        redirectUri?: string,
        correlationID?: string
    }
): Promise<PopupResult | void>
```

## Returns

```javascript
Promise<PopupResult | void>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `chain` | `True` | The chain for which your user wants to manage his wallets. Same as [`SecretType`](../object-type-reference/secrettype.md). |
| `options` | `False` | Add options. |
| `options.redirectUri` | `False` | URI you want users to be redirected to after linking their wallets. Defaults to current URI. |
| `options.correlationID` | `False` | Unique correlationID allowing you to identify this specific transaction. It will be appended as a request parameter to the `redirectUri` upon return. |

## Example

```javascript
// redirects the user to the manage wallets screen for his Ethereum wallets
// + redirects the user to https://arkane.network once he's done
// + appends the correlationID as a request parameter when being redirected back
arkaneConnect.manageWallets(
    'ETHEREUM',
    {
        redirectUri: 'https://arkane.network',
        correlationID: 'f173a18d-7a75-4429-9df4-25153d64a921'
    }
);
```

## Object Types

{% page-ref page="../object-type-reference/popupresult.md" %}



