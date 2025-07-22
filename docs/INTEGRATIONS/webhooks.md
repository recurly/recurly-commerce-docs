---
title: Webhooks
excerpt: >-
  Enable real-time event syncing between Recurly Commerce and merchant systems
  using secure outbound webhooks.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

### Prerequisites & limitations

* A `webhookSigningKey` must be generated and stored for each merchant before they can subscribe to webhook events.
* Merchants must verify webhook request signatures using the shared key.
* Currently, there is no standalone Retool for creating a webhook key entry—one must be created manually or via a separate mechanism.

## Definition

Outbound webhooks allow Recurly to notify merchants about key events—such as subscription changes or billing attempts—by sending signed HTTP requests to a merchant-defined endpoint.

## Key benefits

* **Real-time updates**: Merchants receive immediate notifications of critical subscription and billing events.
* **Secure integration**: All requests are signed using a merchant-specific key to verify authenticity.
* **Event-driven workflows**: Enables custom workflows or data syncing based on specific subscription activity.

## Key details

### Setting up webhook access

To allow merchants to subscribe to webhooks:

1. A `webhookSigningKey` must be created for the merchant. This key is shared securely and used to sign all webhook requests.
2. Merchants must use this key to validate the `X-Recurly-Signature` header in received requests.

> **Note:** Avoid generating a public API token solely to create a webhook key. Instead, we recommend using a dedicated internal tool or new Retool component.

