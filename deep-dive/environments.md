---
description: More detail about environments and networks
---

# Environments & networks

Depending on which environment your application is connecting, your blockchain transactions will be directed to a specific blockchain network. 

Below you find an overview. It is possible to use different networks or your own infrastructure, by making use of the `network` parameter available as an option in several functions. 

## Details

### Production

#### Endpoints

| Service | Description | URL |
| :--- | :--- | :--- |
| Authentication | Endpoint to authenticate | [https://login.arkane.network](https://login.arkane.network/) |
| Wallet | Wallet user interface | [https://app.arkane.network](https://app.arkane.network) |
| API | Endpoint for API calls | [https://api.arkane.network](https://api.arkane.network) |
| Connect | Endpoint used by the Widget | [https://connect.arkane.network](https://connect.arkane.network) |

{% hint style="info" %}
🧙 To connect to our production environment and mainnet, you will need to [register your app](https://arkane-network.typeform.com/to/hzbcGJ) to get a Client ID. 
{% endhint %}

#### Blockchain networks

| Blockchain | Network |
| :--- | :--- |
| Ethereum | mainnet |
| Binance Smart Chain | mainnet |
| Bitcoin | mainnet |
| VeChain | mainnet |
| Litecoin | mainnet |
| GoChain | mainnet |
| Tron | mainnet |
| Aeternity | mainnet |
| NEO | mainnet |
| Matic | mainnet |

{% hint style="info" %}
You are able to use your own nodes by making use of the `network` parameter.
{% endhint %}

### Staging

#### Endpoints

| Service | Description | URL |
| :--- | :--- | :--- |
| Authentication | Endpoint to authenticate | [https://login-staging.arkane.network/](https://login-staging.arkane.network/) |
| Wallet | Wallet user interface | [https://staging.arkane.network/](https://staging.arkane.network/) |
| API | Endpoint for API calls | [https://api-staging.arkane.network/](https://api-staging.arkane.network/) |
| Connect | Endpoint used by the Widget | [https://connect-staging.arkane.network/](https://connect-staging.arkane.network/) |

#### Blockchain networks

| Blockchain | Network |
| :--- | :--- |
| Ethereum | testnet \(Kovan\) |
| Binance Smart Chain | testnet |
| Bitcoin | testnet \(testnet3\) |
| VeChain | testnet |
| Litecoin | testnet |
| GoChain | testnet |
| Tron | testnet \(shasta\) |
| Aeternity | testnet |
| NEO | testnet |
| Matic | testnet \(mumbai\) |

{% hint style="info" %}
You are able to use your own nodes, even own testnets by making use of the `network` parameter.
{% endhint %}

## How to select an environment

By default, you will connect to our production environment  

```javascript
// use production environment
const arkaneConnect = new ArkaneConnect('CLIENT_ID');
```

To connect to the staging environment you add the parameter  `environment`

```javascript
// use staging environment
const arkaneConnect = new ArkaneConnect('CLIENT_ID', { environment: 'staging'});
```

## How to select a network

By default, you will connect to the blockchain network as described above. Mainnet when connecting to our production environment and a certain testnet when connecting to staging.

```javascript
//Using the default Kovan Ethereum testnet
{
  "walletId" : "cdc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
  "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
  "secretType" : "ETHEREUM",
  "data" : "0x",
  "value" : 1.15
}
```

By making use of the network object, you can change the node endpoint. In the example below we are connecting to the Rinkeby Ethereum testnet, instead of the default Kovan testnet.

```javascript
//Using a custom node to connect to the Rinkeby Ethereum testnet
{
  "walletId" : "cdc4c08a-b8fa-4e4c-z5a2-92c87b80f174",
  "to" : "0xdc71b72db51e227e65a45004ab2798d31e8934c9",
  "secretType" : "VECHAIN",
  "network" : {
    "name" : "Rinkeby",
    "nodeUrl" : "https://rinkeby.arkane.network",
    "chainId" : null
  },
  "data" : "0x",
  "value" : 1.15
}
```

