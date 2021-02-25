---
description: Fetch non-fungible items by wallet address
---

# getNonfungiblesByAddress

This function returns the non-fungible \(ERC721, ERC1155\) items for a given wallet

```javascript
arkaneConnect.api.getNonfungiblesByAddress("ETHEREUM","0x3ad396dcb86d3a72855f7e1e305eaa144ec9b434");
```

## Signature

```javascript
getNonfungiblesByAddress = (secretType: SecretType, walletAddress: string): Promise<NFT[]>
```

## Returns

```javascript
Promise<NFT[]>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `walletAddress` | `True` | Wallet address the wallet you want to fetch the balance of |
| [`secretType`](../object-type-reference/secrettype.md)\`\` | `True` | The relevant blockchain \(e.g Ethereum, Matic,..\) |

## Example

```javascript
arkaneConnect.api.getNonfungiblesByAddress("ETHEREUM","0x3ad396dcb86d3a72855f7e1e305eaa144ec9b434");
```

## Object Types

{% page-ref page="../object-type-reference/nft.md" %}

{% page-ref page="../object-type-reference/secrettype.md" %}





