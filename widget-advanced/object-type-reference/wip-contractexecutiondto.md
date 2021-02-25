---
description: Data structure for performing a contract call on a blockchain
---

# ContractExecutionDto

## Signature

```javascript
{

  walletId! : string;
  to! : string;
  secretType! : SecretType;
  network? : {
    name! : string;
    nodeUrl! : string;
    chainId? : number;
  };
  functionName! : string;
  value! : BigDecimal;
  inputs! : [ {
    type! : string;
    value! : string;
  } ],
  chainSpecificFields! :  Object;
}
```

{% hint style="info" %}
The **`chainSpecificFields`** depend on the chain uses to execute the smart contract call. For an overview of the available fields take a look at [Contract calls ](../../deep-dive/contract-calls.md)in the Deep dive section.  
{% endhint %}

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `walletId` | `True` | `String` | ID of the wallet one wants to sign with. |
| `to` | `True` | `String` | Destination address of the transaction.  |
| `secretType` | `True` | [`SecretType`](secrettype.md) | Chain the transaction will be executed on. |
| `network` | `False` | `Object` | The [network](../../deep-dive/environments.md) to submit the transaction to |
| `network.name` | `True` | `String` | Display name of the network to submit the transaction to \(e.g.: "Rinkeby"\). This will be shown to the user when signing the transaction |
| `network.nodeUrl` | `True` | `String` | URL of the node to submit the transaction to \(e.g.: "https://rinkeby.infura.io"\) |
| `network.chainId` | `False` | `Number` | Network ID of the selected network |
| `value` | `True` | `Number` | The amount that will be sent with the contract execution. Value will be passed as-is. This means that for example in Etheruem the value is in WEI |
| `functionName` | `True` | `String` | Name of the function on the contract that needs to be executed |
| `inputs[]` | `True` | `Array` | Array of inputs needed to execute the function |
| `inputs[].type` | `True` | `String` | Type of the input parameter \(ex. uint256\) |
| `inputs[].value` | `True` | `String` | Value of the input parameter. Needs to be passed as a string value, will be parsed by Arkane |
| [`chainSpecificFields`](../../deep-dive/contract-calls.md) | `True` | `Object` | Fields that contain chain specific values. For possible values, please see [chain specific fields documentation](../../deep-dive/contract-calls.md). |

{% hint style="info" %}
🧙 Using the `network` parameter, the node to which the transaction is sent can be set manually. It allows you to submit a transaction to any mainnet or testnet node of your choosing, public or private. \( Ethereum only\)
{% endhint %}

## Example

```javascript
{
  "walletId" : "adc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
  "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
  "secretType" : "ETHEREUM",
  "network" : {
    "name" : "Rinkeby",
    "nodeUrl" : "https://rinkeby.arkane.network",
    "chainId" : null
  },
  "functionName" : "transfer",
  "value" : 0,
  "inputs" : [ {
    "type" : "address",
    "value" : "0x80cbb6c4342948e5be81987dce8251dbedd69138"
  }, {
    "type" : "uint256",
    "value" : 73680000
  } ],
  "chainSpecificFields" : {
    "gasLimit" : "300000"
  }
}
```

## Function Types

{% page-ref page="../reference/executecontract.md" %}

