---
title: Getting Started With Prive Widget API
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## Overview

The Prive Widget API can be used to get the product information for a given productId or get the specific settings of your store.

## API Details

### Product Information

```
method GET
https://subs.api.tryprive.com/stores/${storeUrl}/products/${productId}/new
```

#### Prepaid - Example

```jsx
{
    "productId": "gid://shopify/Product/7604549058805",
    "hasVariantLevel": false,
    "selling_plan_groups": [
        {
            "requires_selling_plan": true,
            "id": "gid://shopify/SellingPlanGroup/628818165",
            "type": "PREPAID_SUBSCRIPTION_ONLY",
            "variants": [],
            "selling_plans": [
                {
                    "variants": null,
                    "specialDiscountActive": true,
                    "specialDiscount": 12,
                    "discountType": "QUANTITY",
                    "specialDiscountModifier": null,
                    "numberOfOrders": 3,
                    "shippingDiscount": null,
                    "specialDiscountType": "QUANTITY",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/628818165",
                    "sellingPlanId": "3192750325",
                    "discount": 4,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": null,
                    "deliveryCadenceCount": 2,
                    "deliveryCadenceUnit": "MONTH",
                    "billingCadenceCount": 12,
                    "billingCadenceUnit": "MONTH",
                    "type": "PREPAID_SUBSCRIPTION_ONLY",
                    "name": "Delivery every 2 months, prepay every 12 months - 4% off",
                    "nameOverride": "Name Custom Discount",
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "PREPAID_SUBSCRIPTION_ONLY",
                    "giftOptions": null
                },
                {
                    "variants": null,
                    "specialDiscountActive": true,
                    "specialDiscount": 12,
                    "discountType": "QUANTITY",
                    "specialDiscountModifier": null,
                    "numberOfOrders": 3,
                    "shippingDiscount": null,
                    "specialDiscountType": "QUANTITY",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/628818165",
                    "sellingPlanId": "3192881397",
                    "discount": 15,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": null,
                    "deliveryCadenceCount": 1,
                    "deliveryCadenceUnit": "MONTH",
                    "billingCadenceCount": 12,
                    "billingCadenceUnit": "MONTH",
                    "type": "PREPAID_SUBSCRIPTION_ONLY",
                    "name": "Delivery every 1 month, prepay every 12 months - 15% off",
                    "nameOverride": "1m X 12 months",
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "PREPAID_SUBSCRIPTION_ONLY",
                    "giftOptions": null
                },
                {
                    "variants": null,
                    "specialDiscountActive": true,
                    "specialDiscount": 12,
                    "discountType": "QUANTITY",
                    "specialDiscountModifier": null,
                    "numberOfOrders": 3,
                    "shippingDiscount": null,
                    "specialDiscountType": "QUANTITY",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/628818165",
                    "sellingPlanId": "3193012469",
                    "discount": 24,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": null,
                    "deliveryCadenceCount": 3,
                    "deliveryCadenceUnit": "MONTH",
                    "billingCadenceCount": 6,
                    "billingCadenceUnit": "MONTH",
                    "type": "PREPAID_SUBSCRIPTION_ONLY",
                    "name": "Delivery every 3 months, prepay every 6 months - 24% off",
                    "nameOverride": null,
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "PREPAID_SUBSCRIPTION_ONLY",
                    "giftOptions": null
                }
            ]
        }
    ]
}
```

#### One-time, Subscribe & Save, Prepaid - Example

