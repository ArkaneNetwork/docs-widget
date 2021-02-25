---
description: Fetch a specific wallet
---

# getWallet

This function returns the details for a specific wallet \(native balance is also included\)

```javascript
arkaneConnect.api.getWallet("d91b644a-076f-44bf-ae90-29251df19784")
```

## Signature

```javascript
arkaneConnect.api.getWallet(walletId: string): Promise<Wallet>
```

## Returns

```javascript
Promise<Wallet>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `walletId` | `True` | Wallet ID of the wallet you want to fetch |

## Example

```javascript
arkaneConnect.api.getWallet("d91b644a-076f-44bf-ae90-29251df19784");
```

## Object Types

{% page-ref page="../object-type-reference/wallet.md" %}

