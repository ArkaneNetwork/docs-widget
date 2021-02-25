---
description: How to retrieve a user's profile.
---

# Retrieve user profile

To get the profile of a user you need to call the function [`getProfile`](../widget-advanced/reference/getprofile.md), which will return a promise including the user's information.

{% hint style="info" %}
🧙 If you only want to retrieve a user's profile `getProfile` is the perfect function, but if you also need to retrieve his wallets and even authenticate the user, then it is recommended to [retrieve the user account](retrieve-a-user-account.md).
{% endhint %}

## Function

```javascript
arkaneConnect.api.getProfile()
```

## Example

```javascript
const arkaneConnect = new ArkaneConnect('YOUR_CLIENT_ID'); 
arkaneConnect.api.getProfile().then((profile) => {
   console.log(`Users email, ${profile.email}, has been successfully executed!`);
});
```

## Returns

```javascript
{
  "userId": "46c87fcb-77ed-4433-a425-814569ca1672",
  "hasMasterPin": true,
  "username": "karel.striegel@arkane.network",
  "email": "karel.striegel@arkane.network",
  "firstName": "Karel",
  "lastName": "Striegel"
}

```

## Function Reference

The function reference describes the different functions that are available in the Widget. For each function you can find the signature, its parameters, and possible options documented. 

{% page-ref page="../widget-advanced/reference/getprofile.md" %}

