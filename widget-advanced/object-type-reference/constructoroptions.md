# ConstructorOptions

## Signature

```javascript
{
  environment?: string,
  windowMode?: WindowMode,
  signMethod?: string,
  bearerTokenProvider?: () => string,
  useOverlayWithPopup?: boolean;
}
```

## Parameters

| Option | Description |
| :--- | :--- |
| [`environment`](../../deep-dive/environments.md) | The environment to which you want to connect, possible values are 'local', 'tst1', 'staging', 'prod'. Default set to 'prod'. |
| [`windowMode`](windowmode.md) | The sign method you want to use, possible values are 'POPUP' or 'REDIRECT'. Default set to 'POPUP'. |
| `signMethod` | **Deprecated** Use [`windowMode`](windowmode.md) instead |
| `bearerTokenProvider` | You can implement all the authentication handling yourself and provide Arkane Connect with your own bearer token provider. The bearer token provider is a function returning the bearer token \(access token\) to login to Arkane. Default the [Arkane Connect authentication client](../../deep-dive/authentication.md) is used. |
| `useOverlayWithPopup` | When using a popup, show an overlay on the parent screen. Default set to 'true'.  |

