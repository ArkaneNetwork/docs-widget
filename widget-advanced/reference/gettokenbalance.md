---
description: Fetch the balance of a specific token (ERC20 standard) on a specific wallet
---

# getTokenBalance

This function returns the token balance for a specified token. Token needs to be based on the ERC20 standard, this included for example ERC20, VIP180, TRC20, ...

```javascript
arkaneConnect.api.getTokenBalance("d91b644a-076f-44bf-ae90-29251df19784", "0xB8c77482e45F1F44dE1745F52C74426C631bDD52");
```

## Signature

```javascript
arkaneConnect.api.getTokenBalance(walletId: string, tokenAddress: string): Promise<TokenBalance>
```

## Returns

```javascript
Promise<TokenBalance>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `walletId` | `True` | Wallet ID of the wallet you want to fetch the balance of |
| `tokenAddress` | `True` | Address of the token contract |

## Example

```javascript
arkaneConnect.api.getTokenBalance("d91b644a-076f-44bf-ae90-29251df19784", "0xB8c77482e45F1F44dE1745F52C74426C631bDD52");
```

## Object Types

{% page-ref page="../object-type-reference/tokenbalance.md" %}





