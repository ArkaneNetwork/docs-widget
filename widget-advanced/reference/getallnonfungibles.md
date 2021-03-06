---
description: Fetch all non-fungible items
---

# getAllNonFungibles

This function returns all non-fungible items for a user \(of all linked wallets\) that can be filtered based on secretType \(optional\)

```javascript
arkaneConnect.api.getAllNonfungibles();
```

## Signature

```javascript
getAllNonfungibles = (secretTypes?: SecretType[]): Promise<WalletItems[]>
```

##  Returns

```javascript
Promise<WalletItems[]>
```



## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `secretTypes` | `False` | An optional list of [`secretTypes`](../object-type-reference/secrettype.md) for which you want to filter |

## Object Types

{% page-ref page="../object-type-reference/walletitems.md" %}

