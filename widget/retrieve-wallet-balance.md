---
description: How to retrieve the native balance of a wallet
---

# Retrieve wallet balance

To fetch the balance of a wallet of a certain user you need to call the function [`getBalance`](../widget-advanced/reference/getbalance.md), which will return a promise containing a [`WalletBalance`](../widget-advanced/object-type-reference/walletbalance.md) object.

{% hint style="info" %}
🧙 If you only want to retrieve the balance of a user's wallet then `getBalance` is the perfect function, but if you also need to fetch his wallets or get some profile information, and maybe even need to authenticate the user, then it is recommended to [retrieve the user account](retrieve-a-user-account.md).
{% endhint %}

## Function

```javascript
arkaneConnect.api.getBalance("<WALLET_ID>");
```

## Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.api.getBalance("d91b644a-076f-44bf-ae90-29251df19784").then((balance) => {
 console.log("The balance is",balance.balance);
})
```

## Returns

```javascript
{
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
```

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function you can find the signature, its parameters, and possible options documented.

{% page-ref page="../widget-advanced/reference/getbalance.md" %}

