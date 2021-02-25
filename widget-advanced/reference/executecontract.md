---
description: Execute a contract call
---

# executeContract

This function allows you to execute a function on a smart contract \(write\). As a result, a new transaction will be submitted to the network containing the smart contract execution. 

{% hint style="warning" %}
This function is not supported for each blockchain. Please read [Contract calls](../../deep-dive/contract-calls.md) for more details.
{% endhint %}

```javascript
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

## Signature

```javascript
signer.executeContract(contractExecutionDto, options?): Promise<SignerResult>
```

## Returns

```javascript
Promise<SignerResult>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| [`contractExecutionDto`](../object-type-reference/wip-tokentransferrequestdto.md) | `True` | Details about the smart contract function you want to execute. For more info on the structure see [`contractExecutionDto`](../object-type-reference/wip-contractexecutiondto.md) . |
| [`options`](../object-type-reference/wip-redirectoptions.md) | `False` | Redirect options you want to pass. Only available when using a REDIRECT [`signer`](createsigner.md#parameters) |

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
}).then((signerResult) => {
    if (signerResult.success) {
        console.log(`Transaction ${signerResult.result.transactionHash} has been successfully executed!`);
    } else {
        console.warn(`Something went wrong while executing the transaction`);
    }
}).catch((reason) => {
    console.log(error);
});
```

{% hint style="info" %}
🧙 Using the `network` parameter, the node to which the transaction is sent can be set manually.  It allows you to submit a transaction to any mainnet or testnet node of your choosing, public or private. \( Ethereum only\)
{% endhint %}

## Object Types

{% page-ref page="../object-type-reference/signer.md" %}

{% page-ref page="../object-type-reference/wip-contractexecutiondto.md" %}

{% page-ref page="../object-type-reference/wip-redirectoptions.md" %}

{% page-ref page="../object-type-reference/wip-signerresult.md" %}

