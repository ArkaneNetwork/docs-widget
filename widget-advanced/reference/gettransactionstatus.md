---
description: Fetch transaction status
---

# getTransactionStatus

This function returns the status for a specific transaction. 

```javascript
arkaneConnect.api.getTransactionStatus("0xe95cfd4c68e4b43f60adb8a97dc10264ad0046518946a768d980ee454e492645", "ETHEREUM");
```

{% hint style="info" %}
🧙 Returns `UNKNOWN` when the specific chain is not supported.
{% endhint %}

## Signature

```javascript
arkaneConnect.api.getTransactionStatus(transactionHash: string, secretType: SecretType): Promise<TxStatusResult>
```

## Returns

```javascript
Promise<TxStatusResult>
```

```javascript
{
    status: 'UNKNOWN' | 'PENDING' | 'FAILED' | 'SUCCEEDED'
}
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `transactionHash` | `True` | Transaction hash |
| [`secretType`](../object-type-reference/secrettype.md) | `True` | Blockchain related to the transaction hash |

## Example

```javascript
arkaneConnect.api.getTransactionStatus("0xe95cfd4c68e4b43f60adb8a97dc10264ad0046518946a768d980ee454e492645", "ETHEREUM");
```

{% hint style="info" %}
🧙 Using the `network` parameter, the node to which the transaction is sent can be set manually.  It allows you to submit a transaction to any mainnet or testnet node of your choosing, public or private. \( Ethereum only\)
{% endhint %}

## Object Types

{% page-ref page="../object-type-reference/secrettype.md" %}

{% page-ref page="../object-type-reference/wip-txstatusresult.md" %}



