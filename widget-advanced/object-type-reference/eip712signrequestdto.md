# Eip712SignRequestDto

## Signature

```javascript
{
  secretType! : SecretType,
  walletId! : string,
  data! : any
}
```

## Parameters

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Required</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>walletId</code>
      </td>
      <td style="text-align:left"><code>True</code>
      </td>
      <td style="text-align:left"><code>String</code>
      </td>
      <td style="text-align:left">ID of the wallet one wants to sign with.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>secretType</code>
      </td>
      <td style="text-align:left"><code>True</code>
      </td>
      <td style="text-align:left"><a href="secrettype.md"><code>SecretType</code></a>
      </td>
      <td style="text-align:left">Chain the transaction will be executed on.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>data</code>
      </td>
      <td style="text-align:left"><code>True</code>
      </td>
      <td style="text-align:left">
        <p><code>JSON</code>
        </p>
        <p><code>String(containing the JSON)</code>
        </p>
      </td>
      <td style="text-align:left">Should contain valid JSON (keys should be quoted)</td>
    </tr>
  </tbody>
</table>

## Example

```javascript
{
  "secretType" : "ETHEREUM",
  "walletId" : "1def2753-a428-4fd2-9993-fc06917897c6",
  "data" : {
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
}
```

## Function Types

{% page-ref page="../../widget/sign-a-eip712-message.md" %}



