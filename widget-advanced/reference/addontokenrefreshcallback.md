---
description: Receive a callback when the bearer token refreshes
---

# addOnTokenRefreshCallback

You can add a callback method that will be called each time the bearer token is refreshed. This can only be used while using the Arkane Connect JS[ authentication client](../../deep-dive/authentication.md). This function has one parameter: a callback function accepting one parameter \(the new bearer token\) and returning void.

```javascript
arkaneConnect.addOnTokenRefreshCallback(token => {
  console.log('Refreshed bearer token: ' + token);
});
```

## Signature

```javascript
arkaneConnect.addOnTokenRefreshCallback(tokenRefreshCallback: (token: string) => void): void
```

## Returns

```javascript
Promise<AuthenticationResult>
```

## Parameters

| Parameter | Description |
| :--- | :--- |
| `tokenRefreshCallback` | a callback function accepting one parameter \(the new bearer token\) and returning void. \(Required\) |

## Example

```javascript
arkaneConnect.addOnTokenRefreshCallback(token => {
  console.log('Refreshed bearer token: ' + token);
});
```

## Object Types

{% page-ref page="../object-type-reference/authenticationresult.md" %}

