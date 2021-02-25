---
description: Unlink a wallet from an application
---

# unlink

This function allows a project to unlink a wallet from its application.

```javascript
arkaneConnect.api.unlink("d91b644a-076f-44bf-ae90-29251df19784")
```

## Signature

```javascript
arkaneConnect.api.unlink(walletId: string): Promise<void>
```

## Returns

```javascript
Promise<void>
```

## Parameters

| Parameter | Required | Description |
| :--- | :--- | :--- |
| `walletId` | `True` | The wallet ID of the wallet you want to unlink. |

## Example

```javascript
arkaneConnect.api.unlink("d91b644a-076f-44bf-ae90-29251df19784")   
             .then(() => {
                 // Update UI
                 myFunction();
             });
```

