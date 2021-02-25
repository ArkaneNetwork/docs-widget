---
description: Log the user out of Arkane
---

# logout

This function will log the user out of Arkane.

```javascript
// Log out and redirect to the current page
arkaneConnect.logout({ windowMode: 'REDIRECT' });
```

The behavior is different depending on the [`windowMode`](../initializing-options.md#windowmode) used to [instantiate ArkaneConnect](../initializing-options.md) or provided in the options.

* **POPUP** \(default\): The user will be logged out in the background and the promise will resolve when finished. This means the application needs to clean up all user data on screen itself.
* **REDIRECT**: The user will be redirected to the logout endpoint of our Arkane authentication provider. Followed by a redirect back to the page the user was on. The page can be altered by using the option `redirectUri` . The page refreshes automatically, no cleanup is necessary.

{% hint style="warning" %}
If you set the [`redirectUri`](../object-type-reference/authenticationoptions.md#parameters) option, make sure that the SDK and the [`AuthenticationResult`](../object-type-reference/authenticationresult.md) handling is also present on the page you redirect to.
{% endhint %}

## Signature

```javascript
arkaneConnect.logout(options?: AuthentciationOptions): Promise<void>
```

## Returns

```javascript
Promise<void>
```

## Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `options` |  [`AuthenticationOptions`](../object-type-reference/authenticationoptions.md) | `False` | Provide extra options on who to logout |

## Examples

```javascript
// Example 1
// Log out, then cleanup user data on screen
arkaneConnect.logout({ windowMode: 'POPUP' })
             .then(() => {
                 // Cleanup user data on screen
                 handleLogout();
             });
```

```javascript
// Example 2
// Log out and redirect to https://foo.io
arkaneConnect.logout({ windowMode: 'REDIRECT' , redirectUri: 'https://foo.io'});
```

## Object Types

{% page-ref page="../object-type-reference/authenticationoptions.md" %}

{% page-ref page="../object-type-reference/authenticationresult.md" %}

{% page-ref page="../object-type-reference/authenticationinstance.md" %}

