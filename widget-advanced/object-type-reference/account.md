# Account

## Signature

```javascript
{
   wallets: Wallet[],
   auth: AuthenticationInstance,
   isAuthenticated: boolean
}
```

## Parameters

| Parameter | Description |
| :--- | :--- |
| `wallets` | Array of [`wallet`](wallet.md) |
| `auth` | The [`AuthenticationInstance`](authenticationinstance.md) |
| `isAuthenticated` | Is true if the user is authenticated, false otherwise. |

## Example

```javascript
{
    auth: {
        tokenParsed: {
            email: "karel.striegel@arkane.network"
            email_verified: true
            family_name: "Striegel"
            given_name: "Karel"
            name: "Karel Striegel"
            preferred_username: "karel.striegel@arkane.network"
        {
    wallets: [] {
        0: {
            address: "0x6156174Da796228b376e3e58506194543cfBCA38"
            archived: false
            balance: {
                available: true
                balance: 0.0012
                decimals: 18
                gasBalance: 0.0012
                gasSymbol: "ETH"
                rawBalance: "1200000000000000"
                rawGasBalance: "1200000000000000"
                secretType: "ETHEREUM"
                symbol: "ETH"
            }
            createdAt: "2020-04-24T08:35:08.566735"
            description: "Kovan Test Wallet"
            id: "1909c484-0dae-4841-89d3-ee9a313c426c"
            secretType: "ETHEREUM"
        }
    }
}
```

