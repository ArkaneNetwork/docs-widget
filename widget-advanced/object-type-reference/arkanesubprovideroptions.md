# ArkaneSubProviderOptions

## Signature

```text
ArkaneSubProviderOptions {
  clientId: string;
  environment?: string;
  secretType?: SecretType;
  authenticationOptions?: AuthenticationOptions
  skipAuthentication: boolean;
  pollingInterval?: number;
}
```



## Parameters

<table>
  <thead>
    <tr>
      <th style="text-align:left">Option</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">clientId</td>
      <td style="text-align:left">The clientId to connect to Arkane</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="../../deep-dive/environments.md"><code>environment</code></a>
      </td>
      <td style="text-align:left">The environment to which you want to connect, possible values are &apos;staging&apos;
        and &apos;prod&apos;. Default set to &apos;prod&apos;.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="secrettype.md"><code>secretType</code></a>
      </td>
      <td style="text-align:left">The secret type to use, allowed for web3 provider: ETHEREUM, BSC, MATIC</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="authenticationoptions.md"><code>authenticationOptions</code></a>
      </td>
      <td style="text-align:left">The options to use for authentications</td>
    </tr>
    <tr>
      <td style="text-align:left">skipAuthentication</td>
      <td style="text-align:left">Boolean flag that indicates if you want to authenticate immediately or
        revert to <a href="../reference/checkauthenticated.md">checkAuthenticated</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">pollingInterval</td>
      <td style="text-align:left">
        <p>When using subscriptions, this is the interval used for polling for updates.</p>
        <p>&#x26A0;&#xFE0F; when set too low, you will be throttled (Default: 15s)</p>
      </td>
    </tr>
  </tbody>
</table>

