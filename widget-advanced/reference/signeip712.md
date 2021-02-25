---
description: Signing an EIP712 structured message
---

# signEip712



This function signs a structured EIP712 message using a specific account.

```javascript
signer.signEip712({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    secretType: 'ETHEREUM',
    data : {
      "types":{
        "EIP712Domain":[
          {
            "name":"name",
            "type":"string"
          },
          {
            "name":"version",
            "type":"string"
          },
          {
            "name":"chainId",
            "type":"uint256"
          },
          {
            "name":"verifyingContract",
            "type":"address"
          },
          {
            "name":"salt",
            "type":"bytes32"
          }
        ],
        "Bid":[
          {
            "name":"amount",
            "type":"uint256"
          },
          {
            "name":"bidder",
            "type":"Identity"
          }
        ],
        "Identity":[
          {
            "name":"userId",
            "type":"uint256"
          },
          {
            "name":"wallet",
            "type":"address"
          }
        ]
      },
      "domain":{
        "name":"My amazing dApp",
        "version":"2",
        "chainId":1,
        "verifyingContract":"0x1C56346CD2A2Bf3202F771f50d3D14a367B48070",
        "salt":"0xf2d857f4a3edcb9b78b4d503bfe733db1e3f6cdc2b7971ee739626c97e86a558"
      },
      "primaryType":"Bid",
      "message":{
        "amount":100,
        "bidder":{
          "userId":323,
          "wallet":"0x3333333333333333333333333333333333333333"
        }
      }
    }
})
```

## Signature

```javascript
signer.signEip712(eip712SignRequestDto, options?): Promise<SignerResult>
```

## Returns

```javascript
Promise<SignerResult>
```

```javascript
{
  "type" : "HEX_SIGNATURE",
  "r" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd",
  "s" : "0x6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a029",
  "v" : "0x1c",
  "signature" : "0xb91467e570a6466aa9e9876cbcd013baba02900b8979d43fe208a4a4f339f5fd6007e74cd82e037b800186422fc2da167c747ef045e5d18a5f5d4300f8e1a0291c"
}
```



| Parameter | Required | Description |
| :--- | :--- | :--- |
| [`eip712SignRequestDto`](../object-type-reference/wip-tokentransferrequestdto.md) | `True` | EIP712 signature request you want to sign. For more info on how this request should look like, see [`eip712SignRequestDto`](../object-type-reference/wip-tokentransferrequestdto.md) . |
| [`options`](../object-type-reference/wip-redirectoptions.md) | `False` | Redirect options you want to pass. Only available when using a REDIRECT [`signer`](createsigner.md#parameters) |

## 

