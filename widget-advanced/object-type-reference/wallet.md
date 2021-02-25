# Wallet

## Signature

```javascript
{
    id!: string;
    address!: string;
    walletType?: WalletType;
    secretType!: SecretType;
    archived!: boolean;
    alias?: string = '';
    description?: string = '';
    primary?: boolean;
    balance?: WalletBalance;
    hasCustomPin?: false;
    status!: string;
    createdAt?: Date;
    lastUpdated?: number = 0;
}
```

## Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `id` | `string` | Wallet ID |
| `address` | `string` | Blockchain address |
| `walletType` | `WalletType` | Type of the wallet |
| `secretType` | [`SecretType`](secrettype.md) | Type of the blockchain |
| `archived` | `boolean` | Is the wallet archived |
| `alias` | `string` | Wallet alias |
| `description` | `string` | Wallet description |
| `primary` | `boolean` | Is the wallet the primary wallet for the `secretType`? |
| `balance` | [`WalletBalance`](walletbalance.md) | Native token balance of the wallet |
| `hasCustomPin` | `boolean` | Has the wallet a custom pin. |
| `createdAt` | `Date` | Creation date |
| `lastUpdated` | `number` | Last updated |

## Example

```javascript
{
  "id" : "1",
  "address" : "0xdc72b72db54e227e65a45004ab2798d31e8934c2",
  "walletType" : "THREEWAY_SHARED",
  "secretType" : "ETHEREUM",
  "createdAt" : [ 2019, 11, 23, 22, 46, 32 ],
  "archived" : false,
  "alias" : "aliasEth",
  "description" : "descriptionEth",
  "primary" : false,
  "hasCustomPin" : false,
  "balance" : {
    "available" : false,
    "secretType" : "ETHEREUM",
    "balance" : 1.0,
    "gasBalance" : 1.0,
    "symbol" : "ETH",
    "gasSymbol" : "ETH",
    "rawBalance" : "1000000000000000000",
    "rawGasBalance" : "1000000000000000000",
    "decimals" : 18
  }
}
```

