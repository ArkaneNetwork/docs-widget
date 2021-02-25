# AuthenticationResult

You can supply two callback functions to the `AuthenticationResult` `authenticated` and `notAuthenticated`, each will be passed the [`AuthenticationInstance`](authenticationinstance.md).

## Signature

```javascript
{
    auth: AuthenticationInstance,
    isAuthenticated: boolean,
    authenticated: (onAuthenticated: (auth: AuthenticationInstance) => void) => AuthenticationResult;
    notAuthenticated: (onNotAuthenticated: (auth: AuthenticationInstance) => void) => AuthenticationResult;
}
```

## Parameters

| Parameter | **Required** | Description |
| :--- | :--- | :--- |
| `authenticated` | `True` | a callback function to be executed when the user is authenticated after the call. |
| `notAuthenticated` | `True` | a callback function to be executed when the user is **not** authenticated after the call. |

## Example

```javascript
// Check if a user is authenticated.
arkaneConnect.checkAuthenticated()
             .then((result) => result.authenticated((auth) => {
                                        console.log('The user is authenticated: ' + auth.subject);
                                     })
                                     .notAuthenticated((auth) => {
                                        console.log('The user is not authenticated');
                                     })
             );

// Check if a user is authenticated. If not, show the login form
arkaneConnect.authenticate()
            .then((result) => result.authenticated((auth) => {
                                       console.log('The user is authenticated: '  + auth.subject);
                                    })
                                    .notAuthenticated((auth) => {
                                       console.log('The user is not authenticated');
                                    })
            );
```

