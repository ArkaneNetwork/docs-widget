# TxStatusResult

## Signature

```javascript
{
    status: 'UNKNOWN' | 'PENDING' | 'FAILED' | 'SUCCEEDED'
}
```

## Parameters

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>status</code>
      </td>
      <td style="text-align:left"><code>String</code>
      </td>
      <td style="text-align:left">
        <ul>
          <li><code>UNKNOWN</code> Not yet visible on the chain.</li>
          <li><code>PENDING</code> Not yet completed (or failed).</li>
          <li><code>SUCCEEDED</code> Completed successfully</li>
          <li><code>FAILED</code> Transaction is failed.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Example

```javascript
{
  "secretType" : "ETHEREUM",
  "walletId" : "1def2753-a428-4fd2-9993-fc06917897c6",
  "data" : "I agree with terms and conditions"
}
```

## Function Types

{% page-ref page="../reference/gettransactionstatus.md" %}



