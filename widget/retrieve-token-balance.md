---
description: How to retrieve the balance of a token for a wallet
---

# Retrieve token balance

To fetch the balance of a certain token for a wallet, you need to call the function [`getTokenBalance`](../widget-advanced/reference/gettokenbalance.md) which will return a promise containing a [`TokenBalance`](../widget-advanced/object-type-reference/tokenbalance.md) object. If you need the entire balance a certain wallet holds, it is recommended to use the [`getTokenBalances`](../widget-advanced/reference/gettokenbalances.md) function. 

## Function

```javascript
arkaneConnect.api.getTokenBalance("<WALLET_ID>", "<TOKEN_ADDRESS>");
```

## Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.api.getTokenBalance("c8ec9954-fa1a-4682-9cf8-ef5c1015d1d1","0x7d1afa7b718fb893db30a3abc0cfc608aacfebb0").then((tokenBalance) => {
 console.log("The balance of",tokenBalance.symbol,"is",tokenBalance.balance);
})
```

## Returns

```javascript
{
  balance: 392.10420561176494
  decimals: 18
  logo: "https://raw.githubusercontent.com/ArkaneNetwork/content-management/master/tokens/ethereum/mainnet/logos/0x7d1afa7b718fb893db30a3abc0cfc608aacfebb0.png"
  rawBalance: "392104205611764916095"
  symbol: "MATIC"
  tokenAddress: "0x7d1afa7b718fb893db30a3abc0cfc608aacfebb0"
  transferable: true
  type: "ERC20"
}
```

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function you can find the signature, its parameters, and possible options documented.

{% page-ref page="../widget-advanced/reference/gettokenbalance.md" %}

