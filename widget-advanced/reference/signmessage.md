---
description: Sign a message
---

# signMessage

This function signs arbitrary data using a specific account.

```javascript
signer.signMessage({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    secretType: 'ETHEREUM',
    data : "I agree with terms and conditions"
})
```

## Signature

```javascript
signer.signMessage(messageSignRequestDto, options?): Promise<SignerResult>
```

## Returns

```javascript
Promise<SignerResult>
```

```javascript
{
  "type" : "HEX_SIGNATURE",
  "r" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd",
  "s" : "0x6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a029",
  "v" : "0x1c",
  "signature" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a0291c"
}
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| [`messageSignRequestDto`](../object-type-reference/wip-tokentransferrequestdto.md) | `True` | Signature request you want to sign. For more info on how this request should look like, see [`messageSignRequestDto`](../object-type-reference/wip-tokentransferrequestdto.md) . |
| [`options`](../object-type-reference/wip-redirectoptions.md) | `False` | Redirect options you want to pass. Only available when using a REDIRECT [`signer`](createsigner.md#parameters) |

## Example

```javascript
const signer = arkaneConnect.createSigner();

signer.signMessage({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    secretType: 'ETHEREUM',
    data : "I agree with terms and conditions"
}).then((signerResult) => {
    if (signerResult.success) {
        console.log(`Successfuly signed: ${signerResult.result.signature}`);
    } else {
        console.warn(`Something went wrong while signing the message`);
    }
}).catch((reason) => {
    console.log(error);
});

```

## Object Types

{% page-ref page="../object-type-reference/signer.md" %}

{% page-ref page="../object-type-reference/messagesignrequestdto.md" %}

{% page-ref page="../object-type-reference/wip-redirectoptions.md" %}

{% page-ref page="../object-type-reference/wip-signerresult.md" %}