```jsx
{
    "productId": "gid://shopify/Product/7604549058805",
    "hasVariantLevel": false,
    "selling_plan_groups": [
        {
            "requires_selling_plan": false,
            "id": "gid://shopify/SellingPlanGroup/633340149",
            "type": "ONETIME_AND_SUBSCRIPTION_AND_PREPAID",
            "variants": [],
            "selling_plans": [
                {
                    "variants": null,
                    "specialDiscountActive": false,
                    "specialDiscount": null,
                    "discountType": "NONE",
                    "specialDiscountModifier": null,
                    "numberOfOrders": null,
                    "shippingDiscount": null,
                    "specialDiscountType": "NONE",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/633340149",
                    "sellingPlanId": "3203006709",
                    "discount": 10,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": 1,
                    "deliveryCadenceCount": 3,
                    "deliveryCadenceUnit": "WEEK",
                    "billingCadenceCount": 3,
                    "billingCadenceUnit": "WEEK",
                    "type": "ONETIME_AND_SUBSCRIPTION_AND_PREPAID",
                    "name": "Delivery every 3 weeks - 10% off",
                    "nameOverride": null,
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "ONETIME_AND_SUBSCRIPTION",
                    "giftOptions": null
                },
                {
                    "variants": null,
                    "specialDiscountActive": false,
                    "specialDiscount": null,
                    "discountType": "NONE",
                    "specialDiscountModifier": null,
                    "numberOfOrders": null,
                    "shippingDiscount": null,
                    "specialDiscountType": "NONE",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/633340149",
                    "sellingPlanId": "3203039477",
                    "discount": 15,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": 2,
                    "deliveryCadenceCount": 12,
                    "deliveryCadenceUnit": "WEEK",
                    "billingCadenceCount": 12,
                    "billingCadenceUnit": "WEEK",
                    "type": "ONETIME_AND_SUBSCRIPTION_AND_PREPAID",
                    "name": "Delivery every 12 weeks - 15% off",
                    "nameOverride": null,
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "ONETIME_AND_SUBSCRIPTION",
                    "giftOptions": null
                },
                {
                    "variants": null,
                    "specialDiscountActive": false,
                    "specialDiscount": null,
                    "discountType": "NONE",
                    "specialDiscountModifier": null,
                    "numberOfOrders": null,
                    "shippingDiscount": null,
                    "specialDiscountType": "NONE",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/633340149",
                    "sellingPlanId": "3203072245",
                    "discount": 12,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": 3,
                    "deliveryCadenceCount": 4,
                    "deliveryCadenceUnit": "WEEK",
                    "billingCadenceCount": 4,
                    "billingCadenceUnit": "WEEK",
                    "type": "ONETIME_AND_SUBSCRIPTION_AND_PREPAID",
                    "name": "Delivery every 4 weeks - 12% off",
                    "nameOverride": null,
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "ONETIME_AND_SUBSCRIPTION",
                    "giftOptions": null
                },
                {
                    "variants": null,
                    "specialDiscountActive": false,
                    "specialDiscount": null,
                    "discountType": "NONE",
                    "specialDiscountModifier": null,
                    "numberOfOrders": null,
                    "shippingDiscount": null,
                    "specialDiscountType": "NONE",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/633340149",
                    "sellingPlanId": "3203105013",
                    "discount": 15,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": 4,
                    "deliveryCadenceCount": 1,
                    "deliveryCadenceUnit": "MONTH",
                    "billingCadenceCount": 6,
                    "billingCadenceUnit": "MONTH",
                    "type": "ONETIME_AND_SUBSCRIPTION_AND_PREPAID",
                    "name": "Delivery every 1 month, prepay every 6 months - 15% off",
                    "nameOverride": null,
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "PREPAID_SUBSCRIPTION_ONLY",
                    "giftOptions": null
                },
                {
                    "variants": null,
                    "specialDiscountActive": false,
                    "specialDiscount": null,
                    "discountType": "NONE",
                    "specialDiscountModifier": null,
                    "numberOfOrders": null,
                    "shippingDiscount": null,
                    "specialDiscountType": "NONE",
                    "sellingPlanGroupId": "gid://shopify/SellingPlanGroup/633340149",
                    "sellingPlanId": "3203137781",
                    "discount": 20,
                    "discountModifier": "PERCENTAGE",
                    "optionOrder": 5,
                    "deliveryCadenceCount": 2,
                    "deliveryCadenceUnit": "MONTH",
                    "billingCadenceCount": 6,
                    "billingCadenceUnit": "MONTH",
                    "type": "ONETIME_AND_SUBSCRIPTION_AND_PREPAID",
                    "name": "Delivery every 2 months, prepay every 6 months - 20% off",
                    "nameOverride": null,
                    "visibility": null,
                    "isDefault": false,
                    "discountCode": null,
                    "optionType": "PREPAID_SUBSCRIPTION_ONLY",
                    "giftOptions": null
                }
            ]
        }
    ]
}
```

### Store Theme

```
method GET
https://subs.api.tryprive.com/stores/<shopify store url>/settings?themeId=<theme_id>
```

```jsx
{
    "currency": "USD",
    "money_format": "${{amount}} USD",
    "multilocation": true,
    "widget_settings": {
        "elements": {
            "buttonPrice": "not-existing-tag"
        },
        "customCss": null,
        "onetimeFirst": false,
        "onetimeCopy": null,
        "subscribeCopy": "Discount Subscription",
        "prepaidCopy": "Prepaid Subscription",
        "subOptionCopy": null,
        "styling": {
            "bgColor": null,
            "borders": null,
            "accentColor": "#000000",
            "quantityStyle": null,
            "bgColorOnSelection": "#dbe4ff",
            "deliveryEveryStyle": null,
            "purchaseOptionsStyle": null,
            "selectedOptionsStyle": {
                "color": "#000000",
                "fontSize": "1",
                "fontWeight": "bold"
            }
        },
        "rank": null
    }
}
```

## References

### Links

* [Shopify Subscription Documentation](https://shopify.dev/docs/apps/selling-strategies/subscriptions)
* Selling Plan Fields: [https://shopify.dev/api/admin-graphql/2022-07/objects/sellingplan](https://shopify.dev/api/admin-graphql/2022-07/objects/sellingplan)

### Liquid Objects

Prive subscription related data is available in Shopify liquid template objects

* [Product](https://shopify.dev/api/liquid/objects#product)
* [Selling Plan](https://shopify.dev/api/liquid/objects#selling_plan)
