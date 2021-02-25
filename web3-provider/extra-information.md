---
description: Use the force Luke ✨
---

# Power of the Widget

Although we use the widget under the hood, the functionality of the web3 wrapper isn’t limited to the web3 API. Linking or fetching profile information is not supported by Web3, but it is available in our wrapper. After creating an Arkane Provider Engine,  an instance of **ArkaneConnect** is added to the global **Arkane** object. As a result, it’s possible to call the widget natively, like so.

```text
Arkane.arkaneConnect().api.getProfile();
```

The full documentation of the Widget can be found here.





