---
title: Widget API
excerpt: >-
  Comprehensive reference for the Recurly Commerce storefront widget API,
  including endpoints, full JSON payload examples, and configuration details.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Requires a live Recurly Commerce integration on Shopify with storefront widget enabled.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Only available for stores using Recurly Commerce Subscription Offers.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

The Widget API provides RESTful endpoints and JSON payloads that expose:

1. Product details and selling plan groups.
2. Individual selling plan definitions (frequency, pricing, discounts, gifting).
3. Store theme and widget styling settings.

# Key benefits

* **Dynamic storefront integration**: Retrieve up-to-date subscription options directly in your theme.
* **Full subscription context**: Access discounts, cadence, and gifting rules without additional API calls.
* **Customizable appearance**: Pull theme settings to ensure widget styles match your storefront.

# Key details

## Links

* Shopify Subscription Documentation: [https://shopify.dev/apps/subscriptions](https://shopify.dev/apps/subscriptions)
* Selling Plan Fields: [https://shopify.dev/api/admin-graphql/2022-07/objects/sellingplan](https://shopify.dev/api/admin-graphql/2022-07/objects/sellingplan)

## Liquid objects

Recurly Commerce data is available in standard Shopify Liquid objects:

* [Product](https://shopify.dev/api/liquid/objects#product)
* [Selling Plan](https://shopify.dev/api/liquid/objects#selling_plan)

## Product details

Fetch the subscription metadata for a product:

```text
GET https://subs.api.tryprive.com/stores/${storeUrl}/products/${productId}/new
```

### Selling plan groups

Represents a selling mode (e.g. “Subscribe & save” or “Pre-paid”).

```json
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

### Hybrid example (One-time, subscribe & save, prepaid)

```json
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

## Store theme

Retrieve widget styling and copy overrides for the active theme:

```text
GET https://subs.api.tryprive.com/stores/${storeUrl}/settings?themeId=<theme_id>
```

```json
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