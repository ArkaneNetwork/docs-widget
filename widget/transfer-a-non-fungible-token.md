---
description: >-
  How to perform a non-fungible transfer. E.g transfer an ERC721 or ERC1155
  token from one wallet to another.
---

# Transfer a non-fungible token

It is not possible to transfer value from a wallet without the approval of the user. Therefore to be able to transfer a token, we will need to do two things: i\) create the transfer and ii\) ask the user for his approval.

The object that can ask the user his approval is called a [`Signer`](../widget-advanced/object-type-reference/signer.md), once we've created a `Signer` object we can use the `Signer` to perform the token transfer.

## Function

```javascript
//Creating the signer
arkaneConnect.createSigner();

//Asking the signer to transfer a certain value to a certain destination.
signer.executeNftTransfer({
    walletId: '<WALLET_ID>',
    to: '<BLOCKCHAIN ADDRESS>',
    tokenAddress: '<TOKEN_BLOCKCHAIN ADDRESS>',
    tokenId: '<TOKEN_ID>',
    secretType: '<BLOCKCHAIN>',
})
```

## Example

{% tabs %}
{% tab title="Address" %}
```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 

//Creating the signer
const signer = arkaneConnect.createSigner();

//Asking the signer to transfer ERC20 token to a blockchain address.
signer.executeNftTransfer({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    tokenAddress: '0x158b6a3540eeced8ecb40f9389e88f0902a3da9f'
    tokenId: '65'
    secretType: 'ETHEREUM',

})
```
{% endtab %}

{% tab title="Email" %}
```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 

//Creating the signer
const signer = arkaneConnect.createSigner();

//Asking the signer to transfer ERC20 tokens to an email address
signer.executeNftTransfer({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: 'john.smith@gmail.com',
    tokenAddress: '0x158b6a3540eeced8ecb40f9389e88f0902a3da9f'
    tokenId: '65'
    secretType: 'ETHEREUM',

})
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
🧙 The destination of a token transfer is not limited to a blockchain address, we also support **email addresses**.
{% endhint %}

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

{% page-ref page="../widget-advanced/reference/executenfttransfer.md" %}

