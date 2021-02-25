# AuthenticationInstance

## Signature

```javascript
{
  authenticated?: boolean;
  subject?: string;
  realmAccess?: { roles: string[] };
  resourceAccess?: string[];
  token?: string;
  tokenParsed?: {
    exp?: number;
    email?: string,
    name?: string,
    iat?: number;
    nonce?: string;
    sub?: string;
    session_state?: string;
    realm_access?: { roles: string[] };
    resource_access?: string[];
  };
  refreshToken?: string;
  refreshTokenParsed?: { nonce?: string };
  idToken?: string;
  idTokenParsed?: { nonce?: string };
  timeSkew?: number;
}
```

## Parameters

| Parameter | Description |
| :--- | :--- |
| `authenticated` | Is true if the user is authenticated, false otherwise. |
| `subject` | The user id. |
| `realmAccess` | The realm roles associated with the token. |
| `resourceAccess` | The resource roles associated with the token. |
| `token` | The base64 encoded token that can be sent in the Authorization header in requests to services. |
| `tokenParsed` | The parsed JWT token as a JavaScript object. |
| `refreshToken` | The base64 encoded refresh token that can be used to retrieve a new token. |
| `refreshTokenParsed` | The parsed refresh token as a JavaScript object. |
| `idToken` | The base64 encoded ID token. |
| `idTokenParsed` | The parsed id token as a JavaScript object. |
| `timeSkew` | The estimated time difference between the browser time and the authentication server in seconds. This value is just an estimation but is accurate enough when determining if a token is expired or not. |

