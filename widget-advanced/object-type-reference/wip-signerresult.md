# SignerResult

## Signature

```javascript
{
    status: 'SUCCESS' | 'ABORTED' | 'FAILED',
    result?: any,
    errors?: []
}
```

## Parameters

| Parameter | Description |
| :--- | :--- |
| `status` | The status of the transaction: `SUCCESS:`Request is successfully executed. `ABORTED:`User closed the popup or clicked the '_back to the application'_ link. `FAILED:` Something went wrong while trying to process the request. |
| `result` | An object containing the result of the sign action, this is different for different actions. It can contain the `transactionHash` of a transaction or the `signedTransaction` of the requested data. |
| `errors` | Array containing the errors of the transaction that you tried to execute. |

## Examples

```javascript
//Launching a transaction
const signer = arkaneConnect.createSigner();

signer.executeTransfer({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    to: '0xf147cA0b981C0CD0955D1323DB9980F4B43e9FED',
    value: 3.14159265359,
    secretType: 'ETHEREUM',
}).then((signerResult) => {
   if (signerResult.success) {
       console.log(`Transaction ${signerResult.result.transactionHash} has been successfully executed!`);
   } else {
       console.warn(`Something went wrong while executing the transaction`);
   }
}).catch((reason) => {
    console.log(error);
});
```

```javascript
//Signing data
const signer = arkaneConnect.createSigner();
signer.sign({...signatureRequest...})
      .then((signerResult) => {
          if (signerResult.success) {
              console.log(`Successfuly signed: ${signerResult.result.signedTransaction}`);
          } else {
              console.warn(`Something went wrong while signing the request`);
          }
      }).catch((reason) => {
          console.log(error);
      });
```

```javascript
//Signing a message
const signer = arkaneConnect.createSigner();

signer.signMessage({
    walletId: '71dec640-4eb8-4321-adb8-b79461573fc4',
    secretType: 'ETHEREUM',
    data : "I agree with terms and conditions"
}).then((signerResult) => {
    if (signerResult.success) {
        console.log(`Successfuly signed: ${signerResult.result.signature}`);
    } else {
        console.warn(`Something went wrong while signing the message`);
    }
}).catch((reason) => {
    console.log(error);
});

```

```javascript
{
    result: {
        transactionHash: "0xe18975940be795f178b2a0bc553a0d40e0ad6ceb72ee5f62ac53f0a816b4460f"
    }
    status: "SUCCESS"
}
```

## Function Types

{% page-ref page="../reference/executetransfer.md" %}

{% page-ref page="../reference/executetokentransfer.md" %}

{% page-ref page="../reference/executenfttransfer.md" %}

{% page-ref page="../reference/executecontract.md" %}

{% page-ref page="../reference/executegastransfer.md" %}

{% page-ref page="../reference/signmessage.md" %}