Once the signing key is in place, merchants can subscribe to webhooks using our [public API](https://docs.recurly.com/recurly-commerce/reference/publicapicontroller_createwebhook#/).

### Webhook topics

| Topic                                   | Description                                     | Payload Code Link         |
| --------------------------------------- | ----------------------------------------------- | ------------------------- |
| `subscriptions/created`                 | A new subscription is created in Recurly        | Subscription payload      |
| `subscriptions/line_removed`            | A line item is removed from a subscription      | Subscription payload      |
| `subscriptions/status/updated`          | Subscription status was updated                 | Subscription payload      |
| `orders/created`                        | A new order has been created for a subscription | Order payload             |
| `billingAttempts/created`               | A billing attempt was initiated                 | Billing attempt payload   |
| `billingAttempts/success`               | A billing attempt was successful                | Billing attempt payload   |
| `billingAttempts/failed`                | A billing attempt failed                        | Billing attempt payload   |
| `paymentMethod/updated`                 | A customer’s payment method was updated         | Subscription payload      |
| `subscriptionActivities/created`        | A new activity was logged on a subscription     | Activity payload          |
| `subscription/customAttributes/updated` | A subscription’s custom attributes were updated | Custom attributes payload |

### Payload structure

Webhook payloads follow this general structure:

```json
{
  "topic": "webhook_topic",
  "idempotencyKey": "123",
  "data": { /* event-specific data */ }
}
```

### Example: `subscriptions/created` payload

```json
{
   "topic":"subscriptions/created",
   "idempotencyKey":"123",
   "data":{
      "id":"subscriptionContract.id",
      "createdAt":"subscriptionContract.createdAt",
      "updatedAt":"subscriptionContract.updatedAt",
      "friendlyId":"subscriptionContract.friendlyId",
      "externalId":"subscriptionContract.internalId",
      "subscriber":{
         "id":"shopper.id",
         "createdAt":"shopper.createdAt",
         "updatedAt":"shopper.updatedAt",
         "externalId":"merchantShopperRelationShipInternalId || shopper.providerId",
         "firstName":"shopper.firstName",
         "lastName":"shopper.lastName",
         "email":"shopper.email",
         "phoneCountryCode":"shopper.phoneCountryCode",
         "phone":"shopper.phone"
      },
      "purchaseDate":"subscriptionContract.purchaseDate",
      "cancelDate":"subscriptionContract.cancelDate",
      "cancelReason":"subscriptionContract.cancelReason",
      "pausedAtDate":"subscriptionContract.pausedAtDate",
      "nextDeliveryDate":"subscriptionContract.adjustedNextDeliveryDate",
      "nextBillingDate":"subscriptionContract.adjustedNextBillingDate",
      "status":"subscriptionContract.status",
      "deliveryCadenceCount":"subscriptionContract.deliveryCadenceCount",
      "deliveryCadenceUnit":"subscriptionContract.deliveryCadenceUnit",
      "billingCadenceCount":"subscriptionContract.billingCadenceCount",
      "billingCadenceUnit":"subscriptionContract.billingCadenceUnit",
      "isPrepaid":"subscriptionContract.isPrepaid",
      "isMembership":"subscriptionContract.isMembership",
      "currencyCode":"subscriptionContract.currencyCode",
      "deliveryFirstName":"subscriptionContract.deliveryFirstName",
      "deliveryLastName":"subscriptionContract.deliveryLastName",
      "deliveryAddress1":subscriptionContract.deliveryAddress1,
      "deliveryAddress2":subscriptionContract.deliveryAddress2,
      "deliveryCountry":"subscriptionContract.deliveryCountry",
      "deliveryProvince":"subscriptionContract.deliveryProvince",
      "deliveryCity":"subscriptionContract.deliveryCity",
      "deliveryZip":"subscriptionContract.deliveryZip",
      "deliveryShippingOption":"subscriptionContract.deliveryShippingOption",
      "deliveryPrice":"subscriptionContract.deliveryPrice",
      "deliveryPhone":"subscriptionContract.deliveryPhone",
      "deliveryCompany":"subscriptionContract.deliveryCompany",
      "billingFirstName":"subscriptionContract.billingFirstName",
      "billingLastName":"subscriptionContract.billingLastName",
      "billingAddress1":subscriptionContract.billingAddress1,
      "billingAddress2":subscriptionContract.billingAddress2,
      "billingCountry":"subscriptionContract.billingCountry",
      "billingProvince":"subscriptionContract.billingProvince",
      "billingCity":"subscriptionContract.billingCity",
      "billingZip":"subscriptionContract.billingZip",
      "paymentMethodExternalId":"subscriptionContract.creditCardInternalId",
      "paymentMethodBrand":"subscriptionContract.creditCardBrand",
      "paymentMethodEmail":"subscriptionContract.paymentMethodEmail",
      "paymentMethodExpiryMonth":"subscriptionContract.creditCardExpiryMonth",
      "paymentMethodExpiryYear":"subscriptionContract.creditCardExpiryYear",
      "paymentMethodType":"subscriptionContract.paymentMethodType",
      "paymentMethodLast4Digits":"subscriptionContract.creditCardLastDigits",
      "paymentMethodName":"subscriptionContract.creditCardName",
      "pauseLimitSettings":"subscriptionContract.pauseLimitSettings",
      "lines":[
         {
            "id":"line.id",
            "createdAt":"line.createdAt",
            "updatedAt":"line.updatedAt",
            "externalId":"line.internalId",
            "subscriptionId":"line.subscriptionContractId",
            "variant":{
               "id":"variant.id",
               "externalId":"variant.providerVariantId",
               "status":"variant.status",
               "currentPrice":"variant.currentPrice",
               "variantTitle":"variant.variantTitle",
               "sku":"variant.sku",
               "product":{
                  "id":"product.id",
                  "createdAt":"product.createdAt",
                  "updatedAt":"product.updatedAt",
                  "externalId":"product.providerProductId",
                  "imageUrl":"product.imageUrl",
                  "productTitle":"product.productTitle",
                  "description":"product.description"
               }
            },
            "quantity":"line.quantity",
            "currentPrice":"line.currentPrice",
            "subscriptionOfferOptionId":"line.subscriptionOfferOption.id",
            "sellingPlanId":"line.subscriptionOfferOption.sellingPlanId",
            "schedule":{
               "id":"schedule.id",
               "deliveryInterval":"schedule.deliveryInterval",
               "deliveryStartOffset":"schedule.deliveryStartOffset",
               "lastIncludedOrderNumber":"schedule.lastIncludedOrderNumber",
               "lastIncludedDate":"schedule.lastIncludedDate",
               "createdAt":"schedule.createdAt",
               "updatedAt":"schedule.updatedAt"
            },
            "customAttributes":"line.customAttributes"
         }
      ],
      "upcomingOrders":[
         {
            "scheduledDate":"uo.scheduledDate",
            "isSkipped":"uo.isSkipped",
            "lines":[
               {
                  "id":"line.id",
                  "createdAt":"line.createdAt",
                  "variantTitle":"variant.variantTitle",
                  "sku":"variant.sku",
                  "product":{
                     "id":"product.id",
                     "createdAt":"product.createdAt",
                     "updatedAt":"product.updatedAt",
                     "externalId":"product.providerProductId",
                     "imageUrl":"product.imageUrl",
                     "productTitle":"product.productTitle",
                     "description":"product.description"
                  }
               },
               "quantity":"line.quantity",
               "currentPrice":"line.currentPrice",
               "subscriptionOfferOptionId":"line.subscriptionOfferOption.id",
               "sellingPlanId":"line.subscriptionOfferOption.sellingPlanId",
               "schedule":{
                  "id":"schedule.id",
                  "deliveryInterval":"schedule.deliveryInterval",
                  "deliveryStartOffset":"schedule.deliveryStartOffset",
                  "lastIncludedOrderNumber":"schedule.lastIncludedOrderNumber",
                  "lastIncludedDate":"schedule.lastIncludedDate",
                  "createdAt":"schedule.createdAt",
                  "updatedAt":"schedule.updatedAt"
               },
               "customAttributes":"line.customAttributes"
            }
         ],
         "upcomingOrders":[
            {
               "scheduledDate":"uo.scheduledDate",
               "isSkipped":"uo.isSkipped",
               "lines":[
                  {
                     "id":"line.id",
                     "createdAt":"line.createdAt",
                     "updatedAt":"line.updatedAt",
                     "externalId":"line.internalId",
                     "subscriptionId":"line.subscriptionContractId",
                     "variant":{
                        "id":"variant.id",
                        "externalId":"variant.providerVariantId",
                        "status":"variant.status",
                        "currentPrice":"variant.currentPrice",
                        "variantTitle":"variant.variantTitle",
                        "sku":"variant.sku",
                        "product":{
                           "id":"product.id",
                           "createdAt":"product.createdAt",
                           "updatedAt":"product.updatedAt",
                           "externalId":"product.providerProductId",
                           "imageUrl":"product.imageUrl",
                           "productTitle":"product.productTitle",
                           "description":"product.description"
                        }
                     },
                     "quantity":"line.quantity",
                     "currentPrice":"line.currentPrice",
                     "subscriptionOfferOptionId":"line.subscriptionOfferOption.id",
                     "sellingPlanId":"line.subscriptionOfferOption.sellingPlanId",
                     "schedule":{
                        "id":"schedule.id",
                        "deliveryInterval":"schedule.deliveryInterval",
                        "deliveryStartOffset":"schedule.deliveryStartOffset",
                        "lastIncludedOrderNumber":"schedule.lastIncludedOrderNumber",
                        "lastIncludedDate":"schedule.lastIncludedDate",
                        "createdAt":"schedule.createdAt",
                        "updatedAt":"schedule.updatedAt"
                     },
                     "customAttributes":"line.customAttributes"
                  }
               ],
               "oneTimeAddOns":[
                  {
                     "id":"o.id",
                     "variantId":"o.variant.id",
                     "quantity":"o.quantity"
                  }
               ]
            }
         ],
         "customAttributes":"subscriptionContract.customAttributes",
         "gift":{
            "id":"gift.id",
            "createdAt":"gift.createdAt",
            "updatedAt":"gift.updatedAt",
            "numberOfDeliveries":"gift.numberOfDeliveries",
            "to":"gift.to",
            "email":"gift.email",
            "message":"gift.message",
            "isOpened":"gift.isOpened",
            "isPrepaid":"gift.isPrepaid"
         },
         "recipient":{
            "id":"shopper.id",
            "createdAt":"shopper.createdAt",
            "updatedAt":"shopper.updatedAt",
            "externalId":"merchantShopperRelationShipInternalId || shopper.providerId",
            "firstName":"shopper.firstName",
            "lastName":"shopper.lastName",
            "email":"shopper.email",
            "phoneCountryCode":"shopper.phoneCountryCode",
            "phone":"shopper.phone"
         },
         "discountCodes":[
            {
               "id":"subscriptionContractDiscount.id",
               "createdAt":"subscriptionContractDiscount.createdAt",
               "updatedAt":"subscriptionContractDiscount.updatedAt",
               "deletedAt":"subscriptionContractDiscount.deletedAt",
               "subscriptionId":"subscriptionContractDiscount.subscriptionContractId",
               "code":"subscriptionContractDiscount.title",
               "discountCodeExternalId":"subscriptionContractDiscount.providerId",
               "type":"subscriptionContractDiscount.type",
               "targetType":"subscriptionContractDiscount.targetType",
               "discountModifier":"subscriptionContractDiscount.discountModifier",
               "discount":"subscriptionContractDiscount.discount",
               "recurringCycleLimit":"subscriptionContractDiscount.recurringCycleLimit",
               "usageCount":"subscriptionContractDiscount.usageCount"
            }
         ],
         "dunningInstances":[
            {
               "createdAt":"dunningContract.createdAt",
               "dunningComplete":"dunningContract.dunningComplete",
               "lastRetryDate":"dunningContract.lastRetryDate",
               "billingRetryCount":"dunningContract.billingRetryCount",
               "maxBillingRetryCount":"dunningContract.maxBillingRetryCount",
               "errorCode":"dunningContract.errorCode",
               "isReactivated":"dunningContract.isReactivated",
               "contractCancelledAt":"dunningContract.contractCancelledAt",
               "maxBillingRetryCountAction":"dunningContract.maxBillingRetryCountAction"
            }
         ]
      }
   }
```