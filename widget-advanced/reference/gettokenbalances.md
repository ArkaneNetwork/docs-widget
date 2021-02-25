---
description: Fetch the token balances (ERC20 standard) for a specific wallet
---

# getTokenBalances

This function returns the balance of all tokens currently supported by Arkane. The list of supported tokens can be found on [Github](https://github.com/ArkaneNetwork/content-management/tree/master/tokens). Tokens need to be based on the ERC20 standard, this included for example ERC20, VIP180, TRC20, ...

```javascript
arkaneConnect.api.getTokenBalances("d91b644a-076f-44bf-ae90-29251df19784");
```

{% hint style="info" %}
🧙 To add support in Arkane for a certain token, simply submit a [pull request](https://github.com/ArkaneNetwork/content-management/tree/master/tokens).
{% endhint %}

## Signature

```javascript
arkaneConnect.api.getTokenBalances(walletId: string): Promise<TokenBalance[]>
```

## Returns

```javascript
Promise<TokenBalance[]>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `walletId` | `True` | Wallet ID of the wallet you want to fetch the balance of |

## Example

```javascript
arkaneConnect.api.getTokenBalances("d91b644a-076f-44bf-ae90-29251df19784");
```

## Object Types

{% page-ref page="../object-type-reference/tokenbalance.md" %}



