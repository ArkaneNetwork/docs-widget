---
description: How to retrieve non-fungible tokens for a wallet.
---

# Retrieve non-fungible tokens

To fetch the non-fungible tokens for a certain wallet, you need to call the function [`getNonfungibles`](../widget-advanced/reference/getnonfungibles.md) , to get all non-fungibles in all the wallets that a user has connected to your application use [`getAllNonfungibles`](../widget-advanced/reference/getallnonfungibles.md).

## By wallet ID

###  Function

```javascript
arkaneConnect.api.getNonfungibles(walletId: string);
```

### Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.api.getNonfungibles("c8ec9954-fa1a-4682-9cf8-ef5c1015d1d1").then((items) => {
 console.log("Your items: ", items);
})
```

### Returns

```javascript
[
  {
    id: "2",
    tokenId: "2",
    description: "Spells of Genesis card",
    imagePreviewUrl: "http://metadata.spellsofgenesis.com/asset/image/320/FOOTSOLDIER.png",
    imageThumbnailUrl: "http://metadata.spellsofgenesis.com/asset/image/320/FOOTSOLDIER.png",
    imageUrl: "http://metadata.spellsofgenesis.com/asset/image/320/FOOTSOLDIER.png",
    name: "Reckless Footsoldier",
    url: "https://www.spellsofgenesis.com/2",
    animationUrl: null,
    attributes: [
      {
        displayType: null,
        maxValue: null,
        traitCount: null,
        traitType: "Name",
        value: "Reckless Footsoldier"
      },
      {
        displayType: null,
        maxValue: null,
        traitCount: null,
        traitType: "Rarity",
        value: "Not Assigned"
      },
      {
        displayType: null,
        maxValue: null,
        traitCount: null,
        traitType: "Attack",
        value: "4"
      },
      {
        displayType: null,
        maxValue: null,
        traitCount: null,
        traitType: "Health",
        value: "8"
      },
      {
        displayType: null,
        maxValue: null,
        traitCount: null,
        traitType: "Speed",
        value: "3"
      }
    ],
    backgroundColor: null,
    contract: {
      address: "0x030bf504a4abeb05b91196536565c7acee9d9f02",
      description: null,
      imageUrl: null,
      media: null,
      name: "Spells of Genesis Askian Card",
      symbol: "SOG",
      type: "ERC_721",
      url: null
    }
  }
]
```

## By wallet Address

###  Function

```javascript
arkaneConnect.api.getNonfungiblesByAddress(secretType: SecretType, walletAddress: string);
```

### Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.api.getNonfungiblesByAddress("MATIC","0x10BCdb57aEbE5b195B750CCd4F506783aF0B52Cf").then((items) => {
 console.log("Your items: ", items);
})
```

## All

Call that returns all non-fungibles for the user for all wallets that are connected to your application. Optional filter to filter based on secret type.

### Function

```javascript
arkaneConnect.api.getAllNonfungibles(secretTypes?: SecretType[]);
```

### Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.api.getAllNonfungibles().then((items) => {
 console.log("Your items: ", items);
})
```

### Returns

```javascript
[{
  items: [{
  animationUrl: null,
  attributes: [{
  displayType: null,
  maxValue: null,
  traitCount: null,
  traitType: "Name",
  value: "Reckless Footsoldier"
}, {
  displayType: null,
  maxValue: null,
  traitCount: null,
  traitType: "Rarity",
  value: "Not Assigned"
}, {
  displayType: null,
  maxValue: null,
  traitCount: null,
  traitType: "Attack",
  value: "4"
}, {
  displayType: null,
  maxValue: null,
  traitCount: null,
  traitType: "Health",
  value: "8"
}, {
  displayType: null,
  maxValue: null,
  traitCount: null,
  traitType: "Speed",
  value: "3"
}],
  backgroundColor: null,
  contract: {
    address: "0x030bf504a4abeb05b91196536565c7acee9d9f02",
    description: null,
    imageUrl: null,
    media: null,
    name: "Spells of Genesis Askian Card",
    symbol: "SOG",
    type: "ERC_721",
    url: null
  },
  description: "Spells of Genesis card",
  id: "2",
  imagePreviewUrl: "http://metadata.spellsofgenesis.com/asset/image/320/FOOTSOLDIER.png",
  imageThumbnailUrl: "http://metadata.spellsofgenesis.com/asset/image/320/FOOTSOLDIER.png",
  imageUrl: "http://metadata.spellsofgenesis.com/asset/image/320/FOOTSOLDIER.png",
  name: "Reckless Footsoldier",
  tokenId: "2",
  url: "https://www.spellsofgenesis.com/2"
}, {
  animationUrl: null,
  attributes: [],
  backgroundColor: null,
  contract: {
    address: "0x038d63df99a46b82796b2ea5d9cabc50340fd69f",
    description: null,
    imageUrl: null,
    media: null,
    name: "PUNK ARK GALLERY",
    symbol: "PARKG",
    type: "ERC_721",
    url: null
  },
  description: "test",
  id: "150865",
  imagePreviewUrl: "http://cryptopunk-dev.ark.gallery:8080/ipfs/QmZfzbs97QVtiFmV77QsR3dE2JjGqsXK2DGvCdkSMNJ6fG",
  imageThumbnailUrl: "http://cryptopunk-dev.ark.gallery:8080/ipfs/QmZfzbs97QVtiFmV77QsR3dE2JjGqsXK2DGvCdkSMNJ6fG",
  imageUrl: "http://cryptopunk-dev.ark.gallery:8080/ipfs/QmZfzbs97QVtiFmV77QsR3dE2JjGqsXK2DGvCdkSMNJ6fG",
  name: "test gif big file",
  tokenId: "150865",
  url: null
}],
  secretType: "ETHEREUM",
  walletAddress: "0x0288E3dDBe9e4f2B0536665f55464187601b41c4",
  walletId: "eeb52670-4fb7-4e79-830d-4f5f613f315b",
  walletType: "THREEWAY_SHARED"
}]
```

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function, you can find the signature, its parameters, and possible options documented.

{% page-ref page="../widget-advanced/reference/getnonfungibles.md" %}

{% page-ref page="../widget-advanced/reference/getallnonfungibles.md" %}



