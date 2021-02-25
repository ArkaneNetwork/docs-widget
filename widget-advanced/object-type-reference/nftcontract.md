---
description: This object describes the properties of an NFT contract
---

# NFTContract

## Signature

```javascript
{
    name?: string;
    description?: string;
    address: string;
    symbol?: string;
    url?: string;
    imageUrl?: string;
    type?: string;
    media?: string;
}
```

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `name` | `False` | `String` | The name of the contract / application |
| `description` | `False` | `String` | The description of the contract / application |
| `address` | `True` | `String` | The contract address \(on the blockchain\) |
| `symbol` | `False` | `String` | Symbol of the contract |
| `url` | `False` | `String` | The \(external\) URL of the contract / application |
| `imageUrl` | `False` | `String` | The image of the contract / application |
| `type` | `False` | `String` | The type of the contract, ex. ERC721/ERC1155 |
| `media` | `False` | `String` | Media associated with this contract, ex. a youtube video |

## Function Reference

{% page-ref page="../reference/getnonfungibles.md" %}



