---
description: How to retrieve a user account
---

# Retrieve a user account

The function to retrieve a user account [`getAccount`](../widget-advanced/reference/getaccount.md) is one of the most powerful functions that the widget has to offer. Not only does it provide a ton of information,  it also takes care of prerequisites, such as authentication and wallet creation.

The function returns the user's profile and the user's wallet\(s\) all in one response. It will also make sure to authenticate the user and create a wallet for him if needed.

## Function

```javascript
arkaneConnect.flows.getAccount('ETHEREUM')
```

## Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.flows.getAccount('ETHEREUM').then((account) => {
  console.log('User name:', account.auth.tokenParsed.name);
  console.log('User email:', account.auth.tokenParsed.email);
  console.log('First wallet address:', account.wallets[0].address);
  console.log('First wallet balance:', account.wallets[0].balance.balance);
});
```

## Returns

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

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function you can find the signature, its parameters, and possible options documented.

{% page-ref page="../widget-advanced/reference/getaccount.md" %}



