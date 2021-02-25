---
description: How to ask users to sign a message
---

# Sign a message

Signing a message is the equivalent to asking the user to sign his signature. Therefore to sign a message, we need to define the message for the user to sign and request his approval.

The object that can ask the user his approval is called a [`Signer`](../widget-advanced/object-type-reference/signer.md), once we've created a `Signer` object we can use the `Signer` to sign the message.

## Function

```javascript
//Creating the signer
arkaneConnect.createSigner();

//Asking the signer to sign a message.
signer.signMessage({
    walletId: '<WALLET_ID>',
    secretType: '<BLOCKCHAIN>',
    data : "<YOUR_MESSAGE>"
})
```

## Example

```javascript
const signer = arkaneConnect.createSigner();

signer.signMessage({
    walletId: 'c8ec9954-fa1a-4682-9cf8-ef5c1015d1d1',
    secretType: 'ETHEREUM',
    data : "I agree with terms and conditions"
})
```

## Returns

```javascript
{
    result: {
        r: "0xc5e7a538a353c53e839ed0a2cf7b726806114b637ad1c527046adfc92fecf0d8"
        s: "0x551041e78e3b3d4432f653d708965d34aceaf067255d9cc5970283b00d5f95e0"
        signature: "0xc5e7a538a353c53e839ed0a2cf7b726806114b637ad1c527046adfc92fecf0d8551041e78e3b3d4432f653d708965d34aceaf067255d9cc5970283b00d5f95e01b"
        v: "0x1b"
    }
    status: "SUCCESS"
}
```

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function you can find the signature, its parameters, and possible options documented.

{% page-ref page="../widget-advanced/reference/createsigner.md" %}

{% page-ref page="../widget-advanced/reference/signmessage.md" %}

