---
description: Data structure for performing a gas transfer
---

# GasTransferRequestDto

## Signature

```javascript
{
  walletId! : string;
  to! : string;
  secretType! : SecretType;
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
| `network` | `False` | `Object` | The [network](../../deep-dive/environments.md) to submit the transaction to |
| `network.name` | `True` | `String` | Display name of the network to submit the transaction to \(e.g.: "Rinkeby"\). This will be shown to the user when signing the transaction |
| `network.nodeUrl` | `True` | `String` | URL of the node to submit the transaction to \(e.g.: "https://rinkeby.infura.io"\) |
| `network.chainId` | `False` | `Number` | Network ID of the selected network |
| `data` | `False` | `String` | Data you want to send. This field will be ignored when building a token transaction request |
| `value` | `True` | `Number` | Token value that should be transferred. |

{% hint style="info" %}
🧙 You don’t have to take into account the number of decimals for different tokens, Arkane handles that for you.

**Example:** If a token has 18 decimals and you want to transfer 1 token, provide the value 1. Arkane will translate this to the correct nondecimal value \(1 \* 10e18\). 
{% endhint %}

{% hint style="info" %}
🧙 Using the `network` parameter, the node to which the transaction is sent can be set manually. It allows you to submit a transaction to any mainnet or testnet node of your choosing, public or private. \( Ethereum only\)
{% endhint %}

## Example

```javascript
{
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    value: 81,
    secretType: 'ETHEREUM',
}
```

## Function Types

{% page-ref page="../reference/executegastransfer.md" %}

