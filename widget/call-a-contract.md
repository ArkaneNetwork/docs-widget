---
description: How to perform a contract call
---

# Call a contract

A contract call is the equivalent to launching a blockchain transaction. We've already covered that we can't execute a transaction without the user's approval. Therefore to be able to call a contract we will need to do two things i\) define the contract call and ii\) ask the user for his approval.

The object that can ask the user his approval is called a [`Signer`](../widget-advanced/object-type-reference/signer.md), once we've created a `Signer` object we can use the `Signer` to perform the contract call.

## Function

```javascript
//Creating the signer
arkaneConnect.createSigner();

//Asking the signer to transfer a certain value to a certain destination.
signer.executeContract({
    secretType: '<BLOCKCHAIN>',
    walletId: '<WALLET_ID>',
    to: '<BLOCKCHAIN ADDRESS>',
    value: 0,
    functionName: '<CONTRACT_FUNCTION_NAME>',
    inputs: [
      {type: "address", value: "0x80cbb6c4342948e5be81987dce8251dbedd69138"},
      {type: "uint256", value: "73680000"}
    ]
})
```

## Example

```javascript
const signer = arkaneConnect.createSigner();

signer.executeContract({
    secretType: 'ETHEREUM',
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    value: 0,
    functionName: 'transfer',
    inputs: [
      {type: "address", value: "0x80cbb6c4342948e5be81987dce8251dbedd69138"},
      {type: "uint256", value: "73680000"}
    ]
})
```

## Returns

```javascript
{
    result: {
        transactionHash: "0xe18975940be795f178b2a0bc553a0d40e0ad6ceb72ee5f62ac53f0a816b4460f"
    }
    status: "SUCCESS"
}
```

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function you can find the signature, its parameters, and possible options documented.

{% page-ref page="../widget-advanced/reference/createsigner.md" %}

{% page-ref page="../widget-advanced/reference/executecontract.md" %}

