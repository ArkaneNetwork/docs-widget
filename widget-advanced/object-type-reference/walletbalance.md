# WalletBalance

## Signature

```javascript
{
    secretType?: SecretType; 
    balance!: number;
    symbol!: string;
    gasBalance!: number;
    gasSymbol!: string;
    rawBalance!: string;
    rawGasBalance!: string;
    decimals!: number;
}
```

## Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `secretType` | [`SecretType`](secrettype.md) | Type of blockchain |
| `balance` | `number` | Normalized balance of the native token |
| `symbol` | `string` | Symbol of the native token |
| `gasBalance` | `number` | Normalized balance of the gas token \(same as `balance` when the token for paying gas/fees is the same native token\) |
| `gasSymbol` | `string` | Symbol of the gas token |
| `rawBalance` | `string` | Raw balance of the native token |
| `rawGasBalance` | `string` | Raw balance of the gas token |
| `decimals` | `number` | Number of decimals of the native token |

