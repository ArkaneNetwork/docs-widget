# ArkaneSubProviderOptions



```text
ArkaneSubProviderOptions {
  clientId: string;
  environment?: string;
  /** Deprecated, use windowMode instead */
  signMethod?: string;
  windowMode?: string;
  bearerTokenProvider?: () => string;
  secretType?: SecretType;
  network?: Network;
  authenticationOptions?: AuthenticationOptions
  skipAuthentication: boolean;
  pollingInterval?: number;
}
```

