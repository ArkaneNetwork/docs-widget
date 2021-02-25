# Signer

The `Signer` allows the user to sign or execute a transaction. Consider a Signer as the approval of the user. In order for the user the give his approval he requires to enter his PIN. A `Signer` will enable him to do so. 

{% hint style="info" %}
If you are using the popup signer and you want to execute a transaction as a reaction to an event \(e.g. a button click\), then call `arkaneConnect.createSigner(…​)` as very first in your event handler otherwise, the popup might get blocked by the popup blocker of the browser.
{% endhint %}

## closePopup

When using the POPUP [`WindowMode`](windowmode.md) you can close the [`Signer`](signer.md) popup manually in case something went wrong. You can use the code snippet below to close it. The type guard, isn’t mandatory, but it makes the code more robust.

```javascript
if (arkaneConnect.isPopupSigner(signer)) {
    signer.closePopup();
}
```

## Function Types

{% page-ref page="../reference/createsigner.md" %}

{% page-ref page="../reference/executetransfer.md" %}

{% page-ref page="../reference/executetokentransfer.md" %}

{% page-ref page="../reference/executenfttransfer.md" %}

{% page-ref page="../reference/executegastransfer.md" %}

{% page-ref page="../reference/executecontract.md" %}

{% page-ref page="../reference/signmessage.md" %}



