---
description: Transfer gas from one destination to another
---

# executeGasTransfer

This function transfers gas \(ex. ETH / VTHO / GAS / …​ \) from one address to another. The destination can be any blockchain address, a wallet, or a smart contract, it can even be an email address.

{% hint style="info" %}
🧙 In case the chain doesn't have a distinct gas token the native token will be used in the transfer.
{% endhint %}

```javascript
signer.executeGasTransfer({
    walletId: '6683c01d-2e10-4982-9b3a-c6ecd45896bb',
    to: 'AN2VD52SLntUGFwzZyjzsRqBBkUzjKpKpT',
    value: 18,
    secretType: 'NEO',
})
```

{% hint style="info" %}
🧙 You don’t have to take into account the number of decimals for different tokens, Arkane handles that for you.

**Example:** If a token has 18 decimals and you want to transfer 1 token, provide the value 1. Arkane will translate this to the correct nondecimal value \(1 \* 10e18\). 
{% endhint %}

## Signature

```javascript
signer.executeGasTransfer(gasTransferRequestDto, options?): Promise<SignerResult>
```

## Returns

```javascript
Promise<SignerResult>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| [`gasTransferRequestDto`](../object-type-reference/wip-gastransferrequestdto.md) | `True` | The transfer request you want to execute. For more info on how this request should look like, see [`gasTransferRequestDto`](../object-type-reference/wip-gastransferrequestdto.md) . |
| [`options`](../object-type-reference/wip-redirectoptions.md) | `False` | Redirect options you want to pass. Only available when using a REDIRECT [`signer`](createsigner.md#parameters) |

## Example

```javascript
const signer = arkaneConnect.createSigner();

signer.executeGasTransfer({
    walletId: '6683c01d-2e10-4982-9b3a-c6ecd45896bb',
    to: 'AN2VD52SLntUGFwzZyjzsRqBBkUzjKpKpT',
    value: 18,
    secretType: 'NEO',
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

{% page-ref page="../object-type-reference/wip-gastransferrequestdto.md" %}

{% page-ref page="../object-type-reference/wip-redirectoptions.md" %}

{% page-ref page="../object-type-reference/wip-signerresult.md" %}

