---
description: Fetch all the wallets for a specifc user
---

# getWallets

This function returns  all the wallets for the specified user \(bearer token\)

```javascript
arkaneConnect.api.getWallets();
```

## Signature

```javascript
arkaneConnect.api.getWallets(filter?: { secretType?: SecretType, includeBalance?:boolean }): Promise<Wallet[]>
```

## Returns

```javascript
Promise<Wallet[]>
```

## Parameters

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Required</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">filter</td>
      <td style="text-align:left"><code>False</code>
      </td>
      <td style="text-align:left">Filter that will be applied to the result</td>
    </tr>
    <tr>
      <td style="text-align:left">filter.secretType</td>
      <td style="text-align:left"><code>False</code>
      </td>
      <td style="text-align:left">Filter on a blockchain, <a href="../object-type-reference/secrettype.md"><code>SecretType</code></a>.</td>
    </tr>
    <tr>
      <td style="text-align:left">filter.includeBalance</td>
      <td style="text-align:left"><code>False</code>
      </td>
      <td style="text-align:left">
        <p>Include balance when fetching wallets.
          <br />By default: true</p>
        <p>&#x26A0;&#xFE0F; Setting this to true might impact performance</p>
      </td>
    </tr>
  </tbody>
</table>

## Example

```javascript
arkaneConnect.api.getWallets();
```

## Object Types

{% page-ref page="../object-type-reference/secrettype.md" %}

{% page-ref page="../object-type-reference/wallet.md" %}

