---
description: Create a Signer object
---

# createSigner

This function will create a [`Signer`](../object-type-reference/signer.md) that allows the user to sign or execute a transaction. Consider a Signer as the approval of the user.

```javascript
arkaneConnect.createSigner();
```

In order for the user the give his approval he requires to enter his PIN. A [`Signer`](../object-type-reference/signer.md) will enable him to do so. The [`Signer`](../object-type-reference/signer.md) object also has the [`WindowMode`](../object-type-reference/windowmode.md) and [`PopupOptions`](../object-type-reference/popupoptions.md) available.

{% hint style="info" %}
If you are using the popup signer and you want to execute a transaction as a reaction to an event \(e.g. a button click\), then call `arkaneConnect.createSigner(…​)` as very first in your event handler otherwise, the popup might get blocked by the popup blocker of the browser.
{% endhint %}

#### closePopup

When using the POPUP [`WindowMode`](../object-type-reference/windowmode.md) you can close the [`Signer`](../object-type-reference/signer.md) popup manually in case something went wrong. You can use the code snippet below to close it. The type guard, isn’t mandatory, but it makes the code more robust.

```javascript
if (arkaneConnect.isPopupSigner(signer)) {
    signer.closePopup();
}
```

## Signature

```javascript
arkaneConnect.createSigner(signUsing?: WindowMode, popupOptions?: PopupOptions): Signer
```

## Returns

```javascript
Signer
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `signUsing` | `False` | The [`WindowMode`](../object-type-reference/windowmode.md) you want to use |
| `popupOptions` | `False` | The [`PopupOptions`](../object-type-reference/popupoptions.md) you want to use |

## Example

```javascript
const signer = arkaneConnect.createSigner('REDIRECT');
```

Example closing a [`Signer`](../object-type-reference/signer.md) with [`WindowMode`](../object-type-reference/windowmode.md) = POPUP

```javascript
const signer = arkaneConnect.createSigner('POPUP');
if (arkaneConnect.isPopupSigner(signer)) {
    signer.closePopup();
}
```

## Object Types

{% page-ref page="../object-type-reference/signer.md" %}



