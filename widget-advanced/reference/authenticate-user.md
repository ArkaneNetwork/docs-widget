---
description: Authenticate a user to Arkane
---

# authenticate

This function will check if the user is authenticated and if not, ask the user to authenticate. 

```javascript
arkaneConnect.flows.authenticate({ windowMode: 'REDIRECT' });
```

* If [`windowMode`](../initializing-options.md#windowmode) = 'REDIRECT', the user will be redirected to `options.redirectUri` with the result after logging in.
* If [`windowMode`](../initializing-options.md#windowmode) = 'POPUP', the popup will close and the promise resolved when the user finishes the request. No extra options are required.

{% hint style="warning" %}
If you set the [`redirectUri`](../object-type-reference/authenticationoptions.md#parameters) option, make sure that the SDK and the [`AuthenticationResult`](../object-type-reference/authenticationresult.md) handling is also present on the page you redirect to.
{% endhint %}

## Signature

```javascript
arkaneConnect.flows.authenticate(options?: AuthenticationOptions): Promise<AuthenticationResult>    
```

## Returns

```javascript
Promise<AuthenticationResult>
```

## Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `options` |  [`AuthenticationOptions`](../object-type-reference/authenticationoptions.md) | `False` | Provide extra auth options |

## Examples

```javascript
// Example 1
// Redirect to the current page
arkaneConnect.flows.authenticate({ windowMode: 'REDIRECT' });
```

```javascript
// Example 2
// Redirect to https://foo.io
arkaneConnect.flows.authenticate({ redirectUri: 'https://foo.io', windowMode: 'REDIRECT'});
```

```javascript
// Example 3
// Login using popup
arkaneConnect.flows.authenticate({ windowMode: 'POPUP' })
    .then((result: AuthenticationResult) => {
        result
            .authenticated((auth: AuthenticationInstance) => {
                alert('logged in: ' + auth.subject);
            })
            .notAuthenticated((auth: AuthenticationInstance) => {
                alert('not logged in');
            });
    });
```

## Object Types

{% page-ref page="../object-type-reference/authenticationoptions.md" %}

{% page-ref page="../object-type-reference/authenticationresult.md" %}

{% page-ref page="../object-type-reference/authenticationinstance.md" %}

