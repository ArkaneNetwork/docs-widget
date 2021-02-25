---
description: Transfer a non-fungible token from one destination to another
---

# executeNftTransfer

This function transfers non-fungible tokens \(ex. ERC721/ ERC1155 / VIP181/…​ \) from one address to another. The destination can be any blockchain address, a wallet, or a smart contract, it can even be an email address.

```javascript
signer.executeNftTransfer({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    tokenAddress: '0x158b6a3540eeced8ecb40f9389e88f0902a3da9f'
    tokenId: '65'
    secretType: 'ETHEREUM',
})
```

## Signature

```javascript
signer.executeNftTransfer(nftTransferRequestDto, options?): Promise<SignerResult>
```

## Returns

```javascript
Promise<SignerResult>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| [`nftTransferRequestDto`](../object-type-reference/wip-nfttransferrequestdto.md) | `True` | The transfer request you want to execute. For more info on how this request should look like, see[ `nftTransferRequestDto`](../object-type-reference/wip-nfttransferrequestdto.md) . |
| [`options`](../object-type-reference/wip-redirectoptions.md) | `False` | Redirect options you want to pass. Only available when using a REDIRECT [`signer`](createsigner.md#parameters) |

## Example

```javascript
const signer = arkaneConnect.createSigner();

signer.executeNftTransfer({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    tokenAddress: '0x158b6a3540eeced8ecb40f9389e88f0902a3da9f'
    tokenId: '65'
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
🧙 Using the `network` parameter, the node to which the transaction is sent can be set manually.  It allows you to submit a transaction to any mainnet or testnet node of your choosing, public or private. \(Ethereum only\)
{% endhint %}

## Object Types

{% page-ref page="../object-type-reference/signer.md" %}

{% page-ref page="../object-type-reference/wip-nfttransferrequestdto.md" %}

{% page-ref page="../object-type-reference/wip-redirectoptions.md" %}

{% page-ref page="../object-type-reference/wip-signerresult.md" %}

