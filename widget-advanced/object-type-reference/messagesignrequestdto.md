# MessageSignRequestDto

## Signature

```javascript
{
  secretType! : SecretType,
  walletId! : string,
  data! : string
}
```

## Parameters

| Parameter | Required | Type | Description |
| :--- | :--- | :--- | :--- |
| `walletId` | `True` | `String` | ID of the wallet one wants to sign with. |
| `secretType` | `True` | [`SecretType`](secrettype.md) | Chain the transaction will be executed on. |
| `data` | `True` | `String` | Address of the token |

## Example

```javascript
{
  "secretType" : "ETHEREUM",
  "walletId" : "1def2753-a428-4fd2-9993-fc06917897c6",
  "data" : "I agree with terms and conditions"
}
```

## Function Types

{% page-ref page="../reference/signmessage.md" %}



