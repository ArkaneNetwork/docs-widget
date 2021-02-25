---
description: Check if a user is authenticated in Arkane
---

# checkAuthenticated

This function call will check if the user is authenticated and redirect the user to `options.redirectUri` \(if present\) with the result.

```javascript
arkaneConnect.checkAuthenticated();
```

{% hint style="warning" %}
If you set the [`redirectUri`](../object-type-reference/authenticationoptions.md#parameters) option, make sure that the SDK and the[`AuthenticationResult`](../object-type-reference/authenticationresult.md) handling is also present on the page you redirect to.
{% endhint %}

## Signature

```javascript
arkaneConnect.checkAuthenticated(options?: AuthenticationOptions): Promise
```

## Returns

```javascript
Promise<AuthenticationResult>
```

## Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `options` |  [`AuthenticationOptions`](../object-type-reference/authenticationoptions.md) | `False` | Provide extra auth options |

## Example

```javascript
// Redirect to https://arkane.network
arkaneConnect.checkAuthenticated({ redirectUri: 'https://arkane.network' });
```

## Object Types

{% page-ref page="../object-type-reference/authenticationoptions.md" %}

{% page-ref page="../object-type-reference/authenticationresult.md" %}

{% page-ref page="../object-type-reference/authenticationinstance.md" %}





