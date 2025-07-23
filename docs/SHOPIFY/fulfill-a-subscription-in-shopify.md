---
title: Fulfill a subscription in Shopify
excerpt: >-
  Learn how to fulfill subscription orders directly in Shopify when using
  Recurly Commerce—no extra setup required.
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
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          All fulfillment must occur in Shopify—Recurly Commerce does not handle shipping or packing.
        </p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          You must have access to your Shopify admin “Orders” section.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Fulfilling a subscription in Shopify means processing and shipping each renewal order through Shopify’s native order management tools. Once Recurly Commerce charges the customer via Shopify Payments, the order appears in Shopify for you to pick, pack, and ship.

# Key benefits

* **Unified operations**: Manage both one-time and subscription orders from the same Shopify interface.
* **Accurate tracking**: Leverage Shopify’s fulfillment and shipment notifications to keep customers updated.
* **No extra configuration**: Simply use your existing Shopify workflows—no new apps or processes needed.

# Key details

## Fulfilling a subscription order in Shopify

All order fulfillment should be handled in Shopify. Recurly Commerce leverages Shopify Payments to process renewals, then relies on Shopify’s built-in fulfillment tools:

1. **Navigate** to the **Orders** tab of your Shopify admin.
2. **Select** the subscription order (or search by customer).
3. **Click** **Fulfill item** to pick, pack, and ship.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/a9b820ec9c524d6d40b8462983c5602c941255c671cbe66b3a486680d0aeebe7-asd.gif" />