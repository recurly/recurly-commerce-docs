---
title: Discount codes
excerpt: >-
  Learn how to create and apply Shopify discount codes to your Recurly Commerce
  subscriptions—no extra setup in Recurly needed.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Recurly Commerce reads in your existing Shopify discount codes so you can apply them directly to subscription contracts. All code creation and configuration happens in Shopify.

### Video

<Embed typeOfEmbed="iframe" url="https://www.loom.com/embed/e6c87287c23d4411b59c333f985623ed" href="https://www.loom.com/embed/e6c87287c23d4411b59c333f985623ed" html="false" iframe="true" />

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Discount codes must be created and managed in Shopify.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Recurly Commerce cannot generate new codes—only import and apply existing ones.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

A discount code in Recurly Commerce is a Shopify-created promo code that you can attach to a subscriber’s contract, applying the same rules and values you set in Shopify.

# Key benefits

* **Instant savings for subscribers**: Offer percentage or fixed‐amount discounts on subscription renewals.
* **Zero duplication of effort**: Create codes once in Shopify, then use them in Recurly Commerce without extra setup.
* **Omnichannel application**: Apply codes at checkout, via the customer portal, or in the merchant admin for targeted promotions.

# Key details

## Creating a discount code in Shopify

1. **Go** to **Discounts** in your Shopify admin and click **Create discount** (green button, top right).

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/d3f1ea4060d6c9f93c3e88149e086528ba401fd73a70bd23040622e4660eb1fb-image.png" />

2. **Select** **Amount off order**, choose percentage or fixed amount. This determines how much to subtract from each renewal.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/9096cae7ecb7976e0f191af080b1f874a5b2a7648e2a3dbbfb291be2874177d8-image.png" />

> **Note:** When naming your code, avoid special characters (%, $, &, etc.)

3. Under **Purchase type**, **choose** **Subscription** or **Both** to make the code available for subscription orders. Complete any other fields, then **click** **Save**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/df33fcdb5477287b97b0c9d41c6b57990f3d53a7bb70ce20c5bf32116c9b0d8d-image.png" />

## Adding a discount code to a subscription

1. **Navigate** to the **Customers** tab in Recurly Commerce and locate the subscriber’s contract.
2. **Click** the **Coupon Code** button.
3. **Enter** the Shopify code exactly as created, then click **Apply**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/989da17991673ae79871dab09350954762fb1ea5de068f9999b30b81ab8654fe-image.png" />

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/4606e311a6626c13dc2a0a2ca1c44e27140fbc683294cd73b6319e333da98889-image.png" />

The code’s parameters—minimum purchase, usage limits, applicable products—are enforced exactly as defined in Shopify. You can apply it:

* During the first subscription checkout
* In the customer portal
* In the merchant **Customers** tab

### Shopify discount code resource

For full details on creating and managing discount codes in Shopify, [learn more here.](https://help.shopify.com/en/manual/discounts/managing-discount-codes)