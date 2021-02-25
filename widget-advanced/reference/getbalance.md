---
description: Fetch the native balance of a wallet
---

# getBalance

This function returns  all the wallets for the specified user \(bearer token\)

```javascript
arkaneConnect.api.getBalance("d91b644a-076f-44bf-ae90-29251df19784");
```

## Signature

```javascript
arkaneConnect.api.getBalance(walletId: string): Promise<WalletBalance>
```

## Returns

```javascript
Promise<WalletBalance>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| \`\`[`walletId`](../object-type-reference/wallet.md#parameters)\`\` | `True` | Wallet ID of the wallet you want to fetch the balance of |

## Example

```javascript
arkaneConnect.api.getBalance("d91b644a-076f-44bf-ae90-29251df19784");
```

## Object Types

{% page-ref page="../object-type-reference/walletbalance.md" %}

