---
description: This page describes an NFT
---

# NFT

## Signature

```javascript
{
    id: string;
    tokenId?: string;
    name?: string;
    description?: string;
    url?: string;
    backgroundColor?: string;
    imageUrl?: string;
    imagePreviewUrl?: string;
    imageThumbnailUrl?: string;
    attributes?: Trait[];
    contract: NFTContract;
}
```

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `id` | `True` | `String` | ID of the token |
| `tokenId` | `False` | `String` | Same as ID |
| `name` | `True` | `String` | Name of the token |
| `description` | `False` | `String` | Description of the token |
| `url` | `False` | `String` | The \(external\) URL that refers to the token \(ex. the website of the application\) |
| `backgroundColor` | `False` | `String` | The background color to be used when displaying the item |
| `imageUrl` | `False` | `String` | The image of the token \(full res\) |
| `imagePrevieweUrl` | `False` | `String` | The image of the token to be used when previewing |
| `imageThumbnailUrl` | `False` | `String` | The image of the token to be used when showed in an overview \(thumbnails\) |
| `attributes` | `False` | `Trait` | Show the attributes/properties of this token |
| `contract` | `True` | `NFTContract` | Details about the contract that this contract belongs to |

## Function Reference

{% page-ref page="../reference/getnonfungibles.md" %}



