# RedirectOptions

## Signature

```javascript
{
  redirectUri?: string,
  correlationID?: string
}
```

{% hint style="info" %}
🧙 Only available when using a REDIRECT [`signer`](../reference/createsigner.md#parameters)
{% endhint %}

## Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `redirectUri` | `string` | The URI you want the user to be redirected after checking authentication. |
| `correlationID` | `string` | Unique correlationID allowing you to identify this specific transaction. It will be appended as a request parameter to the `redirectUri` upon return |

