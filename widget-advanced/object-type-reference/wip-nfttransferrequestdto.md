---
description: Data structure for performing a non-fungible token transfer
---

# NftTransferRequestDto

## Signature

```javascript
{
  walletId! : string;
  to! : string;
  secretType! : SecretType;
  tokenAddress!: string;
  tokenId!: number;
  network?: {
    name!: string;
    nodeUrl!: string,
    chainId?: number;
  };
  data? : string;
  value! : BigDecimal;
}
```

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `walletId` | `True` | `String` | ID of the wallet one wants to sign with. |
| `to` | `True` | `String` | Destination address of the transaction. Can be an address or an email address. |
| `secretType` | `True` | [`SecretType`](secrettype.md) | Chain the transaction will be executed on. |
| `tokenAddress` | `True` | `String` | Address of the token |
| `tokenId` | `True` | `Number` | ID of the non-fungible token or ERC20 token inside ERC1155 |
| `network` | `False` | `Object` | The [network](../../deep-dive/environments.md) to submit the transaction to |
| `network.name` | `True` | `String` | Display name of the network to submit the transaction to \(e.g.: "Rinkeby"\). This will be shown to the user when signing the transaction |
| `network.nodeUrl` | `True` | `String` | URL of the node to submit the transaction to \(e.g.: "https://rinkeby.infura.io"\) |
| `network.chainId` | `False` | `Number` | Network ID of the selected network |
| `data` | `False` | `String` | Data you want to send. This field will be ignored when building a token transaction request |
| `value` | `True` | `Number` | Token value that should be transferred. |

{% hint style="info" %}
🧙 Using the `network` parameter, the node to which the transaction is sent can be set manually. It allows you to submit a transaction to any mainnet or testnet node of your choosing, public or private. \( Ethereum only\)
{% endhint %}

## Example

```javascript
{
  "walletId" : "adc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
  "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
  "secretType" : "VECHAIN",
  "network" : {
    "name" : "Rinkeby",
    "nodeUrl" : "https://rinkeby.arkane.network",
    "chainId" : null
  },
  "tokenAddress" : "0x4df47b4969b2911c966506e3592c41389493953b",
  "from" : "0x89e01cEC55D718fA1Bf6B00fF21e6707cd9A3067",
  "tokenId" : 1
}
```

## Function Types

{% page-ref page="../reference/executenfttransfer.md" %}



