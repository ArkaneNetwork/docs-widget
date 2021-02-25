---
description: Transfer a fungible token from one destination to another
---

# executeTokenTransfer

This function transfers fungible tokens \(ex. ERC20/TRC20/VIP180/NEP5/GO20/…​\) from one address to another. The destination can be any blockchain address, a wallet, or a smart contract, it can even be an email address.

```javascript
signer.executeTokenTransfer({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    value: 1010,
    tokenAddress: '0x02f96ef85cad6639500ca1cc8356f0b5ca5bf1d2'
    secretType: 'ETHEREUM',
})
```

{% hint style="info" %}
🧙 You don’t have to take into account the number of decimals for different tokens, Arkane handles that for you.

**Example:** If a token has 18 decimals and you want to transfer 1 token, provide the value 1. Arkane will translate this to the correct nondecimal value \(1 \* 10e18\). 
{% endhint %}

## Signature

```javascript
signer.executeTokenTransfer(tokenTransferRequestDto, options?): Promise<SignerResult>
```

## Returns

```javascript
Promise<SignerResult>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| [`tokenTransferRequestDto`](../object-type-reference/wip-tokentransferrequestdto.md) | `True` | The transfer request you want to execute. For more info on how this request should look like, see [`tokenTransferRequestDto`](../object-type-reference/wip-tokentransferrequestdto.md) . |
| [`options`](../object-type-reference/wip-redirectoptions.md) | `False` | Redirect options you want to pass. Only available when using a REDIRECT [`signer`](createsigner.md#parameters) |

## Example

```javascript
const signer = arkaneConnect.createSigner();

signer.executeTokenTransfer({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    value: 1010,
    tokenAddress: '0x02f96ef85cad6639500ca1cc8356f0b5ca5bf1d2'
    secretType: 'ETHEREUM',
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

{% page-ref page="../object-type-reference/wip-tokentransferrequestdto.md" %}

{% page-ref page="../object-type-reference/wip-redirectoptions.md" %}

{% page-ref page="../object-type-reference/wip-signerresult.md" %}



