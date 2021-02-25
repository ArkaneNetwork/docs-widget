---
description: How to retrieve a user's wallets
---

# Retrieve user wallets

To fetch the wallet for a certain user you need to call the function [`getWallets`](../widget-advanced/reference/untitled.md), which will return an array of [`wallets`](../widget-advanced/object-type-reference/wallet.md) with additional details for each wallet.

{% hint style="info" %}
🧙 If you only want to retrieve a user's wallet then`getWallets` is the perfect function, but if you also need to authenticate the user and maybe get his email address or first name, then it is recommended to [retrieve the user account](retrieve-a-user-account.md).
{% endhint %}

## Function

```javascript
arkaneConnect.api.getWallets();
```

## Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.api.getWallets().then((wallets)=>{
   console.log(`The address of the first wallet is: ${wallets[0].address}`);
});
```

## Returns

```javascript
[ {
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
}, {
  "id" : "3",
  "address" : "0xae52b72db54e137a65a42434ab2543d31f8454c3",
  "walletType" : "THREEWAY_SHARED",
  "secretType" : "VECHAIN",
  "createdAt" : [ 2019, 11, 23, 22, 46, 32 ],
  "archived" : false,
  "alias" : "aliasVechain",
  "description" : "descriptionVechain",
  "primary" : false,
  "hasCustomPin" : false,
  "balance" : {
    "available" : false,
    "secretType" : "VECHAIN",
    "balance" : 1.0,
    "gasBalance" : 1.0,
    "symbol" : "VET",
    "gasSymbol" : "VTHO",
    "rawBalance" : "1000000000000000000",
    "rawGasBalance" : "1000000000000000000",
    "decimals" : 18
  }
} ]

```

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function you can find the signature, its parameters, and possible options documented. 

{% page-ref page="../widget-advanced/reference/untitled.md" %}

