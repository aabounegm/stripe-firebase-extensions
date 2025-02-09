<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@stripe/firestore-stripe-payments](./firestore-stripe-payments.md) &gt; [onCurrentUserSubscriptionUpdate](./firestore-stripe-payments.oncurrentusersubscriptionupdate.md)

## onCurrentUserSubscriptionUpdate() function

Registers a listener to receive subscription update events for the currently signed in user. If the user is not signed in throws an `unauthenticated` error, and no listener is registered.

Upon successful registration, the `onUpdate` callback will fire once with the current state of all the subscriptions. From then onwards, each update to a subscription will fire the `onUpdate` callback with the latest state of the subscriptions.

<b>Signature:</b>

```typescript
export declare function onCurrentUserSubscriptionUpdate(payments: StripePayments, onUpdate: (snapshot: SubscriptionSnapshot) => void, onError?: (error: StripePaymentsError) => void): () => void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  payments | [StripePayments](./firestore-stripe-payments.stripepayments.md) | A valid [StripePayments](./firestore-stripe-payments.stripepayments.md) object. |
|  onUpdate | (snapshot: [SubscriptionSnapshot](./firestore-stripe-payments.subscriptionsnapshot.md)<!-- -->) =&gt; void | A callback that will fire whenever the current user's subscriptions are updated. |
|  onError | (error: [StripePaymentsError](./firestore-stripe-payments.stripepaymentserror.md)<!-- -->) =&gt; void | A callback that will fire whenever an error occurs while listening to subscription updates. |

<b>Returns:</b>

() =&gt; void

A function that can be called to cancel and unregister the listener.

