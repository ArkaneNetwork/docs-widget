---
description: Fetch non-fungible items by wallet ID
---

# getNonfungibles

This function returns the non-fungible \(ERC721, ERC1155\) items for a given wallet

```javascript
arkaneConnect.api.getNonfungibles("d91b644a-076f-44bf-ae90-29251df19784");
```

## Signature

```javascript
getNonfungibles = (walletId: string): Promise<NFT[]>
```

## Returns

```javascript
Promise<NFT[]>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `walletId` | `True` | Wallet ID of the wallet you want to fetch the balance of |

## Example

```javascript
arkaneConnect.api.getNonfungibles("d91b644a-076f-44bf-ae90-29251df19784");
```

## Object Types

{% page-ref page="../object-type-reference/nft.md" %}





