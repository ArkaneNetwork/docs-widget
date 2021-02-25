---
description: 'Authenticate, and get the wallets of a user for a specific chain.'
---

# getAccount

This function will return the wallets of a user for a specific chain and if needed authenticate the user and create a wallet. 

```javascript
arkaneConnect.flows.getAccount('ETHEREUM');
```

This function will trigger a flow of events in order to return a certain state. In this case, fetch the wallets of a user for a specific chain.

## Flow sequence

### Step 1: Authenticate

Verify is a user is logged in if so the flow continues, otherwise the user will be prompted to log in or create a new account.

### Step 2: Fetch wallets

Retrieve the wallets linked to the applications Client ID for a certain chain. When no wallets have been linked, prompt the user to link a wallet with the application. If the user doesn't possess a wallet on the required chain a new wallet will be created and immediately linked to the application. 

### Step 3: Resolving the promise

When the necessary checks have been fulfilled, the promise is resolved. If all checks passed the user will not receive a pop-up.

## Signature

```javascript
arkaneConnect.flows.getAccount(chain: SecretType): Promise<Account>
```

## Returns

```javascript
Promise<Account>
```

## Parameters

| Parameter | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `chain` | [`SecretType`](../object-type-reference/secrettype.md) | The requested chain of which it will return a user's wallets. | `ETHEREUM` |

## Example

```javascript
// Authenticate, and get the ethereum wallets of current user.
arkaneConnect.flows.getAccount('ETHEREUM').then((account: Account) => {
    if(account.isAuthenticated) {
        console.log('wallets', account.wallets);
        console.log('name', account.auth.tokenParsed.name);
    }
}).catch((e) => {
    console.log('user closed window, or an error occurred', e);
});
```

## Object Types

{% page-ref page="../object-type-reference/account.md" %}

{% page-ref page="../object-type-reference/wallet.md" %}

