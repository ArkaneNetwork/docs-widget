# AuthenticationOptions

## Signature

```javascript
{
  redirectUri?: string,
  windowMode: WindowMode,
  useOverlayWithPopup?: boolean,
  closePopup?: boolean,
  idpHint?: string
}
```

## Parameters

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left"><b>Description</b>
      </th>
      <th style="text-align:left">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>redirectUri</code>
      </td>
      <td style="text-align:left">The URI you want the user to be redirected after checking authentication.
        Only used when <a href="../initializing-options.md#windowmode"><code>windowMode</code></a><code> = REDIRECT.</code> Not
        required, default is the current URI</td>
      <td style="text-align:left"><code>&apos;https://foo.io&apos;</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>windowMode</code>
      </td>
      <td style="text-align:left">Show login form in POPUP, or login using redirect. Default is<a href="../initializing-options.md#windowmode"><code>windowMode</code></a> passed
        in <a href="../initializing-options.md#constructoroptions"><code>ConstructorOptions</code></a>.</td>
      <td
      style="text-align:left"><code>&apos;REDIRECT&apos;</code>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>useOverlayWithPopup</code>
      </td>
      <td style="text-align:left">When using a popup, show an overlay on the parent screen. Default is
        <a
        href="../initializing-options.md#popupoptions"><code>useOverlayWithPopup</code>
          </a>passed in <a href="../initializing-options.md#constructoroptions"><code>ConstructOptions</code></a>.</td>
      <td
      style="text-align:left"><code>false</code>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>idpHint</code>
      </td>
      <td style="text-align:left">When passed, the initial login screen where a user can choose between
        social logins and regular signings is skipped and goes directly to the
        given identity provider</td>
      <td style="text-align:left">
        <p><code>google</code>
        </p>
        <p><code>facebook</code>
        </p>
        <p><code>twitter</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>

